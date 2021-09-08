---
title: Requisitos previos e información clave para implementar [!DNL Analytics for Advertising Cloud]
description: Requisitos previos e información clave para implementar [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Requisitos previos e información clave para implementar [!DNL Analytics for Advertising Cloud]

*Anunciantes con Advertising Cloud DSP y Advertising Cloud Search*

Revise la siguiente información antes de integrar Advertising Cloud con Adobe Analytics.

## Requisitos para la creación de informes de datos de Advertising Cloud en [!DNL Analytics]

* Servicio de identidad de Experience Cloud: `visitorAPI.js` versión 2.0 o superior
* Cualquier versión de Adobe Analytics (incluidas [!DNL Prime], [!DNL Premium] o [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versión 2.1 o superior

>[!TIP]
>
>Para mejorar la fidelidad de los datos, utilice la versión más reciente del servicio de identidad de Experience Cloud con compatibilidad con CNAME, así como la versión más reciente de AppMeasurement para JavaScript de Analytics.

## Requisitos para compartir segmentos de Analytics con Advertising Cloud

* Servicio de identidad de Experience Cloud: `visitorAPI.js` versión 2.1 o superior
* Adobe Analytics: `!DNL appMeasurement.js` versión 1.8 o superior

## Requisitos para la creación de informes de datos [!DNL Analytics] en Advertising Cloud

Proporcione al equipo de implementación de Advertising Cloud lo siguiente:

* El ID del grupo de informes [!DNL Analytics] que se utilizará para generar informes sobre la actividad de medios de pago y para alimentar la actividad del sitio para la optimización y la creación de informes en Advertising Cloud
* El ID de organización de Experience Cloud de la empresa (ID de organización).

Puede encontrar ambos ID en la pantalla [Resumen de Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html).

![Pantalla Resumen del Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Datos en Advertising Cloud {#lookback-a4adc}

Dado que los datos [!DNL Analytics] se envían a Advertising Cloud para su creación de informes y optimización, están sujetos a las reglas de atribución, incluidas las ventanas retrospectivas de clics e impresiones, que están configuradas para el anunciante en Advertising Cloud.

![configuración de la ventana retrospectiva a nivel del anunciante en Advertising Cloud](/help/integrations/assets/a4adc-lookbacks.png)

* Ventana retrospectiva de clic en atribución de Advertising Cloud: Número de días después de que se produzca el primer clic en el que el clic puede atribuirse a una conversión. De forma predeterminada, este valor es de 60 días; el máximo es de 90 días
* Ventana retrospectiva de impresión de atribución de Advertising Cloud: Número de días después de que se produzca una impresión publicitaria en la que la impresión se pueda atribuir a una conversión. De forma predeterminada, este valor es de 14 días; el máximo es de 30 días

   >[!NOTE]
   >
   > La ventana de retrospectiva de impresión es específica para los informes de Advertising Cloud, no de [!DNL Analytics for Advertising Cloud].

El JavaScript [!DNL Analytics for Advertising Cloud] utiliza esta configuración para determinar hasta dónde se debe considerar válida una entrada de visualización o una entrada de pulsación en el sitio. Para obtener más información sobre cómo se determinan las visualizaciones y las pulsaciones, consulte &quot;[Advertising Cloud ID used by Analytics](ids.md)&quot;.

## Datos de Advertising Cloud en [!DNL Analytics]

[!DNL Analytics] establece los Advertising Cloud ID (AMO ID) dentro de la visita de Analytics, sujetos a la configuración de persistencia del eVar del anunciante, que se aplica tanto a las pulsaciones como a las visualizaciones. La configuración de persistencia se configura en el back-end de Advertising Cloud y el administrador de cuentas de Adobe puede cambiarla.

* [!DNL Analytics for Advertising Cloud] Caducidad del eVar: 60 días de forma predeterminada para los AMO ID

>[!NOTE]
>
>Para segmentar datos para un intervalo de tiempo diferente, puede [configurar segmentos personalizados](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) con diferentes ventanas retroactivas dentro de Analysis Workspace.

## Entornos de publicidad compatibles

* Buscar
* Mostrar
* Vídeo
* Vídeo en línea
* Nativo

Póngase en contacto con el administrador de cuentas de Adobe para conocer los últimos entornos de publicidad admitidos en cada canal.

## Aspectos importantes antes de una implementación

* No se cobran costes adicionales por esta integración, ni las llamadas al servidor conllevan [!DNL Analytics] ni tarifas adicionales de Advertising Cloud.

* [!DNL Analytics for Advertising Cloud] no depende del servidor de publicidad: puede producirse una visualización o pulsación desde cualquier servidor de publicidad, y se generan los ID adecuados al entrar en el sitio.

* La integración solo pasa [!DNL Analytics] eventos estándar y personalizados a Advertising Cloud para la optimización de ofertas de los siguientes esfuerzos de publicidad y medios de pago. No pasa [!DNL Analytics] segmentos, métricas calculadas y eVars a Advertising Cloud para la optimización de la oferta.

* Advertising Cloud crea ID persistentes dentro de [!DNL Analytics] en función del último anuncio en el que se hizo clic o se vio antes de que el usuario entrara al sitio, en función de las [ventanas retroactivas de clics y visualizaciones](#lookback-a4adc) configuradas en Advertising Cloud. Si un visitante del sitio tuviera ambos tipos de interacciones de entrada al sitio dentro de su perfil y el clic se encontrara dentro del período retroactivo, entonces el ID de pulsación del visitante anularía el ID de visualización para los informes del sitio.

* [!DNL Analytics for Advertising Cloud] el seguimiento de conversión en Adobe Analytics utiliza una ventana retrospectiva de seguimiento configurable (de forma predeterminada, 60 días). Los informes de Advertising Cloud reflejan las conversiones y la participación del sitio hasta el final de esta ventana retrospectiva de seguimiento.

* Se admiten todos los tipos de anuncios. Sin embargo, no todos los entornos de publicidad son compatibles.

   Por ejemplo, los anuncios de TV conectada (CTV) no se rastrean porque no se producen clics en CTV y no se pueden producir conversiones en el mismo dispositivo. Sin embargo, si la publicidad se ve dentro de un entorno de escritorio, se pueden rastrear algunos datos de entrada al sitio de visualización.

* [!DNL Analytics] actualmente, se realiza un seguimiento de las conversiones, que se atribuyen únicamente a un visitante del mismo dispositivo.

* [!DNL Analytics for Advertising Cloud] no admite conversiones de visualizaciones en la aplicación.

* El seguimiento de visualizaciones no es compatible con los anunciantes que utilizan una implementación de reenvío del lado del servidor de [!DNL Analytics].

### ID suplementario

Una vez implementado el servicio de identidad de Experience Cloud para un sitio, las visitas que contienen datos de [!DNL Analytics] o Advertising Cloud contienen un ID suplementario.

Ejemplo: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Para una integración de datos precisa, todas las llamadas de Advertising Cloud utilizadas por una actividad [!DNL Analytics for Advertising Cloud] para ofrecer contenido o registrar la métrica de objetivos deben tener una visita [!DNL Analytics] correspondiente que comparta el mismo ID suplementario.

Cuando solucione problemas en [!DNL Analytics], asegúrese de que el ID suplementario esté presente para las visitas de [!DNL Analytics]. En [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html), puede ver este ID en la pestaña Advertising Cloud como el parámetro `sdid`.

>[!NOTE]
>
> Esta implementación funciona de forma similar a la integración [!DNL Analytics for Target] .

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Código JavaScript para Analytics for Advertising Cloud](/help/integrations/analytics/javascript.md)

