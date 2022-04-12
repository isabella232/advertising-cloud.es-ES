---
title: Especificaciones de la publicidad
description: Haga referencia a las especificaciones generales y específicas del publicador.
feature: DSP Ads
exl-id: 905dfd9b-e7a3-4eb6-988f-b49d4b282dd2
source-git-commit: f3d4dcfdaaaa4b9546e92ac6d1087e73e5054a26
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# Especificaciones para los tipos de publicidad admitidos

## Anuncios de vídeo (pre-roll y CTV)

### Pantallas compatibles

Los anuncios se entregan de forma predeterminada en dispositivos de escritorio, móviles y TV conectados. La segmentación por dispositivo está disponible para ajustar la entrega.

### Servidores de publicidad de terceros compatibles

Puede utilizar hojas de etiquetas desde [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]y [!DNL Sizmek]. Para obtener una lista completa de los proveedores admitidos, consulte &quot;[Socios certificados de servicio de publicidad](certified-ad-servers.md).&quot;

### Requisitos para los recursos de vídeo de alta definición (obligatorio)

**Tipo de etiqueta de vídeo:** VPAID 2.0 JavaScript o VAST (CTV). Todas las unidades de anuncios VPAID deben adherirse a la variable [Especificación de VPAID 2.0](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) tal como se define en la asociación Interactive Advertising Bureau (IAB).

**Códec de vídeo:** MP4/H.264

**Resolución:** 1280x720 para 720p, 1920x1080 para 1080p

**Velocidad de bits:** De 1500 a 2500 kbps para 720p, de 2500 a 3500 kbps para 1080p

**Perfil/Nivel H.264:** Alto perfil, nivel 3.1 para 720p; Alto perfil, nivel 4.0 para 1080p

**Velocidad de fotogramas de vídeo:** 29,970 fps (comúnmente conocidos como 30 fps) para países NTSC, 25 fps para países PAL, 23,976 fps (comúnmente denominados 24 fps) para contenido con aspecto cinematográfico

**Espacio de color del vídeo:** 4:2:0 Submuestreo de croma YUV

**Interlineado de vídeo:** Escaneo progresivo, es decir, no entrelazado. Sin movimiento dentro del campo (marcos de mezcla) o entrelazado.

**Líderes (pizarra):** No permitido

**Códec de audio:** AAC-LC o HE-AACv1

**Velocidad de bits de audio:** 128 a 192 kbps para AAC-LC, 64 a 128 kbps para HE-AACv1

**Canal de audio:** Mezcla estéreo de 2 canales

**Frecuencia de muestra de audio:** 44,1 kHz o 48 kHz, según el material de origen

**Niveles de audio:** 24 LKFS (+/- 2,0 dB) en EE.UU. según ATSC A/85; 23 LUFS (+/- 1,0) en la UE según EBU R128

#### Requisitos adicionales del editor para anuncios de TV conectados

* **Hulu:** Véase Hulu&#39;s [especificaciones del anuncio](https://advertising.hulu.com/ad-products/video-commercial/).

* **Disney:**

   * Emisión en directo de ESPN:

      **Tasa de bits:** > 14000 kbps
      **Formato:** .mp4
      **Tipo de etiqueta:** VAST 2.0
      **Tamaño creativo:** 1280 x 720 o 1920 x 1080

   * Programación de episodios completos (FEP): ESPN, ABC, Freeform, Nat Geo y FX

      * **Tasa de bits:** > 14000 kbps:

         **Formato:** .mp4

         **Tipo de etiqueta:** VAST 2.0

         **Tamaño creativo:** 1280 x 720 o 1920 x 1080

      * **Tasa de bits:** > 1000 kbps (baja resolución) o 15000 kbps (alta resolución):

         **Formato:** .mp4

         **Tipo de etiqueta:** VAST 2.0 (VPAID 1.0 solo en el escritorio)

         **Tamaño creativo:** 1280 x 720 o 1920 x 1080

## Publicidades de visualización

### Pantallas compatibles

Los anuncios se entregan de forma predeterminada en dispositivos de escritorio y móviles. La segmentación por dispositivo está disponible para ajustar la entrega.

### Tipos de archivo compatibles

**Imagen:** GIF, JPG/JPEG, PNG

**HTML5:** Tipos de archivos de imagen: GIF, JPG/JPEG, PNG, SVG

### Requisitos para los recursos de imagen (obligatorio)

Se admite la visualización universal.

**Tamaños de anuncio recomendados:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x60 0, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x90

**Servidores de publicidad de terceros compatibles:** Puede utilizar hojas de etiquetas desde [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]y [!DNL Sizmek]. Para obtener una lista completa de los proveedores admitidos, consulte &quot;[Socios certificados de servicio de publicidad](certified-ad-servers.md).&quot;

## Anuncios de audio

### Pantallas compatibles

Escritorio, móvil, tableta, altavoces inteligentes y TV conectada

### Servidores de publicidad de terceros compatibles

Puede utilizar hojas de etiquetas desde [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]y [!DNL Sizmek]. Para obtener una lista completa de los proveedores admitidos, consulte &quot;[Socios certificados de servicio de publicidad](certified-ad-servers.md).&quot;

### Requisitos para los recursos de audio (obligatorio)

**Tipo de archivo:** MP3, OGG, AAC

**Líderes (pizarra):**  No permitido

**Tamaño máximo del archivo:** 2 MB

**Velocidad de bits:** 128

**Longitud del archivo:** 0-60

#### Requisitos adicionales del editor

* **[!DNL Spotify]**
   * Longitud: Hasta 30 segundos
   * Tipo de archivo: OGG
   * Tamaño máximo del archivo: 500 MB
   * Volumen: EMR normalizado a -14; Pico dBFS normalizado a -0,2 dBFS

* **[!DNL SoundCloud]**
   * Longitud: 6, 15 o 30 segundos
   * Tipo de archivo: MP3
   * Tamaño máximo del archivo: 5 MB

* **[!DNL Pandora]**
   * Longitud: 15 o 30 segundos
   * Tipo de archivo: MP4 (en la aplicación), MP3 (en el escritorio)
   * Tamaño máximo del archivo: 2,2 MB

* **[!DNL TuneIn]**
   * Longitud: 10, 15 o 30 segundos
   * Tipo de archivo: MP3, OGG
   * Volumen: 44,1 kHz

* **[!DNL iHeartRadio]**
   * Longitud: 5, 15, 30 o 60 segundos
   * Tipo de archivo: MP3
   * Tamaño máximo del archivo: 320 kbps
   * Volumen: 44,1 kHz

* **[!DNL TargetSpot]**
   * Longitud: 15, 30 o 60 segundos
   * Tipo de archivo: MP3

### Requisitos para anuncios de titular Companion (opcional)

**Tamaños compatibles:** 300 x 250, 500 x 500, 640 x 640, 1024 x 1024

#### Requisitos adicionales del editor

* **[!DNL Spotify]:**
   * Tipo de archivo: JPG estático, PNG
   * Tamaño máximo del archivo: 200 KB
   * Dimension: 300 x 250

* **[!DNL SoundCloud]:**
   * Tipo de archivo: JPG estático, PNG
   * Tamaño máximo del archivo: Menos de 400 KB
   * Dimension: 1024x1024

* **[!DNL Pandora]:**
   * Tipo de archivo: JPEG, GIF
   * Tamaño máximo del archivo: Tamaño: 100 KB
   * Dimension: 300x250 (móvil o escritorio) o 500x500 (escritorio)

* **[!DNL TuneIn]:**
   * Tipo de archivo: JPEG, JPG, PNG, GIF, HTML
   * Tamaño máximo del archivo: 2 MB
   * Dimension: 300 x 250

* **[!DNL iHeartRadio]:**
   * Tipo de archivo: JPEG, JPG, PNG, GIF, SWF, HTML
   * Tamaño máximo del archivo: 2,2 MB
   * Dimension: 300 x 250
 

## Anuncios en pantalla nativos

Cada anuncio puede incluir una imagen fija o un GIF en movimiento (párrafo cinematográfico).

### Pantallas compatibles

Los anuncios se entregan de forma predeterminada en dispositivos de escritorio y móviles. La segmentación por dispositivo está disponible para ajustar la entrega.

### Recursos necesarios para todos los formatos nativos en la fuente

#### Recurso de imagen

**Resolución:** Mínimo de 600 x 600 píxeles; Mínimo recomendado de 1200 x 627 px

**Tipo de archivo:** JPEG (imagen de anuncio de imagen o imagen de portada de anuncio de vídeo), GIF (cinemograma)

**Tamaño del archivo:** Menos de 1 MB (la imagen debe estar libre de texto).

#### Logotipo del anunciante

**Resolución:** Mínimo 80x80px; Mínimo recomendado de 300 x 300 píxeles

**Tipo de archivo:** JPEG o PNG.

**Relación de aspecto:**  Relación 1x1

>[!NOTE]
>
>En función de la imagen sobre la que se superponga, elija entre recursos de logotipo claros u oscuros.

#### Texto/Copiar

**Titular:** máximo 200 caracteres; 25 caracteres recomendados

**Pie de ilustración:** máximo 200 caracteres; Se recomiendan 100 caracteres

**Patrocinado Por:** máximo 200 caracteres; Se recomiendan 30 caracteres

**Llamada a acción (solo MoPub):** Máximo de 15 caracteres

>[!NOTE]
>
>El editor define el diseño final durante la ejecución. Si una publicidad supera el recuento de caracteres recomendado, es posible que algunos proveedores de inventario no la entreguen, o que el editor o el SSP trunquen el texto.

#### Dirección URL de la página de aterrizaje

Dirección URL de pulsaciones con rastreadores de clics opcionales.

Requisitos para rastreadores de clics:

* Píxeles de seguimiento de impresión de terceros: Solo formato de URL de imagen 1x1

* Seguimiento de JavaScript de visualizaciones: Sólo compatible con IAS; Imágenes 1x1 solo en formato JS.append

* Píxeles de seguimiento de clics de terceros: Debe redirigir a la página de aterrizaje incrustada en la dirección URL (redireccionamiento HTTP 302)

* No se admiten rastreadores de clics de la plataforma de administración de datos (DMP) con 200 o más respuestas.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de publicidad](ad-about.md)
>* [Crear una sola publicidad](ad-create.md)
>* [Crear varias publicidades de terceros](ad-create-multiple.md)
>* [Editar una publicidad](ad-edit.md)

