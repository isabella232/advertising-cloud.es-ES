---
title: Creación e implementación de un segmento de exclusión de venta de CCPA
description: Obtenga información sobre cómo crear e implementar un segmento para rastrear los ID de usuario de solicitudes de exclusión de venta de clientes.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 1b5f5a56045616a2d67d9bfc5840bb1f06436fbb
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Creación e implementación de un segmento de exclusión de venta de CCPA

Puede crear un segmento para rastrear los ID de usuario a partir de solicitudes de exclusión de venta de consumidores en su sitio web, según la Ley de privacidad del consumidor de California (CCPA). Los usuarios permanecen en segmentos de exclusión de la venta de la CCPA indefinidamente.

Una vez implementada la etiqueta de píxeles del segmento, la publicidad de Adobe empezará a recopilar un grupo de ID en nombre del anunciante.

>[!NOTE]
>
>* Para obtener información sobre cómo comunicar las solicitudes de exclusión de CCPA a Adobe de publicidad mediante la API de Adobe Experience Platform Privacy Service, consulte [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Para rastrear a los usuarios que visitan páginas web con fines no relacionados con el seguimiento de eventos de exclusión de CCPA, así como a los usuarios expuestos a anuncios de dispositivos de escritorio, móviles y CTV, cree un [segmento personalizado](/help/dsp/audiences/custom-segment-create.md).


1. Cree el segmento:

   1. En el menú principal, haga clic en **Audiencias > Segmentos**.

   1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

   1. Escriba un **[!UICONTROL Segment Name]**.

      Nombre del segmento recomendado: &quot;&lt;*Nombre del anunciante*> - Exclusión de la venta de la CCPA (por ejemplo, &quot;Acme - Exclusión de la venta de la CCPA&quot;)

   1. Para la variable [!UICONTROL Segment Type], seleccione **[!UICONTROL CCPA Opt-out of sale]**.

   1. Haga clic **[!UICONTROL Save]**.

1. Copie e implemente una etiqueta de píxeles para rastrear el segmento:

   1. Volver a **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. En la fila de segmento, mantenga el cursor sobre el nuevo segmento y haga clic en **[!UICONTROL Get pixel]**.

   1. Copiar el píxel de imagen (comenzando por `<img src="https://rtd-tm.everesttech.net"`) para recopilar los ID de usuario de los visitantes de escritorio y móviles a una página web.

   1. Proporcione la etiqueta al anunciante o al contacto del sitio web para la implementación mediante el mecanismo que la empresa utiliza para rastrear las solicitudes de exclusión de la venta de CCPA (como el uso de una plataforma de administración de consentimiento).

      Es posible que el departamento de TI u otro grupo del anunciante tenga que programar la implementación de etiquetas o que se le informe al respecto.

      Una vez implementado el píxel, la publicidad de Adobe empezará a recopilar un grupo de ID en nombre del anunciante.

      Aunque la lógica y la elección de la implementación dependen del anunciante, aquí hay un ejemplo de cómo un anunciante podría activar el píxel:

      1. Un consumidor llega a la página de inicio del anunciante.
      1. El consumidor encuentra y hace clic en el botón de exclusión de la CCPA del anunciante.
      1. Al consumidor se le presenta una lista de proveedores de servicios con los que trabaja el anunciante.
      1. El consumidor marca la casilla para desactivar la venta de datos a Adobe Advertising.

         Esta acción déclencheur al píxel para que se active y recopile el ID de cookie del consumidor dentro del &quot;[!UICONTROL CCPA Opt-out of sale]&quot;.

>[!MORELIKETHIS]
>
>* [Soporte publicitario de Adobe para la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión del consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Acerca de [!UICONTROL CCPA Opt-out-of-Sale] Segmentos e informes](ccpa-opt-out-about.md)
>* [Recuperar informes de exclusión de ventas de consumidores](ccpa-opt-out-segment-report-retrieve.md)
>* [Crear e implementar un segmento personalizado](custom-segment-create.md)
>* [Acerca de la gestión de público](audience-about.md)

