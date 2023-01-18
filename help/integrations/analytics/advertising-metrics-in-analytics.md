---
title: Métricas de publicidad de Adobe en Analysis Workspace
description: Métricas de publicidad de Adobe en Analysis Workspace
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Métricas de publicidad de Adobe en Analysis Workspace

*Anunciantes con Adobe de solo integración de Advertising-Adobe Analytics*

>[!NOTE]
>
>* La publicidad de Adobe pasa métricas y dimensiones de tráfico a [!DNL Analytics] diariamente.
>* [!DNL Analytics] captura las pulsaciones y visualizaciones de publicidad de Adobe en tiempo real.


## Métricas de tráfico de la publicidad de Adobe

>[!NOTE]
>
>Todas las métricas de tráfico publicitario de Adobe de [!DNL Analytics] comience con &quot;AMO&quot;.

| Métrica de tráfico | Descripción |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Número de impresiones de publicidad de Adobe. |
| [!UICONTROL AMO Clicks] | El número total de clics en publicidad de Adobe. |
| [!UICONTROL AMO Cost] | El gasto publicitario de Adobe en la divisa del grupo de informes. |
| [!UICONTROL AMO ID Instance] | Número de veces que se establece el ID de publicidad de Adobe. |
| [!UICONTROL AMO Minutes Viewed] | El número de minutos que se vio un vídeo de Adobe Advertising. |
| [!UICONTROL AMO Views] | Número de vistas de un anuncio. Se cuenta una vista cuando el espectador inicia el vídeo Publicidad de Adobe. |
| [!UICONTROL AMO Views 25% Complete] | Número de vistas para las que se ha visto al menos el 25 % de un vídeo publicitario de Adobe. |
| [!UICONTROL AMO Views 50% Complete] | Número de vistas para las que se ha visto al menos el 50 % de un vídeo publicitario de Adobe. |
| [!UICONTROL AMO Views 75% Complete] | Número de vistas para las que se ha visto al menos el 75 % de un vídeo publicitario de Adobe. |
| [!UICONTROL AMO Views 100% Complete] | Número de vistas para las que se ha visto el 100 % de un vídeo publicitario de Adobe. |
| [!UICONTROL AMO Viewable Impressions] | Número de impresiones que se midieron para que se puedan ver según la configuración de ubicación. |
| [!UICONTROL AMO Not Viewable Impressions] | Número de impresiones que se determinó que no eran visibles. Este valor se calcula como ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | El número de impresiones que se han servido para las que la instrumentación de capacidad de visualización se inicializó correctamente. Este valor se calcula como (impresiones instrumentadas: el número de impresiones no medibles). |

## Métricas calculadas personalizadas útiles para la publicidad de Adobe

Considere la posibilidad de crear las métricas siguientes para sus datos de publicidad de Adobe.

* Clics hasta la instancia de página de aterrizaje ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Es el porcentaje de personas que hicieron clic en la publicidad y llegaron a la página de aterrizaje.
* Tasa de medición ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Tasa de impresión visible ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Costo por vista ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Costo por clic ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Dimension publicitarios de Adobe

>[!NOTE]
>
>Todas las dimensiones de publicidad de Adobe en [!DNL Analytics] van seguidos de &quot;(AMO ID)&quot;.

| Dimension | Datos de publicidad de Adobe aplicables | Descripción |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] y [!DNL Search] data | DSP publicitario o el nombre del motor de búsqueda |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] y [!DNL Search] data | El nombre de la cuenta. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] y [!DNL Search] data | RTB ([!DNL DSP]) o el nombre de red de la publicidad ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] y [!DNL Search] data | El nombre de la campaña. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] y [!DNL Search] data | El paquete ([!DNL DSP]) o portafolio ([!DNL Search]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | El nombre de la ubicación. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] data | El nombre del grupo de anuncios. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] data | La palabra clave. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] data | El tipo de coincidencia de búsqueda. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] data | La palabra clave y el tipo de coincidencia. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] y [!DNL Search] data | El tipo de anuncio, como `text`, `video`, `display`o `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] y [!DNL Search] data | El tipo de anuncio ([!DNL DSP]) o título de la publicidad ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] y [!DNL Search] data | La descripción de la publicidad ([!DNL DSP]) o cuerpo del anuncio ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] data | Dirección URL mostrada en la publicidad. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] data | La dirección URL de destino de la publicidad. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] y [!DNL Search] data | Indica si la entrada de página de aterrizaje fue una visualización o una pulsación. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] data | Destino del producto para una publicidad de lista de productos. |

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Datos en publicidad de Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)

