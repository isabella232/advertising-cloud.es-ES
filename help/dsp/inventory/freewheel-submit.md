---
title: Enviar una publicidad para un acuerdo PG a [!DNL FreeWheel]
description: Aprenda a solicitar la aprobación de un anuncio para un contrato garantizado mediante programación con un editor en FreeWheel.
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Enviar una publicidad para un acuerdo garantizado programático a FreeWheel

*Cuentas con el permiso  [!DNL FreeWheel] garantizado programático solamente*

Una vez que [acepte un acuerdo garantizado programático con un editor de FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), que incluya la selección de un anuncio y la creación de la colocación predeterminada garantizada programática que se utilizará para el acuerdo, debe enviar el anuncio a FreeWheel para su aprobación.

>[!PREREQUISITES]
>
>Póngase en contacto con el equipo de su cuenta de Adobe para asegurarse de que su cuenta [!DNL DSP] tiene permiso para utilizar el flujo de trabajo [!DNL FreeWheel] garantizado mediante programación.

1. Copie la clave del anuncio para el anuncio utilizado con la oferta de FreeWheel:

   1. Haga clic en el nombre de la campaña.

   1. En el submenú, haga clic en **[!UICONTROL Ads]**.

   1. Haga clic en **[!UICONTROL ...]>[!UICONTROL Edit]** junto al nombre del anuncio.

   1. Una vez que se abra la configuración de la publicidad, copie la clave de publicidad alfanumérica en la dirección URL que se muestra en la barra de direcciones del explorador.

      Por ejemplo, en la siguiente dirección URL, la clave de publicidad es `3NtNC5ZbaGZtqbei8jD3`

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. Envíe la publicidad a FreeWheel:

   1. En la vista [!UICONTROL Deals], busque la oferta.

   1. En la fila de trabajo, haga clic en ![Opciones menú](/help/dsp/assets/options-menu.png) **[!UICONTROL submit to [!DNL FreeWheel]]**.

   1. Compruebe el ID de la oferta, introduzca el **[!UICONTROL Ad Key]** que ha copiado en el paso 1 y, a continuación, haga clic en **[!UICONTROL Submit]**.

   El anuncio debe enviarse y aprobarse antes de ejecutarse.

1. [Compruebe el estado](freewheel-check-status.md) de envío de la publicidad.

>[!MORELIKETHIS]
>
>* [Visión General de la Configuración de Ofertas Programáticas Garantizadas en FreeWheel](freewheel-overview.md)
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Comprobar el estado de las publicidades  [!DNL FreeWheel] para los acuerdos garantizados programáticos](freewheel-check-status.md)
>* [Códigos de error para envíos de anuncios de FreeWheel](freewheel-error-codes.md)

