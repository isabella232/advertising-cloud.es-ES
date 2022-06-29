---
title: Crear manualmente detalles de ID de acuerdo
description: Obtenga información sobre cómo introducir manualmente los detalles de un ID de acuerdo.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Crear manualmente detalles de ID de acuerdo

1. En el menú principal, haga clic en **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]** y, a continuación, seleccione **[!UICONTROL Deal ID]**.

1. Introduzca la variable [configuración de acuerdo](deal-id-settings.md):

   1. En el [!UICONTROL Deal ID basics] , especifique los detalles de la oferta y los anunciantes que pueden acceder a la oferta. Para ofertas garantizadas, también debe especificar las fechas de vuelo previstas y el número estimado de impresiones, solo con fines de seguimiento.

   1. (Solo usuarios administradores; (opcional) En la [!UICONTROL Technical] , edite la configuración predeterminada según sea necesario.

   1. Haga clic **[!UICONTROL Save]**.

1. (Solo ofertas garantizadas) Seleccione las publicidades que desea utilizar para la oferta y cree una colocación garantizada mediante programación (PG) predeterminada.

   Las ubicaciones de PG predeterminadas garantizan que la oferta siempre devuelva una oferta por cada solicitud de oferta. Si no se crea una colocación de PG predeterminada, las ubicaciones a las que se dirija la oferta no generan ofertas a menos que estén configuradas correctamente. Siempre debe crear una colocación de PG predeterminada. En el [!UICONTROL Placements] vista, las ubicaciones de PG predeterminadas tienen una [!UICONTROL Sub-type] valor de columna de &quot;[!UICONTROL PG Default].&quot;

   Si lo desea, puede utilizar la oferta como destino de inventario en ubicaciones adicionales, pero debe configurarlas correctamente para colocar ofertas.

   1. En el [!UICONTROL Ad & Campaign Selection] , seleccione las publicidades que se utilizarán para la oferta:

      1. Seleccione el anunciante, la campaña y el tipo de publicidad. De forma opcional, seleccione un estado de publicidad mediante el cual filtrar las publicidades.

      1. En la lista de publicidades disponibles, active la casilla de verificación situada junto a cada publicidad que desee utilizar para la oferta.

      1. Haga clic **[!UICONTROL Apply]**.
   1. En la pantalla de configuración de ubicación:

      1. Introduzca el nombre de la colocación.

      1. (Opcional) Edite el [configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md), incluida la sobrescritura de la oferta predeterminada, que se rellena automáticamente con el valor CPM de la oferta; cambiar el intervalo de fechas; o adjuntar más anuncios.

      La oferta se segmenta automáticamente en la sección Destinos de inventario . Todas las demás opciones de segmentación no son aplicables.

      1. Haga clic **[!UICONTROL Create placement]**.



Después de crear la oferta, puede usar la oferta como destino de inventario para varias ubicaciones.

>[!NOTE]
>
> No es necesario que envíe la etiqueta de oferta al editor para que la verifique.

>[!TIP]
>
>* En el [!UICONTROL Inventory] > [!UICONTROL Deals] la vista [!UICONTROL Pacing & Budget] muestra cómo la oferta se está acercando a la fecha de vuelo y al objetivo de impresión especificados.
>
>* Si la entrega está a un ritmo inferior o superior, póngase en contacto con su editor para ajustar el volumen que envía a través de la oferta.


>[!MORELIKETHIS]
>
>* [Configuración manual del ID de trato](deal-id-settings.md)
>* [Configuración de un acuerdo garantizado programático](programmatic-guaranteed-set-up.md)
>* [Enviar una publicidad para un acuerdo garantizado programático con [!DNL FreeWheel]](freewheel-submit.md)
>* [Acerca de los Ofertas Garantizadas mediante Programación](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->