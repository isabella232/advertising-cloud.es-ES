---
title: Acerca de la administración de publicidad en Advertising Cloud DSP
description: Obtenga información sobre la administración de publicidades.
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: ff0e153344f8245ff217cc8b2b276184dd7422b5
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---

# Acerca de la administración de publicidad en Advertising Cloud DSP

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP admite la entrega de anuncios a través de etiquetas de servicios de publicidad de terceros (como Google, Flashtalk o Sizmek) para varios tipos de anuncios y la carga directa de recursos para anuncios en pantalla nativos. Puede cargar etiquetas de terceros de forma individual o masiva. Las cargas masivas utilizan hojas de etiquetas de socios o una plantilla de etiquetas masiva.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Una vez configuradas las publicidades, deberá adjuntarlas a una ubicación, que incluye parámetros de objetivo (como la ubicación geográfica, la audiencia, el dispositivo y la segmentación de inventario) que controlan el envío de la campaña. Puede adjuntar una sola publicidad a una o varias ubicaciones.

## Tipos de anuncios disponibles {#ad-types}

Todos los siguientes tipos de anuncios están disponibles en Advertising Cloud DSP. Para obtener especificaciones completas para cada tipo de anuncio, consulte la [Especificaciones de la publicidad](/help/dsp/assets/ad-specs.pdf).

* **Anuncios de audio (solo de terceros)**: Los anuncios de audio se reproducen entre el contenido en sitios de editores digitales y se pueden ejecutar de forma independiente como archivos de audio o junto con banners complementarios. El audio se utiliza mejor para aumentar la conciencia de la marca y captar la atención de las audiencias en uso. Los indicadores de rendimiento clave para el audio incluyen [!UICONTROL Completion Rate] y [!UICONTROL Cost per Completion].

* **Mostrar anuncios (solo de terceros)**: Los anuncios en pantalla son imágenes animadas o estáticas que se muestran en navegadores web o en aplicaciones. Al hacer clic en la unidad de publicidad, el usuario se dirige a un sitio o micrositio con marca. La visualización es mejor utilizada para impulsar CPM eficientes, aumentar la asociación de mensajes, añadir puntos de contacto de productos o marcas adicionales y dirigir a los usuarios hacia abajo en el canal de compras. Los indicadores de rendimiento clave para la visualización incluyen [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions]y [!UICONTROL Cost per Conversion]. DSP admite una amplia variedad de tamaños de anuncios de tipo titular.

* **Mobile Ads (solo de terceros)**: Los anuncios de Mobile pueden estar en formato de vídeo pre-roll (VAST, MRAID) o de visualización estándar. El vídeo pre-roll de Mobile puede reproducirse automáticamente o pulsarse para reproducirse y se utiliza mejor para llegar a los visualizadores en todas las pantallas. La visualización estándar de Mobile es una imagen estática que se muestra en navegadores web móviles o en aplicaciones y que se utiliza mejor para complementar las compras de vídeo digital, impulsar la asociación de mensajes y añadir puntos de contacto de productos o marcas adicionales. Los anuncios de Mobile también pueden funcionar como adquisiciones a pantalla completa o como intersticiales móviles, que son anuncios móviles de pantalla completa y gran impacto que se utilizan mejor para desarrollar la diferenciación de la marca para audiencias móviles y dirigir conversiones.

* **Anuncios en pantalla nativos (solo de origen)**: Los anuncios nativos se admiten en formato de visualización estándar. Las publicidades nativas incluyen un titular o título, descripción, logotipo e imagen. Los elementos publicitarios se combinan y procesan para que coincidan con el estilo de página del editor, de modo que el anuncio se funda con el contenido orgánico del editor y aumente la participación. Los nativos se utilizan mejor para la diferenciación de la marca y para impulsar la visualización de audiencia y las tasas de participación con una publicidad compatible con el visor. Los indicadores clave de rendimiento incluyen [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions]y [!UICONTROL Cost Per Conversion].

* **Anuncios previos a la emisión (solo de terceros)**: Los anuncios previos a la emisión (VAST y VPAID) se muestran antes del contenido de vídeo premium y ofrecen una experiencia de visualización inmersiva y atractiva. El vídeo previo a la emisión puede ser interactivo, contener funciones multimedia enriquecidas e incluir superposiciones, rollovers y llamadas a la acción. Los indicadores de rendimiento clave para los anuncios de vídeo pre-roll incluyen [!UICONTROL Video Completion Rate] y [!UICONTROL Viewability Rate].

* **Anuncios de TV conectados (solo de terceros)**: Los anuncios de TV conectados se muestran antes y durante el contenido de vídeo de TV premium. Todo el inventario de TV conectado se ejecuta en dispositivos de TV, lo que significa que el vídeo se reproduce automáticamente en un entorno de pantalla completa y retrospectiva que los espectadores no pueden omitir. La TV conectada es el formato de vídeo digital más cercano a los anuncios de TV. Los indicadores de rendimiento clave para la TV conectada incluyen [!UICONTROL Completion Rate].

## Aprobaciones de anuncios de Advertising Cloud DSP

Cuando cree una publicidad, Advertising Cloud DSP la revisa para categorías delicadas, hace clic en la funcionalidad URL y obtiene una vista previa de la renderización.

Inicialmente, verá un punto rojo en la [!UICONTROL Status] para abrir el Navegador. El proceso de revisión suele tardar entre 24 y 48 horas. Sin embargo, un anuncio roto puede tener un estado pendiente durante más de 48 horas, por lo que tiene tiempo para corregir errores antes de que se rechace el anuncio. Los anuncios rechazados incluyen un motivo del rechazo.

Cuando DSP apruebe una publicidad, verá un punto verde en la columna Estado .

![indicador de aprobación en [!UICONTROL Status] column](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Su publicidad solo se publicará si tanto DSP como la SSP han aprobado el elemento creativo. Cada SSP tiene sus propios requisitos y procesos de aprobación.

>[!MORELIKETHIS]
>
>* [Crear una sola publicidad](ad-create.md)
>* [Crear varias publicidades de terceros](ad-create-multiple.md)
>* [Especificaciones de la publicidad](/help/dsp/assets/ad-specs.pdf)

