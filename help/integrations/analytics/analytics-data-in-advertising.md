---
title: "[!DNL Analytics] Datos en publicidad de Adobe"
description: "[!DNL Analytics] Datos en publicidad de Adobe"
feature: Integration with Adobe Analytics
exl-id: 79fbc809-9965-41c1-971f-3652cc78fee3
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Datos en publicidad de Adobe

*Anunciantes con Adobe de solo integración de Advertising-Adobe Analytics*

## Segmentos de Analytics

Todos los segmentos creados en [!DNL Analytics] y publicado para el Experience Cloud.

Los nuevos segmentos tardan entre 24 y 48 horas en aparecer en la publicidad de Adobe. Las actualizaciones de los segmentos existentes se sincronizan en un plazo aproximado de ocho horas.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Métricas de participación en el sitio

>[!NOTE]
>
>* [!DNL Analytics] pasa eventos para el eVar de EF ID a la publicidad de Adobe.  La integración predeterminada no admite el envío de métricas calculadas u otras dimensiones (eVars) a Publicidad de Adobe. Sin embargo, si la métrica calculada se puede capturar por completo en un evento personalizado, la publicidad de Adobe puede ingerir el evento personalizado.
>* [!DNL Analytics] pasa datos a Adobe Advertising por hora.


* [!UICONTROL Timespent_secs_1stvisit]: El número de segundos empleados en el sitio durante la primera visita del visitante.
* [!UICONTROL Timespent_secs_total]: Número total de segundos empleados en el sitio en todas las visitas dentro de la ventana de retrospectiva de clics.
* [!UICONTROL Pageviews_1stvisit]: Número de vistas de página del sitio durante la primera visita del visitante.
* [!UICONTROL Pageviews_total]: Número total de vistas de página del sitio en todas las visitas dentro de la ventana retrospectiva de clics.
* [[!UICONTROL Bounces] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: El número de veces que [!DNL Analytics] recopilan un [!UICONTROL EF ID].

## Métricas de conversión

[!DNL Analytics] pasa métricas de conversión a Adobe Advertising diariamente.

### Métricas de conversión estándar

* [[!UICONTROL Revenue] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] métrica](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Métricas de conversión personalizadas

Estas métricas son específicas del grupo de informes, por lo que las métricas disponibles varían para cada cliente y grupo de informes.

### Métricas de conversión reservadas

Estas métricas son específicas del grupo de informes, por lo que las métricas disponibles varían para cada cliente y grupo de informes.

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising]](overview.md)
>* [Métricas de publicidad de Adobe en Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)

