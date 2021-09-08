---
title: Acerca de [!UICONTROL Deal ID Inbox]
description: Obtenga información sobre la función [!UICONTROL Deal ID inbox], que le permite aceptar ofertas privadas que ya ha negociado con editores en [!DNL Google Authorized Buyers], [!DNL FreeWheel], and [!DNL Rubicon].
feature: Private Inventory, Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Acerca de [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] le permite configurar rápidamente ofertas que Advertising Cloud DSP ha importado de editores a través de plataformas de suministro (SSP) para que no tenga que configurar cada oferta manualmente. Puede aceptar los acuerdos de inventario privado garantizados y no garantizados que ya ha negociado con los editores en [!DNL Google Authorized Buyers] (anteriormente conocidos como [!DNL AdX]), [!DNL FreeWheel] y [!DNL Rubicon], desde [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising Cloud DSP es el primer DSP que se integra con la API [!DNL FreeWheel].

En [!UICONTROL Deal ID inbox], puede ver los detalles de la oferta a medida que los ve el editor, acelerar la configuración de la oferta y evitar errores de entrada manuales.

DSP actualiza automáticamente todos los detalles de la oferta diariamente a las 4:30 EST. También actualiza todas las ofertas [!DNL FreeWheel] y actualiza las ofertas existentes de [!DNL Google] y [!DNL Rubicon] por hora. También puede actualizar manualmente los detalles de la oferta para rellenar nuevas ofertas en cualquier momento.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Para ofertas garantizadas mediante programación a través de [!DNL Google Authorized Buyers], debe entregar al menos el 90% de su presupuesto o su cuenta perderá acceso a [!DNL Google] ofertas en [!UICONTROL Deal ID inbox].

## Implementación de [!UICONTROL Deal ID Inbox]

Para recibir sus ofertas en [!UICONTROL Deal ID inbox], sus cuentas de SSP deben asignar la cuenta de DSP de su organización a su cuenta de SSP. DSP compartirá los nombres de las cuentas de la organización con los SSP pertinentes. Póngase en contacto con el administrador de cuentas de Adobe para obtener instrucciones.

Durante las negociaciones del acuerdo, indique al editor que envíe el acuerdo a su comprador en lugar de a la cuenta DSP principal. El identificador de la operación puede ser un nombre o un ID, según el SSP.

## Acciones que puedes llevar a cabo en tus acuerdos

* **Revise los** acuerdos para verificar que la SSP ha enviado el editor, las fechas de vuelo, el CPM y otros detalles de la operación correctos. Si el editor ha cometido un error, póngase en contacto con ellos fuera de DSP para que puedan corregir y volver a enviar el acuerdo.

* **Acepte** las transacciones después de revisarlas y ya no aparecerán en la  [!UICONTROL Deal ID inbox]. Las ofertas aceptadas se enumeran en [!UICONTROL Inventory] > [!UICONTROL Deals] y están listas para dirigirse a las ubicaciones de los anunciantes.

* **Ignore las** transacciones que no son necesarias o que no se solicitan. Las ofertas ignoradas se mueven a la pestaña [!UICONTROL Ignored Deals] dentro de [!UICONTROL Deal ID inbox], que sirve como archivo. DSP alerta a los SSP y a los editores cuando ignora una oferta.

* **Modifique los detalles de las** transacciones ya aceptadas desde  [!UICONTROL Inventory] >  [!UICONTROL Deals] (no en el  [!UICONTROL Deal ID inbox]). Del mismo modo, cuando los editores envían cambios a ofertas, los anunciantes son responsables de implementar esos cambios en [!UICONTROL Inventory] > [!UICONTROL Deals] porque [!UICONTROL Deal ID inbox] no sincroniza los cambios de los SSP después de configurar las ofertas.

## ¿Qué tipos de acuerdos no se pueden aceptar?

Cuando una lista de ofertas no incluye un icono ![Accept](/help/dsp/assets/accept.png) o un botón [!UICONTROL Accept], no puede aceptarlo desde [!UICONTROL Deal ID inbox]. En su lugar, puede [crear manualmente los detalles del ID de la oferta](/help/dsp/inventory/deal-id-create.md).

No puede aceptar los siguientes tipos de ofertas:

* [!DNL Google] ofertas que no están en USD.

* [!DNL Rubicon] ofertas que no están en USD

* [!DNL FreeWheel] ofertas que no están en la moneda de su cuenta.

* Ofertas que tienen una fecha de finalización anterior a hoy.

* Las antiguas [!DNL Rubicon] ofertas etiquetadas como &quot;varios tipos de medios&quot;.

Los detalles del acuerdo incluyen la razón por la que el acuerdo no está disponible para aceptar.

>[!MORELIKETHIS]
>
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Descripción general de las funciones de inventario](inventory-overview.md)

