---
title: Crear una colocación
description: Aprenda a crear una colocación.
feature: DSP Placements
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---

# Crear una colocación

>[!TIP]
>
>Cree ubicaciones basadas en objetivos de campaña específicos o en necesidades de informes.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña en la que se incluirá la ubicación.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**. En el [!UICONTROL Placement Types] del menú, haga clic en el tipo de ubicación.

   El tipo de ubicación determina el tipo de anuncio que puede incluir la ubicación.

1. Introduzca la variable [configuración de ubicación](placement-settings.md):

   1. Especifique la variable [!UICONTROL Basics] configuración.

   1. En el [!UICONTROL Goals] especifique la [!UICONTROL Gross Budget] y, opcionalmente, especificar objetivos de ubicación adicionales.

      Algunos campos tienen valores predeterminados que se pueden anular.

      Si el paquete al que se asigna la ubicación tiene un ritmo de nivel de paquete, los objetivos y la configuración de ritmo reflejarán la configuración del paquete.

   1. (Opcional) En la [!UICONTROL Geo-Targeting] , reduzca las ubicaciones que se incluyen o excluyen.

      Si no identifica ubicaciones específicas, se segmentan todas las ubicaciones.

      >[!NOTE]
      >
      >Las ubicaciones de ciudad y DMA no están disponibles para las ubicaciones de Roku.

   1. En el [!UICONTROL Inventory Targeting] , reduzca los orígenes de inventario que desea incluir o excluir.

      Para la mayoría de los tipos de ubicación, todos los tipos de inventario y todas las fuentes para cada tipo están incluidos de forma predeterminada. Para [!DNL Roku] ubicaciones, debe especificar el tipo de inventario y los orígenes.

   1. (Opcional) En la [!UICONTROL Site Targeting] , reduzca los sitios a los que desea dirigirse y especifique los sitios que desea excluir.

   1. (Opcional) En la [!UICONTROL Audience Targeting] sección:

      1. Reduzca la audiencia. Esto incluye la selección de segmentos de audiencia para dirigirse dentro de la ubicación.

         Para [!DNL] Colocaciones Roku, puede aprovechar [La audiencia única de DSP coincide con [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) al incluir uno o más segmentos de audiencia que se puedan comparar con el [!DNL Roku] conjunto de datos determinísticos (incluido).
   1. (Para campañas con segmentación entre dispositivos a nivel de personas; (opcional) cuando la ubicación se dirige a una o más audiencias específicas, habilite la segmentación entre dispositivos basada en personas para la ubicación.

      La segmentación entre dispositivos basada en personas la proporciona [!DNL LiveRamp] utilizando solo datos de EE. UU. El servicio está disponible para todos los anunciantes a un CPM de 0,35 $ para impresiones que se entregan utilizando la variable [!DNL LiveRamp] gráfico de dispositivos (es decir, para dispositivos no encontrados dentro de los segmentos de audiencia de destino).

   1. (Opcional) En la [!DNL Brand Safety and Media Targeting] , aplique restricciones de seguridad de marca para sus colocaciones.

   1. (Opcional) En la [!DNL Tracking] , introduzca píxeles de evento de terceros o píxeles de conversión para los anuncios en la ubicación.

      >[!NOTE]
      >
      >([!DNL Roku] colocaciones) Proveedores de píxeles de terceros aprobados por [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]y [!DNL Research Now].


1. Haga clic **[!UICONTROL Create Placement]**.

1. (Opcional) Adjunte los anuncios a la ubicación:

   1. Haga clic **[!UICONTROL Attach an ad]**.

   1. Realice una de las siguientes acciones:
   * Para crear una publicidad nueva:

      1. Haga clic **[!UICONTROL Create a New Ad].**

      1. Especifique la configuración de publicidad para [anuncios de audio](/help/dsp/campaign-management/ads/ad-settings-audio.md), [TV conectada](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [anuncios en pantalla](/help/dsp/campaign-management/ads/ad-settings-display.md), [anuncios móviles](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [anuncios nativos](/help/dsp/campaign-management/ads/ad-settings-native.md), [anuncios previos a la emisión](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)o [anuncios universales en vídeo](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

      1. Haga clic **[!UICONTROL Save & Submit for Review]**.

      1. (Opcional) Para cada publicidad adicional que desee crear para la ubicación, haga clic en **[!UICONTROL Attach Another Ad]** y, a continuación, repita los pasos del 1 al 3.

      1. Si no adjunta ninguna publicidad existente, haga clic en **[!UICONTROL I'm done for now]**.
   * Para adjuntar anuncios existentes en la campaña:

      1. Haga clic **[!UICONTROL Select an Ad]**.

      1. Realice una de las siguientes acciones:

         * Para agregar una publicidad a la vez:

            1. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select].**

            1. (Opcional) Para cada publicidad adicional que desee adjuntar, haga clic en **[!UICONTROL Attach Another Ad]** y, a continuación, repita el proceso.
         * Para agregar hasta 20 anuncios a la vez:

            1. Seleccione la casilla de verificación situada encima de la lista de anuncios.

            1. Seleccione la casilla de verificación situada junto a cada publicidad que desee agregar.

            1. Haga clic **[!UICONTROL Attach]**.

            1. Junto al nombre del anuncio, haga clic en **[!UICONTROL Select]**.
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






>[!MORELIKETHIS]
>
>* [Acerca de la administración de ubicaciones](placement-about.md)
>* [Editar una colocación](placement-edit.md)
>* [Editar la programación de publicidad de una colocación](placement-edit-ad-schedule.md)
>* [Poner en pausa o activar una colocación](placement-pause-activate.md)
>* [Ver el registro de cambios de una colocación](placement-change-log.md)
>* [Configuración de colocación](placement-settings.md)
>* [Métodos abreviados del teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[Resolución de problemas del rendimiento](/help/dsp/optimization/troubleshooting-performance.md)
>* [Vídeo: Cómo crear una colocación de visualización estándar](https://video.tv.adobe.com/v/340454)

