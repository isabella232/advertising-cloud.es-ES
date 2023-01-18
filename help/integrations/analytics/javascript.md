---
title: Código JavaScript para [!DNL Analytics for Advertising]
description: Código JavaScript para [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# Código JavaScript para [!DNL Analytics for Advertising]

*Anunciantes con Adobe de solo integración de Advertising-Adobe Analytics*

*Anunciantes con solo DSP publicitario*

Para los DSP publicitarios, la variable [!DNL Analytics for Advertising] la integración realiza el seguimiento de las interacciones del sitio de pulsaciones y visualizaciones. Las visitas de pulsaciones se rastrean mediante el código estándar de Adobe Analytics en sus páginas web; el [!DNL Analytics] captura los parámetros de ID de AMO e ID de EF en la dirección URL de la página de aterrizaje y los rastrea en sus eVars reservadas respectivas. Puede realizar un seguimiento de las visitas mediante la implementación de un fragmento de JavaScript en las páginas web.

En la primera vista de página de una visita al sitio, el código JavaScript de publicidad de Adobe comprueba si el visitante ha visto o hecho clic previamente en un anuncio. Si el usuario ha entrado previamente al sitio mediante un clic o no ha visto una publicidad, se ignora al visitante. Si el visitante ha visto un anuncio y no ha entrado al sitio a través de un clic durante la visita [haga clic en ventana retrospectiva](/help/integrations/analytics/prerequisites.md#lookback-a4adc) dentro de Publicidad de Adobe, el código JavaScript de Publicidad de Adobe a) utiliza la variable [Servicio de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) para generar un ID suplementario (`SDID`) o b) utiliza el Adobe Experience Platform [!DNL Web SDK] `generateRandomID` método para generar un `[!DNL StitchID]`. Cualquiera de los ID se utiliza para unir datos de la publicidad de Adobe a la visita de Adobe Analytics del visitante. A continuación, Adobe Analytics consulta la Publicidad de Adobe para obtener el ID de AMO y el ID de EF asociados con la exposición de la publicidad. A continuación, el AMO ID y los EF ID se rellenan en sus eVars respectivas. Estos valores persisten durante un período designado (de forma predeterminada, 60 días).

[!DNL Analytics] envía métricas de tráfico del sitio (como vistas de página, visitas y tiempo empleado) y [!DNL Analytics] eventos personalizados o estándar para almacenar en Adobe la publicidad por hora, usando el ID de EF como clave. Estos [!DNL Analytics] a continuación, las métricas se ejecutan a través del sistema de atribución de publicidad de Adobe para conectar las conversiones al historial de clics y exposiciones.

>[!NOTE]
>
>La lógica de seguimiento de JavaScript de publicidad de Adobe se produce en el lado del Adobe y, por lo tanto, prácticamente no afecta al tiempo de carga de la página.
>
>Por el contrario, la lógica de la variable [!DNL DCM] conector de datos a [!DNL Analytics] (mediante [!DNL Google Campaign Manager 360]) para Advertising DSP se produce en el lado del cliente. La vinculación del lado del cliente ralentiza la carga de la página y aumenta el riesgo de pérdida de datos. Esto ocurre porque la variable [!DNL Analytics] JavaScript debe hacer ping [!DNL DoubleClick] y esperar [!DNL DoubleClick] para devolver los datos de último clic o impresión a [!DNL Analytics]. Cuando [!DNL DSP] el equipo configura el [!DNL DCM] conector de datos, debe especificar cuánto tiempo está dispuesto a retrasar la página.

## Implementación del código JavaScript

La biblioteca JavaScript consta de dos líneas que permiten [!DNL Analytics] y Adobe Publicidad para comunicarse entre sí. Si la variable [!DNL Analytics for Advertising] La integración se completó durante la implementación de Adobe Advertising, por lo que ya debería haber recibido este código con instrucciones sobre cómo implementarlo.

### El código

#### Implementaciones que utilizan el servicio de identidad de Experience Cloud `visitorAPI.js` code

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### Implementaciones que utilizan el Experience Platform [!DNL Web SDK] `alloy.js`code

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### Dónde colocar el código

La variable [!DNL Analytics for Advertising] La función JavaScript debe estar detrás del servicio de ID de Experience Cloud, pero antes del código de medición de aplicaciones de Analytics para que el ID suplementario (`SDID`) o `[!DNL StitchID]` se puede incluir en la llamada de Analytics.

![Colocación del código](/help/integrations/assets/a4adc-code-placement.png)

### Validación de la implementación de código

Puede realizar la validación utilizando cualquier tipo de herramienta de detector de paquetes (como [!DNL Charles], [!DNL Fiddler]o [!DNL Chrome Developer Tools]) comparando los valores de los cuatro ID entre la solicitud que se dirige a Publicidad de Adobe y la solicitud que se dirige a [!DNL Analytics], tal como se describe a continuación.

#### Confirmar el código con [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Apertura [!DNL Chrome Developer Tools] y haga clic en el botón **Red** pestaña .

1. Cargue una página de sitio web que contenga la variable [!DNL Analytics for Advertising] JavaScript.

1. Filtre el [!UICONTROL Network] pestaña por `last` y revise dos filas:

   ![Filtrado por última vez](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * La primera fila es la llamada a la biblioteca JavaScript y tiene el título `last-event-tag-latest.min.js`.
   * La segunda fila es la llamada que envía la solicitud al Adobe de publicidad. Comienza de la siguiente manera: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Si no ve la llamada a la publicidad de Adobe, es posible que no sea la primera vista de página de la visita. Con fines de prueba, puede eliminar la cookie para que la siguiente llamada sea la primera vista de página de la visita correspondiente:

      1. En la ficha Aplicación , busque la `adcloud` y compruebe que la cookie contiene `_les_v` (última visita) con un valor de `y` y una marca de tiempo UTC epoch que caduca en 30 minutos.
      1. Elimine el `ad cloud` y actualice la página.

1. (Implementaciones que utilizan el servicio de identidad de Experience Cloud) `visitorAPI.js` código) Filtrar en `/b/ss` para ver la visita de Analytics.

   ![Filtrado en `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementaciones que utilizan el Experience Platform [!DNL Web SDK] `alloy.js`código) Filtrar en `/interact` para comprobar que la carga útil de la solicitud en la red perimetral contiene `advertisingStitchID`.

   ![Filtrado en `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Compare los valores de ID entre las dos visitas. Todos los valores se expresarán en parámetros de cadena de consulta, excepto el ID del grupo de informes de la visita de Analytics, que es la ruta de URL inmediatamente después de `/b/ss/`.

   | ID | Parámetro de Analytics | Red perimetral | Parámetro de publicidad de Adobe |
   | --- | --- | --- | --- |
   | Organización IMS del Experience Cloud | `mcorgid` |  | `_les_imsOrgid` |
   | ID de datos suplementario | sdid |  | `_les_sdid` |
   | ID de vinculación | stitchId | `advertisingStitchID` en el `_adcloud` property |  |
   | Grupo de informes de Analytics | El valor después de `/b/ss/` |  | `_les_rsid` |
   | ID de visitante de Experience Cloud | mid |  | `_les_mid` |

   Si los valores de ID coinciden, se confirma la implementación de JavaScript. La publicidad de Adobe enviará la variable [!DNL Analytics] servidor cualquier detalle de seguimiento de pulsaciones o visualizaciones si existe.

#### Confirmar el código con [!DNL Adobe Experience Cloud Debugger]

1. Abra el [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) en su página de inicio.
1. Vaya a la [!UICONTROL Network] pestaña .
1. En el [!UICONTROL Solutions Filter] barra de herramientas, haga clic en [!UICONTROL Adobe Advertising] y [!UICONTROL Analytics].
1. En el [!UICONTROL Request URL – Hostname] fila de parámetros, localizar `lasteventf-tm.everesttech.net`.
1. En el [!UICONTROL Request – Parameters] , audite las señales generadas, de forma similar al paso 3 en &quot;[Confirmar el código con [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementaciones que utilizan el servicio de identidad de Experience Cloud) `visitorAPI.js` Asegúrese de que la variable `Sdid` coincide con el parámetro `Supplemental Data ID` en el filtro Adobe Analytics.
   * (Implementaciones que utilizan el Experience Platform [!DNL Web SDK] `alloy.js`(código) Asegúrese de que el valor de la variable `advertisingStitchID` coincide con el parámetro `Sdid` enviado a la red perimetral del Experience Platform.
   * Si el código no está generando, compruebe que la cookie publicitaria de Adobe se haya eliminado en la [!UICONTROL Application] pestaña . Una vez eliminada, actualice la página y repita el proceso.

   ![Auditoría [!DNL Analytics for Advertising] Código JavaScript en [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising]](overview.md)
>* [Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]](prerequisites.md)

