---
title: Información general sobre la administración de campañas en Advertising Cloud DSP
description: Obtenga información sobre la jerarquía y los componentes de administración de campañas.
feature: Packages, Placements, Ads, Creatives
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Información general sobre la administración de campañas en Advertising Cloud DSP

Las campañas de Advertising Cloud DSP tienen la siguiente jerarquía:

* Campaign
   * Paquete(s)
      * Colocación(es)
         * Anuncios
            * Creative(s)

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising Cloud DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[](/help/dsp/campaign-management/campaigns/campaign-about.md) Las campañas son el marco general de la configuración de vuelo. Cada campaña está configurada con un anunciante, fechas de inicio y finalización, un presupuesto general, una opción de objetivo entre dispositivos y un límite de frecuencia predeterminado, y opciones de informes para la visualización, el fraude, la seguridad de la marca y la verificación de audiencia. Todos los ajustes del nivel de campaña se aplican automáticamente a cada paquete y colocación dentro de la campaña.

## [!UICONTROL Packages]

Cada campaña puede contener uno o más [paquetes](/help/dsp/campaign-management/packages/package-about.md), cada uno de los cuales incluye un conjunto de ubicaciones.

Utilice paquetes para agrupar ubicaciones para su envío a un presupuesto, un objetivo de rendimiento y una estrategia de ritmo personalizada. DSP optimiza los paquetes cambiando los presupuestos a las ubicaciones con mejor rendimiento del paquete. Puede organizar los paquetes por formato de ubicación, tipo de inventario, proveedor de datos, persona u otras características distinguibles.

Los paquetes son opcionales, pero se recomiendan.

## [!UICONTROL Placements]

Una [ubicación](/help/dsp/campaign-management/placements/placement-about.md) almacena parámetros de objetivo para una o más publicidades del mismo tipo de anuncio. Puede crear una colocación para una sola campaña o paquete y luego asignarle publicidades.

## [!UICONTROL Ads]

[](/help/dsp/campaign-management/ads/ad-about.md) Incluya recursos creativos y URL de seguimiento. Puede cargar sus recursos creativos y DSP publicar los anuncios que los utilizan de forma gratuita, o bien puede cargar etiquetas de servicio de publicidad de terceros.

Una vez configuradas las publicidades, deberá adjuntarlas a una ubicación. Puede adjuntar una sola publicidad a una o más ubicaciones.

Todos los anuncios activos y aprobados de una colocación activa en una campaña activa pueden ejecutarse según los parámetros de objetivo de colocación.

## [!UICONTROL Creatives]

Puede cargar archivos de audio y vídeo para utilizarlos en las publicidades de campañas específicas.
<!-- add link to [About Creative Management](/help/dsp/campaign-management/creatives/creative-about.md) when it's available-->

Puede crear inmediatamente una publicidad con el creativo cargado, o bien puede crearla más tarde desde la vista Creativos o la vista Anuncios.

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

