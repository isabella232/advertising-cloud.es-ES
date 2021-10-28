---
title: Enviar una publicidad para un acuerdo de PG a [!DNL FreeWheel]
description: Aprenda a solicitar la aprobación de un anuncio para un contrato garantizado mediante programación con un editor en FreeWheel.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: c2caed80f0afc0cbe3572d01dc2c89f13ed13712
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Enviar una publicidad para un acuerdo garantizado programático a FreeWheel

*Cuentas con la variable [!DNL FreeWheel] Permiso garantizado mediante programación únicamente*

Una vez que [aceptar un acuerdo garantizado programático con un editor en FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), incluida la selección de una publicidad y la creación de la colocación predeterminada garantizada mediante programación que se utilizará para la oferta, debe enviar la publicidad a FreeWheel para su aprobación.

>[!PREREQUISITES]
>
>Trabaje con su [!DNL Adobe] el equipo de la cuenta para garantizar que su [!DNL DSP] La cuenta tiene permiso para usar la variable [!DNL FreeWheel] flujo de trabajo garantizado mediante programación.

## Copiar una clave de publicidad para usarla con la variable [!DNL FreeWheel] Acuerdo {#copy-ad-key}

1. Haga clic en el nombre de la campaña.

1. En el submenú, haga clic en **[!UICONTROL Ads]**.

1. Haga clic en  **[!UICONTROL ...]>[!UICONTROL Edit]** junto al nombre del anuncio.

1. Una vez que se abra la configuración de la publicidad, copie la clave de publicidad alfanumérica en la dirección URL que se muestra en la barra de direcciones del explorador.

Por ejemplo, en la siguiente dirección URL, la clave de publicidad es `3NtNC5ZbaGZtqbei8jD3`

`https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

## Enviar una publicidad desde el [!UICONTROL Ads] Ver

1. [Copiar la clave de publicidad para la publicidad](#copy-ad-key).

1. Junto al nombre del anuncio, haga clic en  **[!UICONTROL ...]>[!UICONTROL submit to FreeWheel]**.

1. Compruebe el ID de la oferta, introduzca [el **[!UICONTROL Ad Key]**](#copy-ad-key)y, a continuación, haga clic en **[!UICONTROL Submit]**.

   El anuncio debe enviarse y aprobarse antes de ejecutarse.

1. [Comprobar el estado de envío de la publicidad](freewheel-check-status.md).

## Enviar una publicidad desde el [!UICONTROL Deals] Ver

1. [Copiar la clave de publicidad para la publicidad](#copy-ad-key).

1. En el menú principal, haga clic en **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. En la fila de acuerdo, haga clic en ![Menú Opciones](/help/dsp/assets/options-menu.png) **>[!UICONTROL submit to FreeWheel]**.

1. Compruebe el ID de la oferta, introduzca [el **[!UICONTROL Ad Key]**](#copy-ad-key)y, a continuación, haga clic en **[!UICONTROL Submit]**.

   El anuncio debe enviarse y aprobarse antes de ejecutarse.

1. [Comprobar el estado de envío de la publicidad](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Visión General de la Configuración de Ofertas Programáticas Garantizadas en FreeWheel](freewheel-overview.md)
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Compruebe el estado de las publicidades para [!DNL FreeWheel] Ofertas garantizadas mediante programación](freewheel-check-status.md)
>* [Códigos de error para envíos de anuncios de FreeWheel](freewheel-error-codes.md)

