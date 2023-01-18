---
title: Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]
description: Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]

*Anunciantes con DSP publicitarias y[!DNL Advertising Search]*

Revise la siguiente información antes de integrar Publicidad de Adobe con Adobe Analytics.

## Requisitos para la creación de informes de datos publicitarios de Adobe en [!DNL Analytics]

* Cualquiera de los siguientes:
   * SDK web de Adobe Experience Platform: `alloy.js`
   * Servicio de identidad de Experience Cloud: `visitorAPI.js` versión 2.0 o superior
* Cualquier versión de Adobe Analytics (incluida [!DNL Prime], [!DNL Premium]o [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versión 2.1 o superior

>[!TIP]
>
>Para mejorar la fidelidad de los datos, utilice la versión más reciente de cada biblioteca.

## Requisitos para compartir segmentos de Analytics con publicidad de Adobe

* Servicio de identidad de Experience Cloud: `visitorAPI.js` versión 2.1 o superior
* Adobe Analytics: `!DNL appMeasurement.js` versión 1.8 o superior

## Requisitos para la creación de informes [!DNL Analytics] Datos en publicidad de Adobe

Proporcione al equipo de implementación de publicidad de Adobe lo siguiente:

* La variable [!DNL Analytics] ID del grupo de informes que se utilizará para informar sobre la actividad de medios de pago y para alimentar la actividad del sitio para la optimización y la creación de informes en la Publicidad de Adobe
* El ID de organización de Experience Cloud de la empresa (ID de organización).

Puede encontrar ambos ID en el [Pestaña Resumen de Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Pantalla Resumen del Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Datos en publicidad de Adobe {#lookback-a4adc}

Porque [!DNL Analytics] los datos se envían a Adobe Advertising para su creación de informes y optimización, los datos están sujetos a las reglas de atribución, incluidas las ventanas de retrospectiva de clics e impresiones, que están configuradas para el anunciante en Adobe Advertising.

![configuración de la ventana retrospectiva a nivel del anunciante en Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Atribución de publicidad Haga clic en la ventana retrospectiva: Número de días después de que se produzca el primer clic en el que el clic puede atribuirse a una conversión. De forma predeterminada, este valor es de 60 días; el máximo es de 90 días
* Ventana retrospectiva de atribución de Adobe Advertising: Número de días después de que se produzca una impresión publicitaria en la que la impresión se pueda atribuir a una conversión. De forma predeterminada, este valor es de 14 días; el máximo es de 30 días

   >[!NOTE]
   >
   > La ventana de retrospectiva de impresión es específica para la Publicidad de Adobe, no para [!DNL Analytics for Advertising], informes.

La variable [!DNL Analytics for Advertising] JavaScript utiliza esta configuración para determinar hasta dónde se debe considerar válida una entrada de visualización o de pulsación en el sitio. Para obtener más información sobre cómo se determinan las visualizaciones y las pulsaciones, consulte &quot;[ID de publicidad de Adobe utilizados por Analytics](ids.md).&quot;

## Adobe de datos publicitarios en [!DNL Analytics]

[!DNL Analytics] establece los ID de publicidad de Adobe (AMO ID) dentro de la visita de Analytics, sujetos a la configuración de persistencia del eVar del anunciante, que se aplica tanto a pulsaciones como a visualizaciones. La configuración de persistencia se configura en el back-end de la publicidad de Adobe y en su [!DNL Adobe] el equipo de la cuenta puede cambiarlo.

* [!DNL Analytics for Advertising] Caducidad del eVar: 60 días de forma predeterminada para los AMO ID

>[!NOTE]
>
>Para segmentar datos para un intervalo de tiempo diferente, puede [configurar segmentos personalizados](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) con diferentes ventanas retroactivas dentro de Analysis Workspace.

## Entornos de publicidad compatibles

* Buscar
* Mostrar
* Vídeo
* Vídeo en línea
* Nativo

Póngase en contacto con su [!DNL Adobe] equipo de cuenta para conocer los últimos entornos de publicidad admitidos en cada canal.

## Aspectos importantes antes de una implementación

* El equipo de implementación de Adobe Advertising configurará la integración.

* No se cobran costes adicionales por esta integración ni las llamadas al servidor resultan en [!DNL Analytics] o tarifas de publicidad de Adobe.

* [!DNL Analytics for Advertising] no depende del servidor de publicidad: puede producirse una visualización o pulsación desde cualquier servidor de publicidad, y se generan los ID adecuados al entrar en el sitio.

* La integración solo pasa [!DNL Analytics] eventos estándar y personalizados para publicidad de Adobe para la optimización de ofertas de los siguientes esfuerzos de publicidad y medios de pago. No pasa [!DNL Analytics] segmentos, métricas calculadas y eVars a Adobe Publicidad para la optimización de ofertas.

* La publicidad de Adobe crea ID persistentes dentro de [!DNL Analytics] en función del último anuncio en el que se hizo clic o se vio antes de que el usuario entrara al sitio, según la variable [ventanas retrospectivas de clics y visualizaciones](#lookback-a4adc) configurado en Adobe Advertising. Si un visitante del sitio tuviera ambos tipos de interacciones de entrada al sitio dentro de su perfil y el clic se encontrara dentro del período retroactivo, entonces el ID de pulsación del visitante anularía el ID de visualización para los informes del sitio.

* [!DNL Analytics for Advertising] el seguimiento de conversión en Adobe Analytics utiliza una ventana retrospectiva de seguimiento configurable (de forma predeterminada, 60 días). Los informes de publicidad de Adobe reflejan las conversiones y la participación del sitio hasta el final de esta ventana retrospectiva de seguimiento.

* Se admiten todos los tipos de anuncios. Sin embargo, no todos los entornos de publicidad son compatibles.

   Por ejemplo, los anuncios de TV conectada (CTV) no se rastrean porque no se producen clics en CTV y no se pueden producir conversiones en el mismo dispositivo. Sin embargo, si la publicidad se ve dentro de un entorno de escritorio, se pueden rastrear algunos datos de entrada al sitio de visualización.

* [!DNL Analytics] actualmente, se realiza un seguimiento de las conversiones, que se atribuyen únicamente a un visitante del mismo dispositivo.

* [!DNL Analytics for Advertising] no admite conversiones de visualizaciones en la aplicación.

* El seguimiento de visualizaciones no es compatible con los anunciantes que utilizan una implementación de reenvío del lado del servidor de [!DNL Analytics].

### ID suplementario

Una vez implementado el servicio de identidad de Experience Cloud para un sitio, las visitas que contienen datos de [!DNL Analytics] o la publicidad de Adobe contienen un ID suplementario.

Ejemplo: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Para una integración de datos precisa, todas las llamadas de publicidad de Adobe que usa un [!DNL Analytics for Advertising] actividad para entregar contenido o registrar la métrica de objetivo debe tener una [!DNL Analytics] visita que comparte el mismo ID suplementario.

Cuando esté solucionando problemas en [!DNL Analytics], asegúrese de que el ID suplementario esté presente para [!DNL Analytics] visitas individuales. En el [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), puede ver este ID en la pestaña Publicidad de Adobe como el `sdid` parámetro.

>[!NOTE]
>
> Esta implementación funciona de manera similar a la [!DNL Analytics for Target] integración.

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising]](overview.md)
>* [Código JavaScript para Analytics for Advertising](/help/integrations/analytics/javascript.md)

