---
title: Ver los informes de diagnóstico de colocación
description: Aprenda a diagnosticar problemas con la configuración de la ubicación y el ritmo.
feature: Placements
exl-id: d64406b6-83b5-4ae7-984c-98610fc1ee40
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Ver los informes de diagnóstico de colocación

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Las siguientes herramientas pueden ayudarle a diagnosticar problemas con la configuración de la ubicación y el ritmo una vez que una campaña está activa:

* **[!UICONTROL Change Log]:** Muestra los cambios en la configuración de ubicación de claves, como el nombre, el estado y la oferta máxima. Cada entrada incluye la fecha y el nombre de usuario de la persona que realizó el cambio.
* **[!UICONTROL Ad Approvals]:** muestra si los proveedores de inventario aprobaron o rechazaron los anuncios. Si lo desea, puede cambiar el estado de cualquier publicidad (por ejemplo, poner en pausa una publicidad rechazada) o abrir la configuración de la publicidad.
* **[!UICONTROL Non Bids]:** Muestra por qué no DSP pujó en la ubicación.

1. Abra el informe Diagnósticos :
   1. Abra la configuración de ubicación:
      1. En el menú principal, haga clic en **[!UICONTROL Campaigns]**.
      1. Haga clic en el nombre de la campaña y, a continuación, haga clic en **[!UICONTROL Placements]**.
      1. Junto al nombre de la ubicación, haga clic en **[!UICONTROL ...]>[!UICONTROL Edit]**.
   1. En la esquina superior derecha, haga clic en ![Diagnósticos de ubicación](/help/dsp/assets/placement-diagnostics.png) o **[!UICONTROL Diagnostic]**.
1. Realice una de las siguientes acciones:
   * Para ver el registro de cambios:
      1. Haga clic **[!UICONTROL Change Log]**.
      1. (Opcional) Filtre los resultados del informe:
         * En el menú de fecha, cambie el periodo del informe de los últimos 14 días predeterminados a otro periodo (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* o *[!UICONTROL Last 1 year]*).
         * En el menú de la izquierda, filtre el informe por un nombre de usuario específico.
         * En el menú de la derecha, filtre el informe por una configuración de ubicación específica.
   * Para ver el estado de las aprobaciones de publicidad:
      1. En la esquina superior derecha, haga clic en **[!UICONTROL Ad Approvals]**.
      1. (Opcional) Para pausar o activar la publicidad, haga clic en el conmutador de estado (![Conmutador de estado](/help/dsp/assets/status-switch.png)) en la columna Anuncio).
      1. (Opcional) Para abrir la configuración de un anuncio, haga clic en **[!UICONTROL View Ad]** junto al anuncio.
   * Para ver por qué DSP no pujó en la ubicación:
      1. En la esquina superior derecha, haga clic en **[!UICONTROL Non Bids]**.
      1. (Opcional) Para cambiar el intervalo de fechas, haga clic en el campo de fecha y seleccione otra fecha o intervalo de fechas.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Acerca de los informes en la plataforma](campaign-reports-about.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)

