---
title: Información general sobre el envío de datos de exposición DSP medios a Adobe Audience Manager
description: Aprenda a utilizar píxeles de evento de Audience Manager para capturar datos de nivel de impresión y de clics de campañas de Advertising Cloud DSP
feature: Integration with Adobe Audience Manager
source-git-commit: e861fc53ba14d783c763b291cdc618e5f1d4124f
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Información general sobre el envío de datos de exposición DSP medios a Adobe Audience Manager

*Anunciantes solo con Advertising Cloud DSP*

*Anunciantes con solo integración Advertising Cloud-Adobe Audience Manager*

Los clientes de Advertising Cloud DSP con Adobe Audience Manager pueden usar píxeles de evento de Audience Manager para capturar datos de nivel de impresión y datos de nivel de clic de DSP campañas. Los píxeles de evento envían los datos como señales procesables al Audience Manager. Estas señales habilitan varios casos de uso DSP, como segmentación más avanzada, administración de frecuencias, análisis de marketing y perspectivas de informes.

DSP no le carga que envíe estas señales al Audience Manager. Sin embargo, usted paga los costos de ingesta estándar de los Audience Manager en función de las llamadas al servidor, según su contrato de Audience Manager. Audience Manager elimina los eventos duplicados que se rastrean de dos formas diferentes, de modo que cada evento se carga solo una vez.

>[!NOTE]
>
> Audience Manager también admite la captura de datos de archivos de registro del servidor de publicidad, lo que proporciona menos flexibilidad. Ese proceso no se trata en esta documentación.

## Beneficios principales

* DSP datos de campaña fluyen a Audience Manager en tiempo real y puede utilizarlos para crear rasgos basados en reglas que utiliza para definir segmentos.

* Los segmentos están disponibles para la segmentación inmediatamente después de la clasificación de rasgos y segmentos del usuario, lo que refuerza los esfuerzos de segmentación en tiempo real.

* Puede aprovechar los datos de campaña para casos de uso como el límite de frecuencia en los elementos creativos, el redireccionamiento de los usuarios expuestos a campañas anteriores y el análisis del comportamiento y los puntos de entrada del sitio descendentes.

* Los datos agregados proporcionan una vista unificada del rendimiento de la campaña, ayudan a identificar rutas de conversión personalizadas y pueden utilizarse para mejorar la secuencia de eventos que generan conversiones a través del Audience Manager [!DNL Audience Optimization Reports] o a través de un [[!DNL Audience Analytics] integración con Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Cómo se realiza el seguimiento de los datos

Los píxeles del evento de clics e impresiones del Audience Manager se basan en cookies. Los píxeles no capturan eventos que se producen en entornos sin cookies, como aplicaciones móviles y TV conectada (CTV).

### Píxeles de seguimiento de impresión

El Audience Manager rastrea los datos de impresión de una publicidad cuando se adjunta un píxel de seguimiento de eventos transparentes de 1xl-pixel al anuncio. El píxel del evento se carga cada vez que el usuario recibe el anuncio y lo carga el explorador web. El píxel se carga desde un subdominio específico del cliente de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), que es un dominio heredado para Audience Manager, y contiene parámetros como pares clave-valor. La llamada de evento recopila datos de impresión y conversión y los envía a los servidores de recopilación de datos del Audience Manager.

### Píxeles de rastreo de clics

El Audience Manager rastrea los clics de manera similar a las impresiones, excepto que no carga el píxel del evento transparente cada vez que se presenta el anuncio. En su lugar, los datos de clics se rastrean en la dirección URL de pulsaciones de la publicidad. El anuncio apunta a un subdominio específico del cliente de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), que es un dominio heredado para Audience Manager, para que los servidores de recopilación de datos del Audience Manager lo procesen. A continuación, el servidor redirige al usuario a la página de aterrizaje deseada. La dirección URL contiene parámetros como pares clave-valor.

>[!NOTE]
>
>Si su organización utiliza [!DNL Analytics] , es posible que no necesite el rastreo de clics del Audience Manager. Adobe Analytics captura las señales de clic y las puede enviar al Audience Manager a través de [reenvío del lado del servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Recopilación de datos de clics e impresiones de campañas de Advertising Cloud DSP](collect.md)
>* [Casos de uso](use-cases.md)

