---
title: Información general sobre Campaign Management en Advertising Cloud DSP
description: Obtenga información sobre la jerarquía y los componentes de administración de campañas.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: d180b91f7bf5ae72a51e5335638a98c5fc4b4e86
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# Información general sobre Campaign Management en Advertising Cloud DSP

Las campañas de Advertising Cloud DSP tienen la siguiente jerarquía:

* Campaign
   * Paquete(s)
      * Colocación(es)
         * Anuncios

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising Cloud DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campañas](/help/dsp/campaign-management/campaigns/campaign-about.md) son el marco general de configuración de vuelo. Cada campaña está configurada con un anunciante, fechas de inicio y finalización, un presupuesto general, una opción de objetivo entre dispositivos y un límite de frecuencia predeterminado, y opciones de informes para la visualización, el fraude, la seguridad de la marca y la verificación de audiencia. Todos los ajustes del nivel de campaña se aplican automáticamente a cada paquete y colocación dentro de la campaña.

## [!UICONTROL Packages]

Cada campaña puede contener una o más [paquetes](/help/dsp/campaign-management/packages/package-about.md), cada uno de los cuales incluye un conjunto de ubicaciones.

Utilice paquetes para agrupar ubicaciones para su envío a un presupuesto, un objetivo de rendimiento y una estrategia de ritmo personalizada. DSP optimiza los paquetes cambiando los presupuestos a las ubicaciones con mejor rendimiento del paquete. Puede organizar los paquetes por formato de ubicación, tipo de inventario, proveedor de datos, persona u otras características distinguibles.

Los paquetes son opcionales, pero se recomiendan.

## [!UICONTROL Placements]

A [placement](/help/dsp/campaign-management/placements/placement-about.md) almacena parámetros de objetivo para una o más publicidades del mismo tipo de publicidad. Puede crear una colocación para una sola campaña o paquete y luego asignarle publicidades.

## [!UICONTROL Ads]

[Publicidades](/help/dsp/campaign-management/ads/ad-about.md) incluya recursos creativos y direcciones URL de seguimiento. Puede cargar etiquetas de servicios de publicidad de terceros de forma individual o en lote mediante hojas de etiquetas de socios o la plantilla de etiquetas en bloque. También puede crear manualmente anuncios en pantalla nativos para DSP que se vayan a mostrar.

Una vez configuradas las publicidades, deberá adjuntarlas a una ubicación. Puede adjuntar una sola publicidad a una o más ubicaciones.

Todos los anuncios activos y aprobados de una colocación activa en una campaña activa pueden ejecutarse según los parámetros de objetivo de colocación.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de campañas](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Acerca de la administración de paquetes](/help/dsp/campaign-management/packages/package-about.md)
>* [Acerca de la administración de ubicaciones](/help/dsp/campaign-management/placements/placement-about.md)
>* [Acerca de la administración de publicidad](/help/dsp/campaign-management/ads/ad-about.md)
>* [Lista de comprobación de Campaign Launch](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Prácticas recomendadas para configurar campañas de rendimiento](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Acerca de los informes en la plataforma](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Acerca de las vistas de datos de campaña](/help/dsp/campaign-management/reports/campaign-data-views-about.md)
>* [Vídeo: Estructura de la cuenta de DSP e interfaz de usuario](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/ui.html)

