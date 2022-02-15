---
title: JavaScript Code for [!DNL Analytics for Advertising Cloud]
description: Código JavaScript para [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 7bf8f3524954b17d9da336a2210a098bf571399e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# Código JavaScript para [!DNL Analytics for Advertising Cloud]

*Advertisers with an Advertising Cloud-Adobe Analytics Integration Only*

*Anunciantes solo con Advertising Cloud DSP*

Para Advertising Cloud DSP, la variable [!DNL Analytics for Advertising Cloud] la integración realiza el seguimiento de las interacciones del sitio de pulsaciones y visualizaciones. Las visitas de pulsaciones se rastrean mediante el código estándar de Adobe Analytics en sus páginas web; el [!DNL Analytics] captura los parámetros de ID de AMO e ID de EF en la dirección URL de la página de aterrizaje y los rastrea en sus eVars reservadas respectivas. Puede realizar un seguimiento de las visitas mediante la implementación de un fragmento de JavaScript en las páginas web.

On the first page view of a visit to the site, the Advertising Cloud JavaScript code checks to see if the visitor has previously seen or clicked on an ad. Si el usuario ha entrado previamente al sitio mediante un clic o no ha visto una publicidad, se ignora al visitante. If the visitor has seen an ad and hasn&#39;t entered the site via a click-through during the [click lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc) set within Advertising Cloud, then the Advertising Cloud JavaScript code either a) uses the [Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) to generate a supplemental ID (`SDID`) or b) uses the Adobe Experience Platform [!DNL Web SDK] `generateRandomID` method to generate a `[!DNL StitchID]`. Cualquiera de los ID se utiliza para unir datos de Advertising Cloud a la visita de Adobe Analytics del visitante. A continuación, Adobe Analytics consulta a Advertising Cloud el ID de AMO y el ID de EF asociados a la exposición del anuncio. The AMO ID and EF IDs are then populated in their respective eVars. These values persist for a designated period (by default, 60 days).

[!DNL Analytics] sends site traffic metrics (such as page views, visits, and time spent) and any [!DNL Analytics] custom or standard events to Advertising Cloud hourly, using the EF ID as the key. These [!DNL Analytics] metrics then run through the Advertising Cloud attribution system to connect the conversions to the click and exposure history.

>[!NOTE]
>
>The Advertising Cloud JavaScript tracking logic occurs on the Adobe side and thus has virtually no impact to the page load time.
>
>In contrast, the logic for the [!DNL DCM] data connector to [!DNL Analytics] (using [!DNL Google Campaign Manager 360]) for Advertising Cloud DSP occurs on the client side. Client-side stitching slows down the page load and increases the risk of data loss. Esto ocurre porque la variable [!DNL Analytics] JavaScript debe hacer ping [!DNL DoubleClick] y esperar [!DNL DoubleClick] para devolver los datos de último clic o impresión a [!DNL Analytics]. When your [!DNL DSP] team sets up the [!DNL DCM] data connector, you must specify how long you&#39;re willing to delay the page.

## Deploying the JavaScript Code

The JavaScript library consists of two lines that allow [!DNL Analytics] and Advertising Cloud to communicate with each other. If the [!DNL Analytics for Advertising Cloud] integration was completed during the Advertising Cloud implementation, then you should have received this code with instructions on how to deploy it.

**(Implementaciones que utilizan el servicio de identidad de Experience Cloud) `visitorAPI.js` code)**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**(Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code)**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### Dónde colocar el código

La variable [!DNL Analytics for Advertising Cloud] La función JavaScript debe estar detrás del servicio de ID de Experience Cloud, pero antes del código de medición de aplicaciones de Analytics para que el ID suplementario (`SDID`) o `[!DNL StitchID]` se puede incluir en la llamada de Analytics.

![Code placement](/help/integrations/assets/a4adc-code-placement.png)

### Validating Code Deployment

Puede realizar la validación utilizando cualquier tipo de herramienta de detector de paquetes (como [!DNL Charles], [!DNL Fiddler]o [!DNL Chrome Developer Tools]) comparando los valores de los cuatro ID entre la solicitud que se dirige a Advertising Cloud y la solicitud que se dirige a [!DNL Analytics], tal como se describe a continuación.

#### How to Confirm the Code with [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Apertura [!DNL Chrome Developer Tools] y haga clic en el botón **Red** pestaña .

1. Cargue una página de sitio web que contenga la variable [!DNL Analytics for Advertising Cloud] JavaScript.

1. Filtre el [!UICONTROL Network] pestaña por `last` y revise dos filas:

   ![Filtrado por última vez](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * The first row is the call to the JavaScript library and is titled `last-event-tag-latest.min.js`.
   * The second row is the call sending the request to Advertising Cloud. It begins as follows: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Si no ve la llamada a Advertising Cloud, es posible que no sea la primera vista de página de la visita. Con fines de prueba, puede eliminar la cookie para que la siguiente llamada sea la primera vista de página de la visita correspondiente:

      1. En la ficha Aplicación , busque la `adcloud` y compruebe que la cookie contiene `_les_v` (última visita) con un valor de `y` y una marca de tiempo UTC epoch que caduca en 30 minutos.
      1. Elimine el `ad cloud` y actualice la página.

1. (Implementaciones que utilizan el servicio de identidad de Experience Cloud) `visitorAPI.js` código) Filtrar en `/b/ss` para ver la visita de Analytics.

   ![Filtrado en `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementaciones que utilizan el Experience Platform [!DNL Web SDK] `alloy.js`código) Filtrar en `/interact` para comprobar que la carga útil de la solicitud en la red perimetral contiene `advertisingStitchID`.

   ![Filtrado en `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Compare los valores de ID entre las dos visitas. Todos los valores se expresarán en parámetros de cadena de consulta, excepto el ID del grupo de informes de la visita de Analytics, que es la ruta de URL inmediatamente después de `/b/ss/`.

   | ID | Analytics Parameter | Red perimetral | Parámetro Advertising Cloud |
   | --- | --- | --- | --- |
   | Experience Cloud IMS Org | `mcorgid` |  | `_les_imsOrgid` |
   | Supplemental Data ID | sdid |  | `_les_sdid` |
   | ID de vinculación | stitchId | `advertisingStitchID` en el `_adcloud` property |  |
   | Grupo de informes de Analytics | El valor después de `/b/ss/` |  | `_les_rsid` |
   | ID de visitante de Experience Cloud | mid |  | `_les_mid` |

   If the ID values match, then the JavaScript implementation is confirmed. Advertising Cloud enviará el [!DNL Analytics] servidor cualquier detalle de seguimiento de pulsaciones o visualizaciones si existe.

#### Confirmar el código con [!DNL Adobe Experience Cloud Debugger]

1. Abra el [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) en su página de inicio.
1. Go to the [!UICONTROL Network] tab.
1. In the [!UICONTROL Solutions Filter] toolbar, click [!UICONTROL Advertising Cloud] and [!UICONTROL Analytics].
1. In the [!UICONTROL Request URL – Hostname] parameter row, locate `lasteventf-tm.everesttech.net`.
1. In the [!UICONTROL Request – Parameters] row, audit the signals generated, similar to Step 3 in &quot;[How to Confirm the Code with [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementaciones que utilizan el servicio de identidad de Experience Cloud) `visitorAPI.js` Asegúrese de que la variable `Sdid` coincide con el parámetro `Supplemental Data ID` en el filtro Adobe Analytics.
   * (Implementaciones que utilizan el Experience Platform [!DNL Web SDK] `alloy.js`(código) Asegúrese de que el valor de la variable `advertisingStitchID` coincide con el parámetro `Sdid` enviado a la red perimetral del Experience Platform.
   * Si el código no se está generando, compruebe que la cookie de Advertising Cloud se haya eliminado en la variable [!UICONTROL Application] pestaña . Once it&#39;s removed, refresh the page and repeat the process.

   ![Auditing [!DNL Analytics for Advertising Cloud] JavaScript code in [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising Cloud]](prerequisites.md)

