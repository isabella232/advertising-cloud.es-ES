---
title: Especificar ubicaciones y publicidades para un acuerdo privado
description: Aprenda a utilizar una oferta privada con ubicaciones y publicidades adicionales.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---

# Especificar ubicaciones y publicidades para un acuerdo privado

Para las ofertas no garantizadas, puede especificar la oferta como objetivo de inventario para las nuevas ubicaciones desde la variable [!UICONTROL Placements] vista.

Para las ofertas garantizadas mediante programación (PG), puede crear ubicaciones con anuncios especificados desde la variable [!UICONTROL Deals] vista.

También puede [adjuntar nuevas publicidades a ubicaciones existentes](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) asociados con PG y operaciones no garantizadas en cualquier momento.

## Especificar un acuerdo no garantizado como destino de inventario para una ubicación

* [Cree una ubicación desde el [!UICONTROL Placements] ver](/help/dsp/campaign-management/placements/placement-create.md). En el [!UICONTROL Inventory Targeting] , seleccione la oferta privada.

## Adjuntar colocaciones y publicidades a un acuerdo de PG

1. En el menú principal, haga clic en **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. En la fila de acuerdo, haga clic en  **[!UICONTROL ...]>[!UICONTROL Attach New Placement]**.

1. En el [!UICONTROL Ad & Campaign Selection] , seleccione las publicidades que desee utilizar para la colocación:

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

