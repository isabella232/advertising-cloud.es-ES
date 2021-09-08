---
title: Configuración de publicidad móvil
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios móviles.
feature: Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 0%

---

# Configuración de publicidad móvil

## [!UICONTROL Upload or Select Creative]

*Solo formatos de anuncios de vídeo móvil nuevos*

**[!UICONTROL Vertical video]:** (No disponible cuando  [!UICONTROL Custom Transcode] está seleccionado) Indica que el vídeo es vertical (modo vertical).

**[!UICONTROL Transcode to]:** (Algunos usuarios, según los permisos; (opcional) los formatos que desea incluir en la etiqueta VAST cuando el editor tiene requisitos específicos de archivos creativos. Los formatos aceptados por la mayoría de los editores están seleccionados de forma predeterminada.

**[!UICONTROL Custom Transcode]:**  (solo usuarios beta; no disponible cuando está seleccionado Vídeo vertical ) Indica que el vídeo utiliza transcodificación personalizada. Si selecciona esta opción, especifique el formato de archivo, la velocidad de bits del vídeo, el zoom y las dimensiones para hasta tres versiones de transcodificación personalizadas.

**[!UICONTROL XTrader]:** (Algunos usuarios, según los permisos) Indica que el vídeo utiliza otra  [!DNL X_TRADER] fuente más.

**[!UICONTROL Upload Video]:** Para cargar un recurso sin procesar en DSP. Cuando seleccione esta opción, haga lo siguiente:

1. Haga clic en **[!UICONTROL Choose File]** y busque el archivo en su dispositivo o red.
1. Introduzca un título para el archivo, que se utilizará en la vista [!UICONTROL Ads] y en los informes.
1. Haga clic **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Video]:** Para seleccionar cualquier creativo cargado anteriormente con el formato correcto dentro de la cuenta.

**[!UICONTROL Advanced: VAST Tag URL]:**  (Algunos tipos de anuncios) Para introducir una etiqueta VAST de terceros que contenga recursos creativos y rastreando píxeles:

1. Haga clic en ![flecha](/help/dsp/assets/compressed.png) junto a **[!UICONTROL Advanced: VAST Tag URL]**.
1. En el campo **[!UICONTROL URL]**, introduzca la URL de la etiqueta VAST.
1. Introduzca un **[!UICONTROL Title]** para el archivo, que se utilizará en la vista [!UICONTROL Ads] y en los informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la tecla **[!UICONTROL Enter]**. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

**[!UICONTROL Advanced: 3rd party Ad Tag]:**  (Algunos tipos de publicidad) Para introducir una etiqueta de publicidad de terceros que contenga recursos creativos y rastreando píxeles:

1. Haga clic en ![flecha](/help/dsp/assets/compressed.png) junto a **[!UICONTROL Advanced: #3rd party Ad Tag]**.
1. Introduzca un **[!UICONTROL Ad Title]** para el archivo, que se utilizará en la vista [!UICONTROL Ads] y en los informes.
1. En el campo **[!UICONTROL Ad Tag]**, introduzca la etiqueta de publicidad.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Publicidades para pantallas móviles

**[!UICONTROL Ad Type]:**  (Solo lectura) El tipo de publicidad que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la vista Anuncios y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 300x250 Gamer&quot;).

**\[Fuente de publicidad\]**: Si Advertising Cloud DSP está sirviendo el anuncio (*[!UICONTROL Adobe served]*) o está utilizando un servidor de publicidad de terceros (*[!UICONTROL 3rd party]*).

**[!UICONTROL Creative type]:**  (Solo anuncios de Adobe) Si el recurso es un  *[!UICONTROL Image]* recurso o un  *[!UICONTROL HTML5]* recurso.

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:**  (solo anuncios publicados en Adobe) Archivo de imagen o recurso HTML5 comprimido que se va a cargar, según el tipo de creativo. Haga clic en **[!UICONTROL Browse]** y busque el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:**  (Solo anuncios servidos por Adobe) Dirección URL a la que llegará el espectador cuando haga clic en el anuncio.

**[!UICONTROL Final Click URL]:**  (solo anuncios de Adobe; solo lectura) La URL de clic con el rastreo de  [Advertising Cloud DSP necesario ](/help/dsp/campaign-management/macros.md) macronivdado, si corresponde.

**[!UICONTROL Display Code]:**  (Solo anuncios de terceros) La URL del recurso creativo de terceros. Cualquier parámetro [timestamp] y [[timestamp]] se reemplazará por valores reales.

**[!UICONTROL Final Display Code]:** (Solo anuncios de terceros) La URL del recurso creativo de terceros, con el seguimiento de  [Advertising Cloud DSP necesario ](/help/dsp/campaign-management/macros.md) macronizado, si corresponde.

### [!UICONTROL Basic]: Anuncios de vídeo

**[!UICONTROL Ad Type]:**  (Solo lectura) El tipo de publicidad que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la vista Anuncios y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 30 segundos de predesplazamiento del teléfono&quot;).

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:** Ancho de toda la unidad publicitaria. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:** La altura de toda la unidad publicitaria. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

**[!UICONTROL Player X]:** Coordenada X para la unidad de publicidad. Mantenga la configuración predeterminada.

**[!UICONTROL Player Y]:** Coordenada Y para la unidad de publicidad. Mantenga la configuración predeterminada.

**[!UICONTROL Player Width]:** Ancho de toda la unidad de publicidad. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

Es lo mismo que el campo **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

Es lo mismo que el campo **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Dónde incluir controles de vídeo para el anuncio:  *[!UICONTROL Under]*,  *[!UICONTROL Over]*,  *[!UICONTROL Bottom]* o  *[!UICONTROL None]* (opción predeterminada).

**[!UICONTROL Preserve Aspect Ratio]:** Si se deben mantener las proporciones de ancho y alto del vídeo (*[!UICONTROL Yes]*) o si se debe estirar el vídeo para llenar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:**  (Algunos tipos de anuncios) El número de segundos que se tarda en retrasar el aspecto del botón de cierre.

**[!UICONTROL Click URL]:**  (Solo anuncios servidos por Adobe) Dirección URL a la que llegará el espectador cuando haga clic en el anuncio.

**[!UICONTROL Final Click URL]:**  (solo anuncios de Adobe; solo lectura)  [!UICONTROL Click URL] con el seguimiento necesario de  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) macrosserted, si corresponde.

**[!UICONTROL VAST Tag]:** (los anuncios que solo usan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como recurso creativo.

**[!UICONTROL Final VAST Tag]:** (los anuncios que solo usan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que ha introducido como recurso creativo con el seguimiento de  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) necesario, si corresponde.

**[!UICONTROL Wmode]:**  (Algunos tipos de anuncios) El modo de ventana:  *[!UICONTROL window]*,  *[!UICONTROL transparent]* o  *[!UICONTROL opaque]*.

### [!UICONTROL Teaser]

*Formatos de toque para reproducir para dispositivos móviles para anuncios DSP*

**[!UICONTROL Asset]:** La imagen de teaser o el recurso de vídeo:

* Para seleccionar su propia imagen, haga clic en **[!UICONTROL Choose File],** localice el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload Image]**.

   Se recomienda utilizar una imagen con las mismas dimensiones que la unidad de publicidad.

* Para seleccionar una imagen del creativo, haga clic en **[!UICONTROL Choose Thumbnail]**.

Requisitos para teasers de imagen estáticos:

* Formato: GIF, JPEG, PNG
* Tamaño de la imagen: 300 x 250
* Tamaño del archivo: 50 KB o menos
* Recomendado: llamada a la acción, imagen reconocible, logotipo de marca

Requisitos para los teasers de vídeo:

* Tipo de archivo: MOV, MP4
* Tamaño del archivo: Menos de 2 MB
* Duración: 7 a 10 segundos
* Recomendado: imágenes reconocibles, caras, cortes rápidos

### [!UICONTROL Overlays]

*Formatos interactivos interactivos de anuncio previo a la emisión y móviles y de toque para reproducción para anuncios DSP*

Las siguientes opciones se aplican a cada superposición que cree o edite.

**[!UICONTROL Asset]:**  (Solo recursos sin procesar) El recurso de imagen de superposición. El archivo debe estar en formato GIF, JPG o PNG de un solo fotograma y el tamaño máximo de la imagen debe ser inferior a 2 MB. Para cargar el recurso, haga clic en **[!UICONTROL Browse]**, busque el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

>[!TIP]
>
>Consulte las [Prácticas recomendadas para diseñar superposiciones](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

**[!UICONTROL Click URL]:**  URL a la que llegará el espectador cuando haga clic en una superposición de su publicidad.

**[!UICONTROL X]:** Coordenada X para la superposición. Seleccione la posición de inicio de la superposición y, a continuación, introduzca el número de píxeles desde la posición de inicio (por ejemplo, 10 píxeles desde el centro). La práctica recomendada es utilizar *Desde el centro*, lo que evita que la superposición se mueva con diferentes tamaños de reproductor en los sitios del editor.

**[!UICONTROL Y]:** La coordenada Y para la superposición. Seleccione la posición inicial de la superposición y, a continuación, introduzca el número de píxeles desde la posición inicial (como 10 píxeles desde arriba). La práctica recomendada es especificar una coordenada *[!UICONTROL From Bottom]* o *[!UICONTROL From Top],* en función de la posición en la que desea que se muestre la superposición en el anuncio.

**[!UICONTROL Layer]:** La capa en la que aparecerá la superposición. El vídeo y cada superposición se encuentran en capas independientes.

* *[!UICONTROL 2 through 5]:* Delante del vídeo pero detrás de otras superposiciones.

* *[!UICONTROL 1]:* Delante del vídeo.

* *[!UICONTROL 0]:* en la misma capa que el vídeo. El vídeo se reducirá para ocupar el espacio restante. No recomendado para la preconfiguración interactiva.

* *[!UICONTROL -1]:* Detrás del vídeo.

* *[!UICONTROL -2 through -5]:* Detrás del vídeo pero delante de otras superposiciones.

* *[!UICONTROL Background]:* Detrás del vídeo y otras superposiciones. La superposición se escalará hasta el ancho y la altura completos del vídeo y no se conservará la relación de aspecto.

### [!UICONTROL Endcap]

Obsoleto

### [!UICONTROL Pixel]

Todos los píxeles de seguimiento de eventos existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento.

Las siguientes opciones se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel para que se active. Para este tipo de anuncio, utilice píxeles que se activen en *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indica si el píxel es un  *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles),  *[!UICONTROL HTML]* o  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** La dirección URL de la imagen en píxeles, en el formato adecuado para el  [!UICONTROL Pixel Type] especificado.

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* o  *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Acerca de la administración de publicidad](ad-about.md)
>* [Crear una publicidad](ad-create.md)
>* [Enumerar las ubicaciones asociadas a una publicidad](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tipos de anuncios disponibles](ad-types.md)
>* [Especificaciones de la publicidad](/help/dsp/assets/ad-specs.pdf)
>* [Prácticas recomendadas para el diseño de superposiciones](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Macros de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

