---
title: Cree un [!UICONTROL Simple Ad Serving] Acuerdo
description: Obtenga información sobre cómo crear un píxel de seguimiento para un [!UICONTROL Simple Ad Serving] trato.
feature: DSP Simple Ad Serving
exl-id: d8de85ec-616c-44ed-9a1a-cc25713ad4a4
source-git-commit: 3e47fec28a17cb64de42309c0368293e1ef1cdea
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Cree un [!UICONTROL Simple Ad Serving] Acuerdo

1. En el menú principal, haga clic en **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]** y, a continuación, seleccione **[!UICONTROL Simple Ad Serving]**.

1. Introduzca la variable [configuración de acuerdo](simple-deal-settings.md):

   1. En el [!UICONTROL Select Ad Source] , especifique información sobre el publicador, el anunciante y la campaña, y el tipo de publicidad y, a continuación, haga clic en **[!UICONTROL Next]**.

   1. En el [!UICONTROL Select Ad(s)] , especifique una publicidad para utilizarla como proxy en DSP:

      1. Realice una de las siguientes acciones:

         * Para las publicidades existentes, seleccione las que desee utilizar.

         * Para nuevas publicidades, cree un proxy [anuncio de origen](/help/dsp/campaign-management/ads/ad-create.md) o [anuncio de terceros](/help/dsp/campaign-management/ads/ad-create-third-party.md).
      >[!NOTE]
      > En realidad, no DSP los anuncios que especifique. El editor publicará el anuncio.

      1. Haga clic **[!UICONTROL Next]**.
   1. En Detalles de fuente, edite los detalles de la fuente y, a continuación, haga clic en **[!UICONTROL Next]**.

      Advertising Cloud DSP genera automáticamente una ubicación denominada &quot;Ubicación SAS - &lt;*nombre de la oferta*>,&quot; para el anuncio. En la ubicación, la oferta se dirige automáticamente a la [!UICONTROL Inventory Targets] para obtener más información. Todas las demás opciones de segmentación no son aplicables.



1. Envíe los píxeles de seguimiento de eventos al editor para su implementación de cualquiera de estas formas:

   * (Opcional) Desde la [!UICONTROL Activate Tag with Publisher] , envíe la etiqueta de oferta al editor.

      Al finalizar los pasos anteriores, DSP genera un mensaje de correo electrónico que puede enviar al editor. El mensaje incluye los detalles de la oferta, un vínculo desde el cual recuperar la etiqueta de oferta y un código de autorización para el vínculo.

      1. Revise los detalles de la oferta y, a continuación, realice una de las acciones siguientes:

         * Para pegar la información en un mensaje de correo electrónico en una aplicación de correo electrónico del dispositivo, haga clic en **[!UICONTROL Email & Done]** y seleccione la aplicación de correo electrónico. La variable [!UICONTROL CC:] el campo se rellena previamente con una [!DNL Adobe] dirección de soporte técnico. A continuación, puede enviar el mensaje al contacto apropiado para el editor.

         * Para copiar la información en el portapapeles, haga clic en **[!UICONTROL Copy Email].** A continuación, puede pegar manualmente el contenido en un mensaje de correo electrónico y enviarlo al contacto apropiado para el editor. Debe incluir una copia (CC:) para `publisher-support-global@adobe.com`. Cuando haya terminado de copiar el mensaje, haga clic en **[!UICONTROL Email & Done]**.
      1. (Si es necesario) Haga un seguimiento con el editor para ver si la etiqueta incluye las macros adecuadas para que la etiqueta funcione con el servidor de publicidad del editor.
   * (Opcional) Envíe manualmente los píxeles de seguimiento de eventos al editor:

      1. En la fila de la oferta dentro de la [!UICONTROL Deals] ver, haga clic en ![Menú Opciones](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Los píxeles de evento incluyen un [!UICONTROL Clickthrough] píxel y [!UICONTROL Impression] píxel. Los anuncios de vídeo y audio también incluyen píxeles de evento por cuartil completados (a partir de [!UICONTROL 25% Complete] a [!UICONTROL 100% Complete]).

      1. Copie los píxeles de seguimiento de eventos y proporciónelos al editor.



>[!MORELIKETHIS]
>
>* [Acerca de [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Configuración](simple-deal-settings.md)
>* [Ver píxeles de seguimiento de eventos para un [!UICONTROL Simple Ad Serving] Acuerdo](simple-deal-show-pixels.md)

