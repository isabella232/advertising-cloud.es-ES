---
title: Información general de [!DNL Analytics for Advertising Cloud]
description: Información general de [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---

# Información general de [!DNL Analytics for Advertising Cloud]

*Anunciantes con Advertising Cloud DSP y Advertising Cloud Search*

[!DNL Analytics for Advertising Cloud] integra Adobe Analytics y Adobe Advertising Cloud para ampliar y mejorar las capacidades de cada producto.

La integración permite a los anunciantes realizar un seguimiento de las interacciones de clics y visualizaciones del sitio en sus [!DNL Analytics] instancias, lo que permite a las marcas ver cómo su gasto en publicidad conduce a la participación del sitio y a objetivos empresariales críticos.

Además, Advertising Cloud puede acceder a los vastos datos de origen que [!DNL Analytics] recopila mediante etiquetas [!DNL Analytics] que ya están en el sitio. Esto permite una administración de recorridos más sólida, remarketing de origen e informes de sitio de medios de pago. Advertising Cloud puede utilizar aún más los datos [!DNL Analytics] para optimizar los gastos y las ofertas.

Cuando se utiliza correctamente, [!DNL Analytics for Advertising Cloud] borra las líneas entre dos funciones tradicionales: administración de recorridos publicitarios (el acto de enviar usuarios al sitio a través de anuncios) y comprender esa participación en el sitio a través del análisis web.

Beneficios principales:

* Envíe [!DNL Analytics] segmentos directamente a Advertising Cloud para el remarketing de sitio de origen.
* Utilice [!DNL Analytics] eventos personalizados y estándar como señales de conversión para optimizar la publicidad de medios de pago.
* Aproveche Analysis Workspace [!DNL Analytics] para comprender mejor los puntos de entrada al sitio y el comportamiento de las visitas.
* Permita una colaboración más estrecha entre analistas web y equipos de medios de pago.
* Utilice ID de pulsaciones y visualizaciones persistentes de Advertising Cloud en [!DNL Analytics] para comprender la participación en el sitio.
* Mejore los informes de medios de pago tradicionales en Analysis Workspace con métricas personalizadas, dimensiones personalizadas y actividad del sitio que no se pueden lograr al exportar datos o píxeles a servidores de publicidad u otros DSP.
* Aproveche el código [!DNL Analytics] que ya se encuentra en su sitio web para realizar el seguimiento y la optimización dentro de Advertising Cloud.

>[!TIP]
>
> Vea un [vídeo introductorio a [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Uso de Analytics para informes de medios pagados

[!DNL Analytics for Advertising Cloud] mejora los informes y la perspectiva sobre cómo la publicidad impulsa el comportamiento del sitio al permitirle:

* Utilice ID de pulsaciones y visualizaciones persistentes de Advertising Cloud en [!DNL Analytics] para comprender la participación en el sitio.
* Aproveche Analysis Workspace para comprender mejor los puntos de entrada al sitio y el comportamiento de las visitas. Puede acceder a los datos dimensionales y de evento de medios de pago, que incluyen los nombres de entidad de Advertising Cloud Campaign (hasta las ubicaciones y publicidades) y sus métricas asociadas, como clics, impresiones y costes.

Para utilizar [!DNL Analytics] como herramienta de informes de medios de pago, su organización necesita un inicio de sesión de Experience Cloud con acceso a Analysis Workspace. Su equipo de Advertising Cloud le ayudará a asignar los datos de Advertising Cloud a grupos de informes individuales en Analysis Workspace. Puede enviar datos de Advertising Cloud a cualquier grupo de informes, pero debe tener en cuenta los grupos de informes que se han asignado a Advertising Cloud y los que no lo han hecho. En función del grupo de informes, esto puede cambiar los datos notificados.

[Los ID de Advertising Cloud  [!DNL Analytics]](ids.md) en funcionan como otras eVars, con una caducidad personalizada y persistente. De forma predeterminada, la ventana de retrospectiva de atribución se establece en 60 días durante la implementación de Advertising Cloud. Para cambiar esta configuración, trabaje con el administrador de cuentas de Adobe.

Las dimensiones de Advertising Cloud se agregan con el sufijo &quot;(AMO ID)&quot; (como &quot;Tipo de anuncio (AMO ID)&quot;). Consulte &quot;[Métricas de Advertising Cloud en Analysis Workspace](advertising-cloud-metrics-in-analytics.md)&quot; para obtener una lista de las dimensiones disponibles.

>[!NOTE]
>
> Cuando vea datos de Advertising Cloud (o cualquier conjunto de datos) dentro de [!DNL Analytics], tenga en cuenta que las métricas y los informes se basan en reglas que se establecen dentro de [!DNL Analytics]. Los datos podrían ser diferentes a los que se ven en otros sistemas de informes, como los informes de servidores de publicidad, los informes [!DNL DSP] o los informes de motores de búsqueda. Para comprender las diferencias de datos en [!DNL Analytics], debe saber cuándo caducan los datos del eVar, qué define una visita, qué se considera atribución de último contacto frente a atribución total persistente y otros factores. Para obtener más información, consulte [Variaciones de datos previstas entre [!DNL Analytics] y Advertising Cloud](data-variances.md).

## Uso de Analytics para potenciar campañas y Portfolio de Advertising Cloud

Sin requerir píxeles adicionales, [!DNL Analytics for Advertising Cloud] permite una mejor optimización y segmentación de audiencia mediante el envío de dos señales principales a Advertising Cloud:

* Métricas de conversión que se utilizarán como señales de oferta:
   * métricas estándar, como [!UICONTROL Revenue] y [!UICONTROL Cart Views].
   * métricas de participación en el sitio, como vistas de página y métricas de visitas.
   * métricas de ingresos personalizadas.
   * métricas de ingresos reservadas.
* Segmentos creados en [!DNL Analytics] y publicados para el Experience Cloud.

   Puede utilizar segmentos [!DNL Analytics] para redireccionar sitios de origen en [!DNL DSP] y anuncios de búsqueda paga.

   (Solo Advertising Cloud Search) Los anunciantes con [!DNL Analytics] pero no los Audience Manager también pueden crear audiencias basadas en etiquetas de sitios web de Google (listas de remarketing) y audiencias de coincidencia de clientes (listas de clientes) a partir de segmentos [!DNL Analytics] que se comparten con los Experience Cloud.

### Métricas de conversión de sitio como señales de oferta

Puede usar los eventos estándar y los eventos personalizados de [!DNL Analytics] para crear objetivos ponderados en Advertising Cloud. Los objetivos informan las decisiones de oferta para los paquetes [!DNL DSP] y los portafolios de búsqueda.

>[!NOTE]
>
> No puede asignar métricas calculadas de [!DNL Analytics] a Advertising Cloud.

Su equipo de Advertising Cloud le ayudará a identificar y asignar los eventos aplicables al rendimiento de medios de pago en Advertising Cloud, donde aparecerán en [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Consulte &quot;[Métricas de Analytics en Advertising Cloud](analytics-data-in-advertising-cloud.md)&quot; para obtener una lista de las métricas disponibles.

### Segmentos de Analytics para redireccionamiento de sitios

Advertising Cloud puede introducir [!DNL Analytics] segmentos con fines de remarketing para Advertising Cloud DSP y [!DNL Search] anuncios mediante la integración de audiencias de Experience Cloud nativa entre [!DNL Analytics] y el Experience Cloud.

Para acceder a los segmentos [!DNL Analytics], una cuenta de anunciante debe tener habilitado el [Servicio de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html). Cuando el servicio de ID está habilitado, todos los segmentos del Experience Cloud (incluidos los segmentos creados en [!DNL Analytics] y publicados para el Experience Cloud, los segmentos creados en Adobe Audience Manager, los segmentos creados en el Experience Cloud mediante [!DNL People core service] y los segmentos creados en Adobe Experience Platform y enviados a Advertising Cloud mediante el Audience Manager) quedan disponibles en Advertising Cloud en cuanto se procesan.

[!DNL Analytics] Los segmentos de están disponibles en un plazo de 24 horas y se actualizan diariamente.

Para obtener más información sobre el servicio Audiencias de Experience Cloud, consulte [Audiencias de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Ejemplos de cómo utilizar la integración

### Uso de datos de Advertising Cloud en Analysis Workspace

Para aprender a utilizar los datos de Advertising Cloud para crear informes visuales en Analysis Workspace, consulte el vídeo &quot;[Introducción a Workspace y a los informes](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)&quot;.

### Creación de tableros de Advertising Cloud

Para obtener información sobre cómo realizar un seguimiento de los datos de Advertising Cloud en relación con sus objetivos en Analysis Workspace, consulte el vídeo &quot;[Creación de paneles de Advertising Cloud con Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html)&quot;.

### Uso del Advertising Cloud ID para el análisis de entrada al sitio

Para ver cómo se puede crear un informe de entrada al sitio de Advertising Cloud para supervisar las influencias de día de la semana, hora del día, explorador y ubicación geográfica, consulte el vídeo &quot;[Creación de informes de entrada al sitio de Advertising Cloud](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;.

>[!MORELIKETHIS]
>
>* [Vídeo: Introducción a [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Advertising Cloud ID utilizados por Analytics](ids.md)
>* [Código JavaScript para Analytics for Advertising Cloud](/help/integrations/analytics/javascript.md)
>* [Variaciones de datos previstas  [!DNL Analytics] entre Advertising Cloud y](data-variances.md)
>* [Métricas de Advertising Cloud en Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Datos en Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

