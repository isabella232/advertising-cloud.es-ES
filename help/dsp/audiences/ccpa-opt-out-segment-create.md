---
title: Creación e implementación de un segmento de exclusión de venta de CCPA
description: Obtenga información sobre cómo crear e implementar un segmento para rastrear los ID de usuario de solicitudes de exclusión de venta de clientes.
feature: CCPA, Segments
exl-id: aebe0c5b-382f-4e4a-b145-c32f32d216ca
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Creación e implementación de un segmento de exclusión de venta de CCPA

Puede crear un segmento para rastrear los ID de usuario a partir de solicitudes de exclusión de venta de consumidores en su sitio web, según la Ley de privacidad del consumidor de California (CCPA). Los usuarios permanecen en segmentos de exclusión de la venta de la CCPA indefinidamente.

Una vez implementada la etiqueta de píxeles de segmento, Advertising Cloud empezará a recopilar un grupo de ID en nombre del anunciante.

>[!NOTE]
>
>* Para obtener información sobre cómo comunicar las solicitudes de exclusión de CCPA a Advertising Cloud mediante la API de Adobe Experience Platform Privacy Service, consulte [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html).
>* Para rastrear a los usuarios que visitan páginas web con fines no relacionados con el seguimiento de eventos de exclusión de la CCPA, así como a los usuarios expuestos a anuncios de dispositivos de escritorio, móviles y CTV, cree un [segmento personalizado](/help/dsp/audiences/custom-segment-create.md).


1. Cree el segmento:

   1. En el menú principal, haga clic en **Audiencias > Segmentos**.

   1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

   1. Escriba un **[!UICONTROL Segment Name]** único.

      Nombre del segmento recomendado: &quot;&lt;*El nombre del anunciante*>: exclusión de la CCPA&quot; (como &quot;Acme - Exclusión de la venta de la CCPA&quot;)

   1. Para el [!UICONTROL Segment Type], seleccione **[!UICONTROL CCPA Opt-out of sale]**.

   1. Haga clic **[!UICONTROL Save]**.

1. Copie e implemente una etiqueta de píxeles para rastrear el segmento:

   1. Vuelva a **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. En la fila de segmento, mantenga el cursor sobre el nuevo segmento y haga clic en **[!UICONTROL Get pixel]**.

   1. Copie el píxel de imagen (comenzando por `<img src="https://rtd-tm.everesttech.net"`) para recopilar los ID de usuario de visitantes de escritorio y móviles a una página web.

   1. Proporcione la etiqueta al anunciante o al contacto del sitio web para la implementación mediante el mecanismo que la empresa utiliza para rastrear las solicitudes de exclusión de la venta de CCPA (como el uso de una plataforma de administración de consentimiento).

      Es posible que el departamento de TI u otro grupo del anunciante tenga que programar la implementación de etiquetas o que se le informe al respecto.

      Una vez implementado el píxel, Advertising Cloud empezará a recopilar un grupo de ID en nombre del anunciante.

      Aunque la lógica y la elección de la implementación dependen del anunciante, aquí hay un ejemplo de cómo un anunciante podría activar el píxel:

      1. Un consumidor llega a la página de inicio del anunciante.
      1. El consumidor encuentra y hace clic en el botón de exclusión de la CCPA del anunciante.
      1. Al consumidor se le presenta una lista de proveedores de servicios con los que trabaja el anunciante.
      1. El consumidor marca la casilla para desactivar la venta de datos a Adobe Advertising Cloud.

         Esta acción déclencheur al píxel que se activa y que recopila el ID de cookie del consumidor dentro del segmento &quot;[!UICONTROL CCPA Opt-out of sale]&quot; especificado.

>[!MORELIKETHIS]
>
>* [Compatibilidad de Adobe Advertising Cloud con la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión del consumidor](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [Acerca de los  [!UICONTROL CCPA Opt-out-of-Sale] segmentos y los informes](ccpa-opt-out-about.md)
>* [Recuperar informes de exclusión de ventas de consumidores](ccpa-opt-out-segment-report-retrieve.md)
>* [Crear e implementar un segmento personalizado](custom-segment-create.md)
>* [Acerca de la gestión de público](audience-about.md)

