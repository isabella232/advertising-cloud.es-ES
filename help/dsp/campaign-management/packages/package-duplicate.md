---
title: Duplicar un paquete
description: Aprenda a duplicar un paquete.
feature: Packages
exl-id: 4c37883f-5feb-4513-9573-ed4e32606132
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Duplicar un paquete

Duplique un paquete para crear un paquete con una configuración similar. Puede:

* Duplique el paquete dentro del anunciante y la campaña originales o dentro de diferentes
* Si lo desea, duplique las ubicaciones dentro del paquete
* (Para paquetes duplicados dentro de las campañas originales) Opcionalmente, duplique los píxeles de evento de nivel de ubicación y anuncios originales
* Modificación de las fechas de vuelo del nuevo paquete

Consulte &quot;[Novedades no duplicadas](#package-not-duplicated)&quot; para obtener una lista de las configuraciones de ubicación que no están duplicadas.

1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.
1. Haga clic en el nombre de la campaña para abrir la vista [!UICONTROL Packages].
1. Junto al nombre del paquete, haga clic en **[!UICONTROL ...]>[!UICONTROL Duplicate]**.
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
* Ubicaciones predeterminadas para ofertas y ubicaciones garantizadas mediante programación (PG) para ofertas [!UICONTROL Simple Ad Serving]
* (Si copia colocaciones en otra campaña):
   * Segmentos geográficos
   * Píxeles de evento
   * Publicidades
   * Segmentos [!DNL DoubleVerify Authentic Brand Safety] de nivel de ubicación (que anulan los segmentos de nivel de anunciante)

>[!MORELIKETHIS]
>
>* [Acerca de la administración de paquetes](package-about.md)
>* [Creación de un paquete](package-create.md)
>* [Editar un paquete](package-edit.md)
>* [Configuración de paquetes](package-settings.md)

