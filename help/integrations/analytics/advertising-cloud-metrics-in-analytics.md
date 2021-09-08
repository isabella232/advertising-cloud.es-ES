---
title: Métricas de Advertising Cloud en Analysis Workspace
description: Métricas de Advertising Cloud en Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Métricas de Advertising Cloud en Analysis Workspace

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

>[!NOTE]
>
>* Advertising Cloud pasa métricas de tráfico y dimensiones a [!DNL Analytics] diariamente.
>* [!DNL Analytics] captura las pulsaciones y visualizaciones de Advertising Cloud en tiempo real.


## Métricas de tráfico de Advertising Cloud

>[!NOTE]
>
>Todas las métricas de tráfico de Advertising Cloud en [!DNL Analytics] empiezan por &quot;AMO&quot;.

| Métrica de tráfico | Descripción |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Número de impresiones de Advertising Cloud. |
| [!UICONTROL AMO Clicks] | El número total de clics de Advertising Cloud. |
| [!UICONTROL AMO Cost] | El gasto de Advertising Cloud en la moneda del grupo de informes. |
| [!UICONTROL AMO ID Instance] | Número de veces que se establece el Advertising Cloud ID. |
| [!UICONTROL AMO Minutes Viewed] | El número de minutos que se vio un vídeo de Advertising Cloud. |
| [!UICONTROL AMO Views] | Número de vistas de un anuncio. Se cuenta una vista cuando el espectador inicia el vídeo de Advertising Cloud. |
| [!UICONTROL AMO Views 25% Complete] | Número de vistas para las que se ha visto al menos el 25 % de un vídeo de Advertising Cloud. |
| [!UICONTROL AMO Views 50% Complete] | Número de vistas para las que se ha visto al menos el 50 % de un vídeo de Advertising Cloud. |
| [!UICONTROL AMO Views 75% Complete] | Número de vistas para las que se ha visto al menos el 75 % de un vídeo de Advertising Cloud. |
| [!UICONTROL AMO Views 100% Complete] | Número de vistas para las que se ha visto el 100 % de un vídeo de Advertising Cloud. |
| [!UICONTROL AMO Viewable Impressions] | Número de impresiones que se midieron para que se puedan ver según la configuración de ubicación. |
| [!UICONTROL AMO Not Viewable Impressions] | Número de impresiones que se determinó que no eran visibles. Este valor se calcula como ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | El número de impresiones que se han servido para las que la instrumentación de capacidad de visualización se inicializó correctamente. Este valor se calcula como (impresiones instrumentadas: el número de impresiones no medibles). |

## Métricas calculadas personalizadas útiles para Advertising Cloud

Considere la posibilidad de crear las métricas siguientes para sus datos de Advertising Cloud.

* Clics en la instancia de la página de aterrizaje ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Es el porcentaje de personas que hicieron clic en la publicidad y llegaron a la página de aterrizaje.
* Tasa mensurable ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Tasa de impresión visible ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Costo por vista ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Costo por clic ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Dimension de Advertising Cloud

>[!NOTE]
>
>Todas las dimensiones de Advertising Cloud en [!DNL Analytics] van seguidas de &quot;(AMO ID)&quot;.

| Dimension | Datos de Advertising Cloud aplicables | Descripción |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] y  [!DNL Search] datos | Advertising Cloud DSP o el nombre del motor de búsqueda |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] y  [!DNL Search] datos | El nombre de la cuenta. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] y  [!DNL Search] datos | RTB ([!DNL DSP]) o el nombre de red de publicidad ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] y  [!DNL Search] datos | El nombre de la campaña. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] y  [!DNL Search] datos | El nombre del paquete ([!DNL DSP]) o portafolio ([!DNL Search]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | El nombre de la ubicación. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] data | El nombre del grupo de anuncios. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] data | La palabra clave. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] data | El tipo de coincidencia de búsqueda. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] data | La palabra clave y el tipo de coincidencia. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] y  [!DNL Search] datos | El tipo de anuncio, como `text`, `video`, `display` o `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] y  [!DNL Search] datos | El tipo de anuncio ([!DNL DSP]) o el título del anuncio ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] y  [!DNL Search] datos | La descripción del anuncio ([!DNL DSP]) o el cuerpo del anuncio ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] data | Dirección URL mostrada en la publicidad. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] data | La dirección URL de destino de la publicidad. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] y  [!DNL Search] datos | Indica si la entrada de página de aterrizaje fue una visualización o una pulsación. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] data | Destino del producto para una publicidad de lista de productos. |

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](overview.md)
>* [[!DNL Analytics] Datos en Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

