---
title: Especificar colocaciones y publicidades para un ID de acuerdo
description: Aprenda a utilizar una oferta privada con ubicaciones y publicidades adicionales.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 669cadcf-021b-4129-95d5-3d24af4a4b88
source-git-commit: 3e47fec28a17cb64de42309c0368293e1ef1cdea
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---

# Especificar colocaciones y publicidades para un ID de acuerdo

Para las ofertas no garantizadas, puede especificar la oferta como objetivo de inventario para las nuevas ubicaciones desde la variable [!UICONTROL Placements] vista.

Para las ofertas garantizadas mediante programación (PG), puede crear nuevas ubicaciones con anuncios especificados desde la variable [!UICONTROL Deals] vista.

También puede [adjuntar nuevas publicidades a ubicaciones existentes](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) asociados con PG y operaciones no garantizadas en cualquier momento.

## Especificar un acuerdo no garantizado como destino de inventario para una ubicación

* [Cree una ubicación desde el [!UICONTROL Placements] ver](/help/dsp/campaign-management/placements/placement-create.md). En el [!UICONTROL Inventory Targeting] , seleccione la oferta privada.

## Adjuntar colocaciones y publicidades a un acuerdo de PG

1. En el menú principal, haga clic en **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. En la fila de acuerdo, haga clic en  ![Menú Opciones](/help/dsp/assets/options-menu.png) **>[!UICONTROL attach a placement]**.

1. En el [!UICONTROL Ad & Campaign Selection] , seleccione las publicidades que se utilizarán para la colocación:

       1. Seleccione el anunciante, la campaña y el tipo de publicidad. De forma opcional, seleccione un estado de publicidad mediante el cual filtrar las publicidades.
       
       1. En la lista de publicidades disponibles, active la casilla de verificación situada junto a cada publicidad que se utilizará para la oferta.
       
       1. Haga clic **[!UICONTROL Apply]**.
   
   1. En la pantalla de configuración de ubicación:

      1. Introduzca el nombre de la colocación.

      1. (Opcional) Edite el [configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md), incluida la sobrescritura de la oferta predeterminada, que se rellena automáticamente con el valor CPM de la oferta; cambiar el intervalo de fechas; o adjuntar más anuncios.

      La oferta se segmenta automáticamente en la sección Destinos de inventario . Todas las demás opciones de segmentación no son aplicables.

      1. Haga clic **[!UICONTROL Create placement]**.


La ubicación empezará a ejecutarse después de que el editor active su ID de oferta de PG.

>[!NOTE]
>
> No es necesario que envíe la etiqueta de oferta al editor para que la verifique.

>[!MORELIKETHIS]
>
>* [Acerca del inventario privado](private-inventory-about.md)
>* [Lista de colocaciones y publicidades de un acuerdo privado](/help/dsp/inventory/private-deal-view-placements.md)
>* [Crear manualmente detalles de ID de acuerdo](deal-id-create.md)
>* [Configuración manual del ID de trato](deal-id-settings.md)
>* [Configuración de un acuerdo garantizado programático](programmatic-guaranteed-set-up.md)

