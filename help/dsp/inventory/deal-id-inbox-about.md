---
title: Acerca de [!UICONTROL Deal ID Inbox]
description: Obtenga información sobre [!UICONTROL Deal ID inbox] , que le permite aceptar ofertas privadas que ya ha negociado con editores en [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] (anteriormente [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 2539d9b8ec7de7202dd6c3400dda85aa133853e3
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Acerca de [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] le permite configurar rápidamente ofertas que Advertising Cloud DSP ha importado de editores a través de plataformas de suministro (SSP) para que no tenga que configurar cada oferta manualmente. Puede aceptar los acuerdos de inventario privado garantizados y no garantizados que ya ha negociado con editores en [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anteriormente conocido como [!DNL AdX]) y [!DNL Magnite DV+] (anteriormente [!DNL Rubicon]) de [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising Cloud DSP es el primer DSP que se integra con la variable [!DNL FreeWheel] API.

En el [!UICONTROL Deal ID inbox], puede ver los detalles de la oferta tal como los ve el editor, acelerar la configuración de la oferta y evitar errores de entrada manuales.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP actualiza automáticamente todos los detalles de la oferta diariamente a las 4:30 EST. También actualiza todas las [!DNL FreeWheel] ofertas y actualizaciones de ofertas existentes de [!DNL Google] y [!DNL Magnite DV+] cada hora. También puede actualizar manualmente los detalles de la oferta para rellenar nuevas ofertas en cualquier momento.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Para acuerdos garantizados mediante programación, [!DNL Google Authorized Buyers], debe entregar al menos el 90 % de su presupuesto o su cuenta perderá acceso a [!DNL Google] ofertas de [!UICONTROL Deal ID inbox].

## Implementación de [!UICONTROL Deal ID Inbox]

Para recibir sus ofertas en el [!UICONTROL Deal ID inbox], las cuentas de SSP deben asignar la cuenta de DSP de su organización a su cuenta de SSP. DSP compartirá los nombres de las cuentas de la organización con los SSP pertinentes. Póngase en contacto con su [!DNL Adobe] administrador de cuentas para obtener instrucciones.

Durante las negociaciones del acuerdo, indique al editor que envíe el acuerdo a su comprador en lugar de a la cuenta DSP principal. El identificador de la operación puede ser un nombre o un ID, según el SSP.

## Acciones que puedes llevar a cabo en tus acuerdos

* **Revisar ofertas** para verificar que la SSP ha enviado el editor, las fechas de vuelo, el CPM y otros detalles de acuerdo correctos. Si el editor ha cometido un error, póngase en contacto con ellos fuera de DSP para que puedan corregir y volver a enviar el acuerdo.

* **Aceptar ofertas** después de la revisión, y ya no aparecerán en la variable [!UICONTROL Deal ID inbox]. Las ofertas aceptadas se enumeran en [!UICONTROL Inventory] > [!UICONTROL Deals] y están listos para dirigirse a las ubicaciones de los anunciantes.

* **Omitir ofertas** que no son necesarios o no son solicitados. Las ofertas ignoradas se mueven al [!UICONTROL Ignored Deals] dentro de la pestaña [!UICONTROL Deal ID inbox], que sirve como archivo. DSP alerta a los SSP y a los editores cuando ignora una oferta.

* **Modificar detalles para ofertas ya aceptadas** from [!UICONTROL Inventory] > [!UICONTROL Deals] (no en la variable [!UICONTROL Deal ID inbox]). Del mismo modo, cuando los editores envían cambios a ofertas, los anunciantes son responsables de implementar dichos cambios en [!UICONTROL Inventory] > [!UICONTROL Deals] porque la variable [!UICONTROL Deal ID inbox] no sincroniza los cambios de los SSP después de configurar las ofertas.

## ¿Qué tipos de acuerdos no se pueden aceptar?

Cuando una oferta no incluye un ![Accept](/help/dsp/assets/accept.png) icono o [!UICONTROL Accept] , no puede aceptarlo desde el [!UICONTROL Deal ID inbox]. En su lugar, puede [crear manualmente los detalles del ID de acuerdo](/help/dsp/inventory/deal-id-create.md).

No puede aceptar los siguientes tipos de ofertas:

* [!DNL Google] ofertas que no están en USD.

* [!DNL Magnite DV+] ofertas que no están en USD

* [!DNL FreeWheel] ofertas que no están en la moneda de su cuenta.

* Ofertas que tienen una fecha de finalización anterior a hoy.

* Antiguo [!DNL Magnite DV+] ofertas etiquetadas como &quot;varios tipos de medios&quot;.

Los detalles del acuerdo incluyen la razón por la que el acuerdo no está disponible para aceptar.

>[!MORELIKETHIS]
>
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Descripción general de las funciones de inventario](inventory-overview.md)

