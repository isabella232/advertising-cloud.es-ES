---
title: Duplicar una campaña
description: Obtenga información sobre cómo duplicar una campaña.
feature: DSP Campaigns
exl-id: 2bb4030d-22b0-4a16-aeed-35f64a19df6a
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Duplicar una campaña

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique una campaña para crear una nueva campaña con una configuración similar. Puede:

* Duplique la campaña para el anunciante original o para otra
* Opcionalmente, duplique los paquetes y las ubicaciones originales
* Modificación de las fechas de vuelo de la nueva campaña

Consulte &quot;[Novedades no duplicadas](#campaign-not-duplicated)&quot; para obtener una lista de las configuraciones de ubicación que no están duplicadas.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.
1. Junto al nombre de la campaña, haga clic en **... >[!UICONTROL Duplicate]**.
1. Especifique la nueva configuración de campaña:
   1. Introduzca el nuevo nombre de la campaña y la fecha de finalización del vuelo.
   1. (Opcional) Cambie la configuración predeterminada.

      De forma predeterminada, la nueva campaña se asigna al anunciante original, tiene un programa de vuelo que comienza el día actual e incluye los paquetes y las ubicaciones originales.

1. Haga clic **[!UICONTROL Submit]**.

## Novedades no duplicadas {#campaign-not-duplicated}

Todos los ajustes de las ubicaciones originales se duplican, excepto:

* Configuración del experimento
* (Si cambia las fechas de vuelo) Programación de anuncios personalizada
* (Si no adjunta anuncios) Ponderación y programación de anuncios personalizados
* Ubicaciones predeterminadas para ofertas y ubicaciones garantizadas mediante programación (PG) para ofertas [!UICONTROL Simple Ad Serving]
* (Si copia colocaciones en otra campaña):
   * Segmentos geográficos
   * Píxeles de evento
   * Publicidades
   * Segmentos [!DNL DoubleVerify Authentic Brand Safety] de nivel de ubicación (que anulan los segmentos de nivel de anunciante)

>[!MORELIKETHIS]
>
>* [Acerca de la administración de campañas](campaign-about.md)
>* [Creación de una campaña](campaign-create.md)
>* [Editar una campaña](campaign-edit.md)
>* [Configuración de campaña](campaign-settings.md)

