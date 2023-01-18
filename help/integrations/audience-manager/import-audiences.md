---
title: Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios
description: Obtenga información sobre cómo importar su [!DNL Adobe] audiencias en Advertising DSP y Buscar con Adobe Audience Manager
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios

DSP publicitarias y [!DNL Advertising Search] puede cada uno extraer metadatos, datos de jerarquía y datos de audiencia únicos para todos los datos de anunciantes o agencias [!DNL Adobe] audiencias<!-- segments or audiences? Standardize terms per AAM's docs -->. Esto incluye datos para:

* Segmentos de Adobe Audience Manager

* Segmentos de Adobe Analytics que se publican en Adobe Experience Cloud

* Segmentos que se crean en Adobe Experience Cloud usando la variable [!DNL People core service]

* Segmentos que se crean en Adobe Experience Platform y se envían a Adobe de publicidad a través del Audience Manager

Para acceder a [!DNL Adobe] audiencias en DSP o [!DNL Creative], debe importar las audiencias en DSP. Para acceder a [!DNL Adobe] audiencias en [!DNL [!DNL Search]], debe importar las audiencias en [!DNL [!DNL Search]].

## Requisitos previos

* El anunciante debe implementar [el [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) versión 2.0 o superior. La variable [!DNL Identity Service] proporciona un identificador universal y persistente que identifica a los visitantes en todas las soluciones de Experience Cloud.

   La implementación incluye la adición de [!DNL Identity service] para cada página web en los sitios del anunciante.

* La organización debe ser [habilitado para servicios de Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) y tener un Experience Cloud [!DNL Organization ID] (antes denominado [!DNL IMS org ID]).

   La variable [!UICONTROL Organization ID] permite a las organizaciones con varios productos de Adobe Experience Cloud compartir datos entre algunos de los productos.

* (Anunciantes con [!DNL Analytics]) El anunciante debe [implementar [!DNL Analytics] using `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) versión 1.6.4 o superior.

* Los visitantes del sitio web del anunciante no incluyen un gran volumen de [!DNL Apple Safari] usuarios.

* (Recomendado cuando el anunciante utiliza tanto el Audience Manager como el [!DNL Analytics]) Para reducir las llamadas a cada página web, elimine el Audience Manager existente. [!DNL Data Integration Library] código para la recopilación de datos y habilitar el reenvío del lado del servidor para cada [!DNL Analytics] grupo de informes en su lugar. Para obtener más información, consulte &quot;[Resumen del reenvío del lado del servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (Recomendado) Para tasas de coincidencia más altas, envíe solo datos de sitios web de origen a Publicidad de Adobe. Si el anunciante aúna datos de terceros o datos sin conexión de un sistema de administración de la relación con los clientes, la fuga de datos puede reducir las tasas de coincidencia.

## Importar audiencias de Audience Manager a DSP

### Pasos para importar audiencias a DSP

La variable [!DNL Adobe] los equipos de operaciones de datos y cuentas realizarán los siguientes pasos.

1. La variable [!DNL Adobe] El equipo de la cuenta debe configurar el nivel del anunciante &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. La variable [!DNL Adobe] el equipo de la cuenta debe enviar una solicitud<!-- Submit a request as a JIRA task? --> al equipo de operaciones de datos<!-- implementation team? --> para importar los segmentos de Audience Manager de la organización mediante la integración de la API nativa de Advertising DSP.

### ¿Qué cambios provocan el Audience Manager?

La API de automáticamente:

* Crea dos destinos DSP en el Audience Manager:

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* Asigna los dos destinos a todos los segmentos del Audience Manager, lo que permite al Audience Manager compartir los segmentos con la cuenta del anunciante de DSP asociada al mismo Experience Cloud [!DNL Organization ID] para Audience Manager. <!-- Verify -->

   La organización puede, opcionalmente, eliminar segmentos innecesarios de los destinos dentro de Audience Manager.

* Agrega el siguiente píxel de sincronización de cookies de intercambio al contenedor de Audience Manager de la organización para mejorar el alcance de las campañas de clientes:

   * Adobe AdCloud: 411 (Esto viene de forma estándar y automática como parte de [!DNL Identity Service] versión 2.0. Organizaciones con [!DNL Identity Service] las versiones anteriores a 2.0 deben añadir este píxel a su contenedor de Audience Manager.

## Importar audiencias de Audience Manager a [!DNL Search]

### Pasos para importar audiencias a [!DNL Search]

[!DNL Adobe] el personal realizará la mayoría o todos los pasos siguientes.

1. La variable [!DNL Adobe] el equipo de la cuenta debe enviar una solicitud al equipo de operaciones de datos para configurar una integración entre [!DNL Search] y Audience Manager. Incluya los nombres de los segmentos de Audience Manager a los que desea exportar [!DNL Search].

1. En el Audience Manager, configure los destinos para [!DNL Search]:

   1. Cree dos nuevos destinos: `[!UICONTROL Adobe Media Optimizer (HTTP)]` y `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] es un nombre anterior para [!DNL Search].

   1. Especifique los segmentos para cada uno de los destinos.

      Con la variable [!UICONTROL Automatically map all current and future segments] , todos los segmentos se asignan y sincronizan diariamente.

      La variable [!UICONTROL Manually map segments] le permite asignar manualmente los segmentos para sincronizar con el destino del lote (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). No es necesario asignar ningún segmento manualmente al destino HTTP.

1. Within [!DNL Search], ya sea la variable [!DNL Search] el equipo de implementación o un usuario con la función de administrador de cliente de acceso directo deben iniciar la importación desde [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Debe introducir el Experience Cloud de la organización [!DNL Organization ID] ([!DNL IMS org ID]). El ID debe ser el mismo que el utilizado para la cuenta de Audience Manager de la organización.

### ¿Qué cambios provocan el Audience Manager?

La organización verá dos [!DNL Search] destinos en Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## Sincronización de datos

La importación inicial tarda unas 24 horas. Después de la importación inicial, los datos se sincronizan en tiempo real con un retraso de uno a dos segundos.

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].
 
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## Dónde encontrar los segmentos sincronizados

### En DSP

En DSP, los nombres de los segmentos están organizados por la taxonomía de Audience Manager y están disponibles con los recuentos de pertenencia a los segmentos correspondientes en:

* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): En el [!UICONTROL Adobe Segments] de la pestaña [!UICONTROL Audience Targeting] para obtener más información.

* En [configuración de audiencia](/help/dsp/audiences/audience-settings.md): En el [!UICONTROL Adobe Segments] pestaña .

### En Advertising Creative

En [!DNL Creative], los segmentos están disponibles en la configuración de experiencia para los nodos de destino.

### En [!DNL Advertising Search]

En [!DNL [!DNL Search]], los segmentos están disponibles cuando crea un [!DNL Google] audiencia que utiliza la variable [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; de [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Para cada [!DNL Google] audiencia que cree, [!DNL Google] proporciona el tamaño de la audiencia.

>[!MORELIKETHIS]
>
>* [Integraciones de publicidad de Adobe con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

