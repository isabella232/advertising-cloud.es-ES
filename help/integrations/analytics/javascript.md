---
title: Código JavaScript para [!DNL Analytics for Advertising Cloud]
description: Código JavaScript para [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# Código JavaScript para [!DNL Analytics for Advertising Cloud]

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

*Anunciantes solo con Advertising Cloud DSP*

Para Advertising Cloud DSP, la integración [!DNL Analytics for Advertising Cloud] rastrea las interacciones del sitio de pulsaciones y visualizaciones. Las visitas de pulsaciones se rastrean mediante el código estándar de Adobe Analytics en sus páginas web; el código [!DNL Analytics] captura los parámetros de AMO ID e EF ID en la dirección URL de la página de aterrizaje y los rastrea en sus eVars reservadas respectivas. Puede realizar un seguimiento de las visitas mediante la implementación de dos líneas de código JavaScript en las páginas web.

En la primera vista de página de una visita al sitio, el código JavaScript de Advertising Cloud comprueba si el visitante ha visto o hecho clic previamente en un anuncio. Si el usuario ha entrado previamente al sitio mediante un clic o no ha visto una publicidad, se ignora al visitante. Si el visitante ha visto un anuncio y no ha entrado en el sitio mediante un clic durante el [click lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc) establecido en Advertising Cloud, el código JavaScript de Advertising Cloud utiliza el [servicio de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) para generar un ID suplementario (`SDID`), que se utiliza para unir datos de Advertising Cloud a la visita de Adobe Analytics del visitante. A continuación, Adobe Analytics consulta a Advertising Cloud el ID de AMO y el ID de EF asociados a la exposición del anuncio. A continuación, el AMO ID y los EF ID se rellenan en sus eVars respectivas. Estos valores persisten durante un período designado (de forma predeterminada, 60 días).

[!DNL Analytics] envía métricas de tráfico del sitio (como vistas de página, visitas y tiempo empleado) y cualquier evento  [!DNL Analytics]  personalizado o estándar a Advertising Cloud por hora, utilizando el EF ID como clave. Estas métricas [!DNL Analytics] se ejecutan a través del sistema de atribución de Advertising Cloud para conectar las conversiones al historial de clics y exposiciones.

>[!NOTE]
>
>La lógica de seguimiento JavaScript de Advertising Cloud se produce en el Adobe y, por lo tanto, prácticamente no afecta al tiempo de carga de la página.
>
>Por el contrario, la lógica del conector de datos [!DNL DCM] a [!DNL Analytics] (que utiliza [!DNL Google Campaign Manager 360]) para Advertising Cloud DSP se produce en el lado del cliente. La vinculación del lado del cliente ralentiza la carga de la página y aumenta el riesgo de pérdida de datos. Esto ocurre porque el JavaScript [!DNL Analytics] debe hacer ping [!DNL DoubleClick] y esperar a que [!DNL DoubleClick] devuelva los datos de último clic/impresión a [!DNL Analytics]. Cuando su equipo [!DNL DSP] configura el conector de datos [!DNL DCM], debe especificar cuánto tiempo está dispuesto a retrasar la página.

## Implementación del código JavaScript

La biblioteca JavaScript consta de dos líneas que permiten a [!DNL Analytics] y a Advertising Cloud comunicarse entre sí. Si la integración [!DNL Analytics for Advertising Cloud] se completó durante la implementación de Advertising Cloud, debería haber recibido este código con instrucciones sobre cómo implementarlo.

Si aún no dispone del código, póngase en contacto con el equipo de asistencia de Advertising Cloud.

### Dónde colocar el código

La función [!DNL Analytics for Advertising Cloud] de JavaScript debe situarse después del servicio de ID de Experience Cloud, pero antes del código de medición de aplicaciones de Analytics, de modo que el ID suplementario (`SDID`) se pueda incluir en la llamada de Analytics.

![Colocación del código](/help/integrations/assets/a4adc-code-placement.png)

### Validación de la implementación de código

Puede realizar la validación utilizando cualquier tipo de herramienta de detector de paquetes (como [!DNL Charles], [!DNL Fiddler] o [!DNL Chrome Developer Tools]) comparando los valores de los cuatro ID entre la solicitud que va a Advertising Cloud y la solicitud que va a [!DNL Analytics], como se describe a continuación.

#### Confirmar el código con [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Abra [!DNL Chrome Developer Tools] y haga clic en la pestaña **Network**.
1. Cargue una página de sitio web que contenga el JavaScript [!DNL Analytics for Advertising Cloud].
1. Filtre la pestaña [!UICONTROL Network] por `last` y revise dos filas:

   ![Filtrado por última vez](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * La primera fila es la llamada a la biblioteca JavaScript y se titula `last-event-tag-latest.min.js`.
   * La segunda fila es la llamada que envía la solicitud a Advertising Cloud. Comienza de la siguiente manera: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Si no ve la llamada a Advertising Cloud, es posible que no sea la primera vista de página de la visita. Con fines de prueba, puede eliminar la cookie para que la siguiente llamada sea la primera vista de página de la visita correspondiente:

      1. En la ficha Aplicación, busque la cookie `adcloud` y verifique que la cookie contenga `_les_v` (última visita) con un valor de `y` y una marca de tiempo UTC epoch que caduque en 30 minutos.
      1. Elimine la cookie `ad cloud` y actualice la página.
1. Filtre en `/b/ss` para ver la visita de Analytics.

   ![Filtrado en  `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. Compare los valores de ID entre las dos visitas. Todos los valores se expresarán en parámetros de cadena de consulta, excepto el ID del grupo de informes de la visita de Analytics, que es la ruta de URL inmediatamente después de `/b/ss/`.

   | ID | Parámetro de Analytics | Parámetro Advertising Cloud |
   |--- |--- |--- |
   | Organización IMS del Experience Cloud | `mcorgid` | `_les_imsOrgid` |
   | ID de datos suplementario | sdid | `_les_sdid` |
   | Grupo de informes de Analytics | El valor después de `/b/ss/` | `_les_rsid` |
   | ID de visitante de Experience Cloud | mid | `_les_mid` |

   Si los valores de ID coinciden, se confirma la implementación de JavaScript. Advertising Cloud enviará al servidor [!DNL Analytics] cualquier detalle de seguimiento de pulsaciones o visualizaciones si existe.

#### Confirmar el código con [!DNL Adobe Experience Cloud Debugger]

1. Abra [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) en la página principal.
1. Vaya a la pestaña [!UICONTROL Network].
1. En la barra de herramientas [!UICONTROL Solutions Filter], haga clic en [!UICONTROL Advertising Cloud] y [!UICONTROL Analytics].
1. En la fila del parámetro [!UICONTROL Request URL – Hostname], busque `lasteventf-tm.everesttech.net`.
1. En la fila [!UICONTROL Request – Parameters*], audite las señales generadas, de forma similar al paso 3 en &quot;[Confirmar el código con [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;.
   * Compruebe que el parámetro `SDID` coincide con el `Supplemental Data ID` del filtro de Adobe Analytics.
   * Si el código no está generando, compruebe que la cookie de Advertising Cloud se haya eliminado en la pestaña [!UICONTROL Application] . Una vez eliminada, actualice la página y repita el proceso.

   ![Auditoría del código  [!DNL Analytics for Advertising Cloud] JavaScript en  [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising Cloud]](prerequisites.md)

