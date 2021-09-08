---
title: Acerca de la administración de publicidad en Advertising Cloud DSP
description: Obtenga información sobre la administración de publicidades.
feature: Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Acerca de la administración de publicidad en Advertising Cloud DSP

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP ofrece dos maneras de servir sus publicidades:

* Advertising Cloud DSP ofrecerá sus publicidades de forma gratuita cuando cargue sus propios recursos (como banners de visualización, recursos de vídeo, archivos de audio o direcciones URL) directamente a DSP. Para los recursos DSP, tiene acceso a funciones adicionales, como superposiciones.

* Si utiliza un servidor de publicidad de terceros (como Google, Flashtalk o Sizmek), puede cargar las etiquetas de servicio de publicidad de terceros a DSP individual o en lote. La función de carga masiva requiere que: a) cargue hojas de etiquetas DoubleClick y Flashtalk o b) descargue una plantilla, introduzca las etiquetas en la plantilla y, a continuación, vuelva a cargar la plantilla.<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Una vez configuradas las publicidades, deberá adjuntarlas a una ubicación, que incluye parámetros de objetivo (como la ubicación geográfica, la audiencia, el dispositivo y la segmentación de inventario) que controlan el envío de la campaña. Puede adjuntar una sola publicidad a una o varias ubicaciones.

## Tipos de anuncios disponibles

* Audio
* Televisión conectada
* Mostrar
* Móvil
* Nativo
* Anuncio

Para obtener más información sobre estos tipos de anuncios, consulte [Tipos de anuncios disponibles](ad-types.md) y las [Especificaciones de anuncios](/help/dsp/assets/ad-specs.pdf) completas.

## Características de los anuncios especiales

Las siguientes funciones solo están disponibles para los anuncios DSP.

### Banners Companion

Los banners adjuntos se proporcionan junto con [anuncios previos a la emisión](ad-settings-pre-roll.md) o (con algunos editores) [anuncios de audio](ad-settings-audio.md) y pueden ayudar a reforzar la asociación de marca y mensaje.

>[!NOTE]
>
>* No todos los editores permiten banners complementarios. Los editores que sí permiten banners complementarios no garantizan impresiones de banners complementarios.
>* Es posible que los banners adjuntos de etiquetas de publicidad de terceros no siempre estén disponibles para la vista previa.


Puede cargar su propio recurso de banner complementario o cargar un iFrame de terceros o una etiqueta de banner de secuencia de comandos de un socio de servicio de publicidad de terceros certificado.

### Superposiciones

Las superposiciones ayudan a lograr la promoción de la marca persistente en todo el vídeo y pueden generar clics adicionales. La función de superposición está disponible para [anuncios previos interactivos](ad-settings-pre-roll.md) y para [anuncios móviles en formatos interactivos y de toque para reproducir](ad-settings-mobile.md).

Consulte las [Prácticas recomendadas para diseñar superposiciones](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

### Teasers

Un teaser es una imagen llamativa que separa al espectador de la reproducción de un anuncio. Los teasers solo se aplican a los formatos de anuncios de toque para reproducción móviles.

## Aprobaciones de anuncios de Advertising Cloud DSP

Cuando cree una publicidad, Advertising Cloud DSP la revisa para categorías delicadas, hace clic en la funcionalidad URL y obtiene una vista previa de la renderización.

Inicialmente, verá un punto rojo en la columna [!UICONTROL Status]. El proceso de revisión suele tardar entre 24 y 48 horas. Sin embargo, un anuncio roto puede tener un estado pendiente durante más de 48 horas, por lo que tiene tiempo para corregir errores antes de que se rechace el anuncio. Los anuncios rechazados incluyen un motivo del rechazo.

Cuando DSP apruebe una publicidad, verá un punto verde en la columna Estado .

![indicador de aprobación en la  [!UICONTROL Status] columna](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Su publicidad solo se publicará si tanto DSP como la SSP han aprobado el elemento creativo. Cada SSP tiene sus propios requisitos y procesos de aprobación.

>[!MORELIKETHIS]
>
>* [Crear una publicidad](ad-create.md)
>* [Crear varias publicidades de terceros](ad-create-third-party.md)
>* [Tipos de anuncios disponibles](ad-types.md)
>* [Especificaciones de la publicidad](/help/dsp/assets/ad-specs.pdf)

