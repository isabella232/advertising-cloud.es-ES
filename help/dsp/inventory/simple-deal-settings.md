---
title: '"[!UICONTROL Simple Ad Serving] Configuración de ofertas"'
description: Obtenga información sobre la configuración disponible para [!UICONTROL Simple Ad Serving] ofertas.
feature: DSP Simple Ad Serving
source-git-commit: 2c94b6c02b4e24878639dd9edbc0455e1751f679
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Configuración de ofertas

## Nuevo [!UICONTROL Simple Ad Serving] Ofertas

### [!UICONTROL Select Ad Source]

| Parámetro | Descripción |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Tipo de medio para esta operación: *[!UICONTROL Video],* *[!UICONTROL Display],* o *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | Nombre del publicador que vende este inventario. Busque un publicador introduciendo al menos los dos primeros caracteres en el nombre. Para agregar un publicador que no aparece en la lista, póngase en contacto con su [!DNL Adobe] equipo de la cuenta. |
| **[!UICONTROL Advertiser]** | Un solo anunciante de la cuenta que puede acceder a esta oferta. Seleccione también la campaña y (opcionalmente) el paquete en el que está disponible la oferta. |
| **[!UICONTROL Media Quality Assessment?]** | (Algunos usuarios) Habilita la publicidad para que se ejecute en otra DSP para verificación de terceros. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | La única opción es *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Solo ofertas nuevas) Si:<ul><li>*[!UICONTROL Create New]:* Para crear una publicidad para esta oferta.</li><li>*[!UICONTROL Select Ads]:* Para usar una publicidad existente para esta oferta.</li></ul> |
| **[!UICONTROL Ad Type]** | El tipo de anuncio para esta oferta. Si va a crear nuevas publicidades para la oferta, incluya el tamaño o la duración de la publicidad, según se solicite. Las opciones disponibles varían según el tipo de medio. |

{style=&quot;table-layout:auto&quot;}

### [!UICONTROL Select Ad(s)]

(Cuando está usando anuncios existentes) Las publicidades que se incluirán en la oferta. Seleccione la casilla de verificación situada junto a cada publicidad que desee incluir.

### [!UICONTROL Select & Upload [Media Type]]

(Solo anuncios nuevos) Screens para crear una nueva [anuncio de origen](/help/dsp/campaign-management/ads/ad-create.md) o [anuncio de terceros](/help/dsp/campaign-management/ads/ad-create-third-party.md).

### [!UICONTROL Feed Details]

| Parámetro | Descripción |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | El coste por mil impresiones (CPM), tal como se refleja en la tarjeta de tarifa de su contrato. Póngase en contacto con su [!DNL Adobe] equipo de cuenta para este valor. <br><br>Especifique también la moneda para la oferta. Todos los usuarios pueden seleccionar USD o, si el SSP admite monedas adicionales, la moneda de la cuenta de DSP. |
| **[!UICONTROL Third Party Billed Fees]** | (Opcional) Una tasa estática de terceros que se rastreará como un costo no facturable, y la moneda para el acuerdo.<br><br>Todos los usuarios pueden seleccionar USD o, si el SSP admite monedas adicionales, la moneda de la cuenta de DSP. **NOTA:** Las tasas facturables se reflejan en la [!UICONTROL Net CPM] métrica. |
| **[!UICONTROL Third Party Fee Description]** | (Opcional) Descripción de las tarifas de terceros. |
| **[!UICONTROL Flight Dates]** | Las fechas de inicio y finalización del tráfico que utiliza esta oferta. Las fechas de vuelo deben incluirse en las fechas de vuelo de la campaña. Las etiquetas publicitarias solo devolverán una respuesta durante el vuelo especificado.<br><br> Se recomienda crear una campaña de servicio de publicidad sencilla independiente de un año de duración y crear píxeles de seguimiento dentro de ella. |
| **[!UICONTROL Impressions]** | (Opcional) El número estimado de impresiones que espera ejecutar usando esta oferta. Este valor se utiliza únicamente con fines de seguimiento y para marcar cuándo se cumplen los objetivos de envío. el editor controla la entrega de publicidad real. La práctica recomendada es introducir un número elevado de impresiones para mantener la etiqueta activa dentro de DSP, de modo que se pueda renovar o ampliar si es necesario. |
| **[!UICONTROL Deal Name]** | El nombre del trato. Escriba un nombre o seleccione *[!UICONTROL Auto Generate Deal Name]* para permitir que DSP un nombre basado en los detalles de la oferta.<br><br>Ejemplo de nombre generado automáticamente: `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Solo lectura) Los anuncios que forman parte del acuerdo. Para editar una publicidad, haga clic en el nombre de la publicidad. Para eliminar una publicidad de la oferta, haga clic en **[!UICONTROL X]** junto al nombre del anuncio. |

{style=&quot;table-layout:auto&quot;}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [Acerca de [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Cree un [!UICONTROL Simple Ad Serving] Acuerdo](simple-deal-create.md)
>* [Ver píxeles de seguimiento de eventos para un [!UICONTROL Simple Ad Serving] Acuerdo](simple-deal-show-pixels.md)

