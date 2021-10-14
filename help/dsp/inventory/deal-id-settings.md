---
title: Configuración manual del ID de trato
description: Consulte las descripciones de la configuración para los ID de acuerdos introducidos manualmente.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: 5f39608155f9237fb6d69a7b31c007d1b8d0306f
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Configuración manual del ID de trato

| Sección | Parámetro | Descripción | Requerido | Editable |
|---------|-----------|-------------|----------|----------|
| [Detalles del trato] | [!UICONTROL Deal name] | El nombre para identificar su [!UICONTROL Deal ID] en Advertising Cloud DSP. Introduzca un nombre o seleccione [!UICONTROL Auto-name] para permitir que Advertising Cloud genere un nombre basado en los detalles de la oferta.<br><br>Ejemplo de nombre generado automáticamente:  [!DNL *DEAL_ID*  - ID de acuerdo - Fijo garantizado - USD - 5 - 24Cocina - Privado] | Sí | Sí |
|  | [!UICONTROL External deal ID] | ID utilizado por el editor y la plataforma compartida única para identificar este acuerdo. | Sí | No |
|  | [!UICONTROL Publisher] | Nombre del publicador que vende este inventario. | Sí | No |
|  | [!UICONTROL SSP] | La plataforma de suministro (SSP) a través de la cual se ejecutará esta operación. | Sí | No |
|  | [!UICONTROL Media type] | El tipo de medios que comprarán a través de este acuerdo: [!UICONTROL Desktop video], [!UICONTROL Mobile video], [!UICONTROL Connected TV], [!UICONTROL Display] o [!UICONTROL Audio]. Las opciones varían según el SSP.<br><br> Si la oferta permite varios tipos de medios, seleccione el tipo de medio para la ubicación predeterminada al crear la oferta. Posteriormente, puede seleccionar otro tipo de medio para crear una nueva ubicación con el tipo de medio adicional.<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Sí | No |
|  | [!UICONTROL Deal type] | La estructura de asignación y precios de acuerdo:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Usted y el editor no se han comprometido con un número fijo de envíos de impresión. El acuerdo especifica el precio mínimo para el inventario, aunque el CPM puede fluctuar y aumentar dependiendo de las condiciones del mercado.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Usted y el editor no se han comprometido con un número fijo de envíos de impresión. El precio es a un tipo fijo negociado.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Usted y el editor han acordado un número predefinido de impresiones, segmentación, fechas de vuelo y precio fijo.<br><br><b>Nota:</b> Las ofertas garantizadas requieren fechas de vuelo y un número específico de impresiones en la  [!UICONTROL Tracking] sección. También tendrá que crear una colocación garantizada mediante programación (PG) predeterminada para la oferta y, opcionalmente, puede utilizar la oferta para otras ubicaciones.</li></ul> | Sí | No |
|  | [!UICONTROL CPM] | El coste negociado por mil impresiones (CPM). | Sí | Sí |
|  | [Moneda] | La moneda para el acuerdo.<br><br>Todas las SSP aceptan ofertas en USD. Cuando el SSP acepta la moneda de su cuenta de DSP, dicha moneda también está disponible. | Sí | No |
|  | [!UICONTROL Billing method] | Todos los ID de acuerdo están financiados y facturados por [!DNL Adobe]. Advertising Cloud pagará a todos los proveedores de medios disponibles según el uso, administrará las discrepancias con los proveedores y enviará una factura consolidada a la cuenta. Esta opción incurre en cargos adicionales, tal como se describe en la tarjeta de tarifas de la cuenta. | Sí | No |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | La dirección de correo electrónico de la cuenta de usuario que puede acceder a la oferta. | No | Sí |
|  | [!UICONTROL Advertisers that can access this deal] | Los anunciantes específicos de la cuenta que pueden acceder a esta oferta.<br><br><b>Nota:</b> Puede compartir la oferta con los anunciantes en cuentas adicionales desde la  [!UICONTROL Deals] vista. En la fila de acuerdo, haga clic en **[!UICONTROL #]**, en **[!UICONTROL share]** y, a continuación, comparta la operación con una dirección de correo electrónico. | Sí | Sí |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Las fechas de inicio y finalización del tráfico que utiliza esta oferta. Estas fechas son solo para fines de seguimiento y no afectan al envío de anuncios.<br><br><b>Sugerencia:</b> En la  [!UICONTROL Inventory] vista  [!UICONTROL Deals] > , la  [!UICONTROL Pacing & Budget] columna mostrará cómo se está llevando a cabo la operación hasta el objetivo especificado de fecha de vuelo e impresión. Si la entrega está a un ritmo inferior o superior, póngase en contacto con su editor para ajustar el volumen que envía a través de la oferta. | Ofertas garantizadas: Sí<br>Ofertas no garantizadas: No | Sí |
|  | [!UICONTROL Impressions] | (Opcional para ofertas no garantizadas) El número estimado de impresiones que espera ejecutar usando esta oferta. Este valor solo tiene fines de seguimiento; el editor controla el envío de anuncios. | Ofertas garantizadas: Sí<br>Ofertas no garantizadas: No | Sí |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Crear manualmente detalles de ID de acuerdo](deal-id-create.md)
>* [Socios de SSP](ssp-partners.md)

<!-- >* [About Private Inventory](private-inventory-about.md) -->
