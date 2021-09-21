---
title: Duplicar ubicaciones
description: Obtenga información sobre cómo duplicar una o más ubicaciones.
feature: DSP Placements
exl-id: d22a61a8-4f1b-41ee-b4fb-3124bec81a2f
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# Duplicar ubicaciones

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique una o más ubicaciones para crear ubicaciones con configuraciones similares. Puede:

* Realización de varios duplicados de ubicaciones
* Duplicar ubicaciones dentro de los anunciantes y campañas originales o dentro de diferentes
* (Para ubicaciones duplicadas dentro de las campañas originales) Si lo desea, duplique las publicidades originales
* Modificación del estado y las fechas de vuelo de las nuevas ubicaciones

Consulte &quot;[Novedades no duplicadas](#placement-not-duplicated)&quot; para obtener una lista de las configuraciones de ubicación que no están duplicadas.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.
1. Haga clic en el nombre de la campaña.
1. En el submenú, haga clic en **[!UICONTROL Placements]**.
1. Realice una de las siguientes acciones:
   * Para duplicar una ubicación, haga clic en **[!UICONTROL ...]>[!UICONTROL Duplicate]** junto al nombre del paquete.
   * Para duplicar varias ubicaciones:
      1. Seleccione la casilla de verificación situada junto a cada ubicación que desee duplicar.
      1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Duplicate]**.
1. Especifique la nueva configuración de ubicación:
   1. (Colocaciones únicas) Introduzca el nuevo nombre de la colocación.
   1. En el menú **[!UICONTROL Choose Package (Required)]**, seleccione el paquete principal o **[!UICONTROL No package]*.
   1. (Opcional) Cambie la configuración predeterminada.

   La configuración se aplica a todas las ubicaciones seleccionadas.

   De forma predeterminada, las nuevas ubicaciones son para el tipo de anuncio original, se asignan a los anunciantes y campañas originales, tienen programas de vuelo que comienzan el día actual, están en pausa y no incluyen los anuncios originales.

   Cuando se crean varias ubicaciones, los nuevos nombres de colocación se añaden con un número, en secuencia, mediante la convención &lt;*original_placement_name #N*>, como &quot;Mi ubicación #2&quot;.

1. Haga clic **[!UICONTROL Submit]**.

## Novedades no duplicadas {#placement-not-duplicated}

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
>* [Acerca de la administración de ubicaciones](placement-about.md)
>* [Crear una colocación](placement-create.md)
>* [Editar una colocación](placement-edit.md)
>* [Configuración de colocación](placement-settings.md)

