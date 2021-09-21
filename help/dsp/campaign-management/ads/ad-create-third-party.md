---
title: Crear varias publicidades de terceros
description: Aprenda a crear varias publicidades de terceros a la vez.
feature: DSP Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Crear varias publicidades de terceros

Puede crear hasta 500 publicidades de terceros a la vez cargando etiquetas que apunten a recursos creativos alojados en servidores de publicidad de terceros. Puede incluir el seguimiento de píxeles para los anuncios.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Puede cargar hojas de etiquetas [!DNL DoubleClick] y [!DNL Flashtalking] o un archivo rellenado manualmente mediante la plantilla proporcionada.

Para crear una sola publicidad de terceros, consulte [Crear una publicidad](ad-create.md).

>[!TIP]
>
> La práctica recomendada es utilizar anuncios de terceros que se proporcionen de forma segura mediante HTTPS. Las direcciones URL servidas mediante HTTPS empiezan por &quot;https&quot;.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña en la que se incluirá la publicidad.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**. En la sección Tipos de publicidad del menú, haga clic en **[!UICONTROL Bulk upload ads]**.

1. Seleccione el servidor de publicidad en el que se aloja la publicidad: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* o *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] y [!DNL Flashtalking] anuncios) Seleccione el tipo de etiqueta que se utilizará para cada recurso de vídeo y para cada recurso de visualización. Las opciones disponibles varían según el servidor de publicidad.

1. (Anuncios en todos los servidores de publicidad excepto [!DNL DoubleClick] y [!DNL Flashtalking]) Haga clic en **[!UICONTROL Download this template]** para descargar una plantilla en formato [!DNL Microsoft Excel] hoja de cálculo (XLSX), que puede rellenar con datos de publicidad y guardar localmente. Las columnas requeridas incluyen [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag] y [!UICONTROL Ad Types].

1. Haga clic en **[!UICONTROL Upload]** y seleccione un archivo en los formatos .xlsx o .xls desde su dispositivo o red.

   Para las publicidades [!DNL DoubleClick] y [!DNL Flashtalking] , cargue las hojas de etiquetas sin editar desde el servidor de publicidad. Para otros servidores de publicidad, utilice la plantilla que descargó en el paso 3.

1. Una vez finalizada la carga, haga clic en **[!UICONTROL Start Building Ads]**.

1. Revise los detalles y el estado de cada anuncio:

   1. Revise el estado de cada publicidad, que se basa en comprobaciones de validación de la etiqueta cargada.
   1. (Opcional) Realice una de las siguientes acciones para cada anuncio:
      * Para obtener una vista previa de un anuncio, haga clic en ![play](/help/dsp/assets/play.png) en la fila del anuncio.
      * Para editar los detalles de la publicidad, haga clic en ![editar](/help/dsp/assets/edit.png), edite los detalles y, a continuación, haga clic en **Guardar**.
      * Para eliminar una publicidad, haga clic en **[!UICONTROL X]** en la fila de publicidad.

1. Haga clic en **[!UICONTROL Create *N *Anuncios]**.

1. Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL Done]**.

   * (Si se rechaza una publicidad; (opcional) Para editar el registro de publicidad y volver a enviarlo para su revisión:
      1. Haga clic en el nombre del anuncio.
      1. Edite la configuración de la publicidad.
      1. Haga clic **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de publicidad](ad-about.md)
>* [Crear una publicidad](ad-create.md)
>* [Tipos de anuncios disponibles](ad-types.md)
>* [Especificaciones de la publicidad](/help/dsp/assets/ad-specs.pdf)

