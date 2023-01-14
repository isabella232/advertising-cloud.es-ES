---
title: Duplicar un paquete
description: Aprenda a duplicar un paquete.
feature: DSP Packages
exl-id: 4c37883f-5feb-4513-9573-ed4e32606132
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Duplicar un paquete

Duplique un paquete para crear un paquete con una configuración similar. Puede:

* Duplique el paquete dentro del anunciante y la campaña originales o dentro de diferentes
* Si lo desea, duplique las ubicaciones dentro del paquete
* (Para paquetes duplicados dentro de las campañas originales) Opcionalmente, duplique los píxeles de evento de nivel de ubicación y anuncios originales
* Modificación de las fechas de vuelo del nuevo paquete

Consulte &quot;[Novedades no duplicadas](#package-not-duplicated)&quot; para obtener una lista de los ajustes de ubicación que no están duplicados.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.

1. Haga clic en el nombre de la campaña para abrir el [!UICONTROL Packages] vista.

1. Junto al nombre del paquete, haga clic en  **[!UICONTROL ...]>[!UICONTROL Duplicate]**.

1. Especifique la nueva configuración del paquete:

   1. Introduzca el nuevo nombre del paquete.

   1. (Opcional) Cambie la configuración predeterminada.

      De forma predeterminada:

      * El nuevo paquete se asigna al anunciante y la campaña originales.

      * El nuevo paquete se activa en el día actual.<!-- and the flight continues for NN  days. -->

      * Las ubicaciones dentro del paquete original se copian en el nuevo paquete.

      * Los anuncios y los píxeles de evento de nivel de ubicación no se copian en el nuevo paquete.

1. Haga clic **[!UICONTROL Submit]**.

## Novedades no duplicadas {#package-not-duplicated}

Todos los ajustes de las ubicaciones originales se duplican, excepto:

* Configuración del experimento
* (Si cambia las fechas de vuelo) Programación de anuncios personalizada
* (Si no adjunta anuncios) Ponderación y programación de anuncios personalizados
* Ubicaciones predeterminadas para ofertas y ubicaciones garantizadas mediante programación para [!UICONTROL Simple Ad Serving] ofertas
* (Si copia colocaciones en otra campaña):
   * Segmentos geográficos
   * Píxeles de evento
   * Publicidades
   * Nivel de ubicación [!DNL DoubleVerify Authentic Brand Safety] segmentos (que anulan los segmentos de nivel de anunciante)

>[!MORELIKETHIS]
>
>* [Acerca de la administración de paquetes](package-about.md)
>* [Creación de un paquete](package-create.md)
>* [Editar un paquete](package-edit.md)
>* [Ver el registro de cambios de un paquete](package-change-log.md)
>* [Configuración de paquetes](package-settings.md)

