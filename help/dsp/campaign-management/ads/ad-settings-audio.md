---
title: Configuración de anuncios de audio
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios de audio.
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# Configuración de anuncios de audio

## [!UICONTROL Upload or Select Creative]

*Solo anuncios nuevos*

**[!UICONTROL Upload Audio]:** Para cargar un recurso sin procesar en DSP. Cuando seleccione esta opción, haga lo siguiente:

1. Haga clic en **[!UICONTROL Choose File]** y busque el archivo en su dispositivo o red.
1. Introduzca un título para el archivo, que se utilizará en la variable [!UICONTROL Ads] ver e informes.
1. Haga clic **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** Para seleccionar cualquier creativo cargado anteriormente con el formato correcto dentro de la cuenta.

**[!UICONTROL Advanced: VAST Tag URL]:** Para introducir una etiqueta VAST de terceros que contenga recursos creativos y rastreando píxeles:

1. Haga clic en ![flecha](/help/dsp/assets/compressed.png) junto a **[!UICONTROL Advanced: VAST Tag URL]**.
1. En el **[!UICONTROL URL]** , introduzca la URL de la etiqueta VAST.
1. Escriba un **[!UICONTROL Title]** para el archivo , que se utilizará en la variable [!UICONTROL Ads] ver e informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la opción **[!UICONTROL Enter]** clave. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad. Su valor predeterminado es *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la variable [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: Audio de 30 segundos&quot;).

**[!UICONTROL Ad Duration]:** Longitud del archivo de audio. Se configura automáticamente como [!UICONTROL 15] o [!UICONTROL 30], según la unidad de publicidad seleccionada.

Este campo puede mostrarse o no, en función de los permisos de la cuenta.

**[!UICONTROL Click URL]:** (Los anuncios que utilizan recursos sin procesar y solo con banners de visualización; (opcional) la dirección URL a la que llegará el espectador cuando haga clic en un banner de visualización que acompañe a su publicidad.

**[!UICONTROL Final Click URL]:** (Los anuncios que utilizan recursos sin procesar y solo con banners de visualización; solo lectura) La variable [!UICONTROL Click URL] con los [Macros de seguimiento de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL VAST Tag]:** (Anuncios que solo usan etiquetas VAST) Una dirección URL para una fuente de publicidad de terceros. Asegúrese de que la etiqueta VAST incluya solo archivos multimedia de audio.

**[!UICONTROL Final VAST Tag]:** (Los anuncios que utilizan únicamente etiquetas VAST) La dirección URL del origen de los anuncios de terceros con los [Macros de seguimiento de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Select Rate]:** (Usuarios con permiso solamente) Una tasa previamente negociada facturada a través del Adobe, o una de las tarifas que ha negociado y se facturará a través del proveedor. Para agregar una tasa, póngase en contacto con su [!DNL Adobe] equipo de la cuenta.

### [!UICONTROL Companion]

*Solo anuncios DSP*

Si lo desea, puede adjuntar hasta tres banners adjuntos con un anuncio. La práctica recomendada es adjuntar banners complementarios siempre que sea posible.

>[!NOTE]
>
>* No todos los editores permiten banners complementarios. Los editores que sí permiten banners complementarios no garantizan impresiones de banners complementarios.
>* Es posible que los banners adjuntos de etiquetas de publicidad de terceros no siempre estén disponibles para la vista previa.


**\[Casilla de verificación\]:** Incluye el banner complementario especificado con el anuncio. Cuando la casilla de verificación está desactivada, no se incluye el banner complementario.

**\[Tamaño del banner\]:** El tamaño del banner complementario: *[!UICONTROL 300x250]* (se usa para [!DNL iHeartRadio], [!DNL Spotify], [!DNL SoundCloud]y [!DNL TuneIn]), *[!UICONTROL 640x640]* (se usa para [!DNL Spotify), or *1024x1024]* (se usa para [!DNL SoundCloud]).

**\[Fuente\]:** Origen del recurso del banner complementario:

* *[!UICONTROL Upload My Own Asset]:* Para cargar su propio recurso.
* *[!UICONTROL Use a Third Party Tag]:* Para introducir una etiqueta de iFrame o script de un socio de servicio de publicidad de terceros certificado.

Utilice una etiqueta de terceros cuando desee rastrear impresiones de banners de terceros.

**[!UICONTROL Asset]:** (Solo recursos sin procesar) El recurso del banner complementario, en formato GIF, JPG o PNG. Haga clic en **[!UICONTROL Browse]** y busque el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:** (Solo recursos sin procesar) La URL en la que llegará el visor cuando haga clic en el banner complementario del anuncio. Puede incluir un redireccionamiento de clics mediante un píxel de rastreo de clics de terceros.

**[!UICONTROL Final Click URL]:** (Sólo activos sin procesar; solo lectura) La URL del clic con la [Macros de seguimiento de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Ad Tag]:** (Anuncios que solo utilizan etiquetas de publicidad de terceros) Una etiqueta de banner de iFrame o script para un origen de banner complementario de terceros. Debe proceder de un socio de terceros certificado que preste servicios.

**[!UICONTROL Final Ad Tag]:** (Los anuncios que usan etiquetas de publicidad de terceros solo) La etiqueta de publicidad con la etiqueta de publicidad necesaria [Macros de seguimiento de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insertado, si procede.

### Píxel

Todos los píxeles de seguimiento de eventos existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento.

Las siguientes opciones se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel que se activará. Para este tipo de anuncio, utilice píxeles que se activen en la variable *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indica si el píxel es un *[!UICONTROL IMG UR]L* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Dirección URL de la imagen de píxel, en el formato adecuado para el tipo de píxel especificado.

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* o *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de publicidad](ad-about.md)
>* [Crear una publicidad](ad-create.md)
>* [Enumerar las ubicaciones asociadas a una publicidad](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tipos de anuncios disponibles](ad-types.md)
>* [Especificaciones de la publicidad](/help/dsp/assets/ad-specs.pdf)
>* [Macros de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

