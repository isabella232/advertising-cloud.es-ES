---
title: Adjuntar una publicidad a una colocación
description: Aprenda a adjuntar una publicidad a una ubicación.
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 1%

---

# Adjuntar una publicidad a una colocación

## Adjuntar una publicidad nueva desde el [!UICONTROL Ads] Ver

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Ads]**.

1. Junto al nombre del anuncio, haga clic en  **... >[!UICONTROL Add to Placements]**.

1. En la pantalla Colocar publicidad , realice una de las acciones siguientes:

   * Para crear una nueva ubicación para la publicidad:

      1. Haga clic **[!UICONTROL Create New Placement]**.

      1. Introduzca la variable [configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)y, a continuación, haga clic en **[!UICONTROL Create Placement]**.
   * Para agregar la publicidad a una o más ubicaciones existentes:

      1. Haga clic **[!UICONTROL Select a Placement].**

      1. Realice una de las siguientes acciones:

         * Para agregar una publicidad a la vez:

            1. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select].**

            1. (Opcional) Para cada publicidad adicional que desee adjuntar, haga clic en **[!UICONTROL Attach to Other Placement]**. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select].**
         * Para adjuntar la publicidad a un máximo de 20 ubicaciones a la vez:

            1. Seleccione la casilla de verificación situada junto a **Selección masiva&quot;.

            1. Seleccione la casilla de verificación situada junto a cada ubicación a la que desee adjuntar la publicidad.

            1. Haga clic **[!UICONTROL Attach]**.
      1. En la ficha Completar y revisar , seleccione una de las siguientes opciones:

         * Para volver a la vista Publicidades, haga clic en **[!UICONTROL I'm done for now]**.

         * Para adjuntar la publicidad a otra ubicación, haga clic en **[!UICONTROL Attach To Other Placement]**.




## Adjuntar una publicidad nueva o existente desde el [!UICONTROL Placements] Ver

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Placements]**.

1. Junto al nombre de la ubicación, haga clic en  **... > [!UICONTROL Attach Ads].**

1. En el [!UICONTROL Add Ad to Placement] , realice una de las acciones siguientes:

   * Para crear una publicidad nueva:

      1. Haga clic **[!UICONTROL Create a New Ad]**.

      1. Introduzca la configuración de publicidad para [anuncios de audio](ad-settings-audio.md), [TV conectada](ad-settings-connected-tv.md), [anuncios en pantalla](ad-settings-display.md), [anuncios móviles](ad-settings-mobile.md), [anuncios nativos](ad-settings-native.md)o [anuncios previos a la emisión](ad-settings-pre-roll.md).

      1. Haga clic **[!UICONTROL Save & Submit for Review]**.

         La variable [revisión de anuncio](ad-about.md) para el nuevo anuncio tarda de 24 a 48 horas e incluye comprobaciones de categorías delicadas, clic en la funcionalidad URL y vista previa del procesamiento. La variable [!UICONTROL Status] indica si DSP ha aprobado el anuncio. Los anuncios rotos pueden tener un estado pendiente durante más de 24-48 horas, por lo que tiene tiempo para corregir errores antes de que se rechacen.

         >[!NOTE]
         >
         >Su publicidad solo se publicará si tanto DSP como la SSP han aprobado el elemento creativo. Cada SSP tiene sus propios requisitos y procesos de aprobación.
   * Para seleccionar publicidades existentes:

      1. Haga clic **[!UICONTROL Select an Ad].**

      1. Especifique las publicidades:
         * Para agregar una publicidad a la vez:

            1. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select].**

            1. (Opcional) Para cada publicidad adicional que desee adjuntar, haga clic en **[!UICONTROL Add Another Ad]**. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select].**
         * Para agregar hasta 20 anuncios a la vez:

            1. Seleccione la casilla de verificación situada junto a **[!UICONTROL Bulk Select]**.&quot;

            1. Seleccione la casilla de verificación situada junto a cada publicidad que desee agregar.

            1. Haga clic **[!UICONTROL Attach]**.
      1. (Opcional) Para anular el periodo de vuelo predeterminado y la rotación de anuncios para anuncios específicos en la ubicación:

         1. Haga clic **[!UICONTROL Custom Schedule Ads]**.

         1. Realice una de las siguientes acciones:

            * Para añadir un vuelo, haga clic en **[!UICONTROL Add Flight]** y, a continuación, especifique la fecha de inicio y la fecha de finalización.

            * Para añadir un vuelo existente a un anuncio, haga clic en **[!UICONTROL +]** en la fila de publicidad de la columna &quot;flight&quot;.

            * Para eliminar un vuelo existente de un anuncio, haga clic en **[!UICONTROL x]** en la fila de publicidad de la columna &quot;flight&quot;.

            * (Cuando varios anuncios tengan el mismo vuelo) Para girar los anuncios de forma desigual, haga clic en **[!UICONTROL Even Rotation]** en la información de vuelo y, a continuación, introduzca el peso relativo por el que debe rotar cada anuncio, como porcentaje.

               El peso total debe ser igual a 100.
         1. En la esquina superior derecha, haga clic en **[!UICONTROL Continue]**.

         1. Revise los detalles del vuelo y haga clic en **[!UICONTROL Save & Finish]**.
      1. Haga clic **[!UICONTROL I'm done for now]**.






>[!MORELIKETHIS]
>
>* [Acerca de la administración de publicidad](ad-about.md)
>* [Crear una sola publicidad](ad-create.md)
>* [Crear varias publicidades de terceros](ad-create-multiple.md)
>* [Editar una publicidad](ad-edit.md)
>* [Enumerar las ubicaciones asociadas a una publicidad](ad-list-placements.md)
>* [Editar la programación de publicidad de una colocación](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)

