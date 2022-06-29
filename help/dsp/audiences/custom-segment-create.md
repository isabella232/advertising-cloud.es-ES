---
title: Crear e implementar un segmento personalizado
description: Aprenda a crear e implementar un segmento personalizado para rastrear a los usuarios expuestos a publicidades o usuarios que visitan sus páginas web.
feature: DSP Segments
exl-id: 691903e2-773e-4205-837e-822f435f57a7
source-git-commit: b6e77b91ad5626bb9ece45ec3f01126715dbe37b
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Crear e implementar un segmento personalizado

Puede recopilar sus propios datos de audiencia de origen creando e implementando un segmento de Advertising Cloud personalizado. Puede utilizar el segmento para realizar el seguimiento de a) usuarios expuestos a anuncios de dispositivos de escritorio, móviles y CTV y b) usuarios que visitan páginas web específicas. Posteriormente, puede redirigirse a los usuarios del segmento con anuncios adicionales o evitar que los usuarios del segmento reciban anuncios adicionales.

>[!NOTE]
>
>Para realizar un seguimiento de los ID de los usuarios procedentes de solicitudes de exclusión de venta de clientes en su sitio web, de acuerdo con la Ley de privacidad del consumidor de California (CCPA), cree un [Segmento de exclusión de CCPA](ccpa-opt-out-segment-create.md).

1. Cree el segmento:

   1. En el menú principal, haga clic en **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

   1. Escriba un **[!UICONTROL Segment Name]**.

   1. Para la variable [!UICONTROL Segment Type], seleccione **[!UICONTROL Custom]**.

   1. Introduzca la ventana del segmento, que es el número de días que la cookie de un usuario permanece en el segmento.

      La ventana predeterminada es de 45 días. Introduzca un valor de uno (1) a 365.

   1. Haga clic **[!UICONTROL Save]**.

1. Copie e implemente etiquetas para realizar el seguimiento del segmento, según sea necesario:

   1. Volver a **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   2. Mantenga el cursor sobre la fila de segmento y haga clic en **[!UICONTROL Get pixel]**.

      * Para realizar un seguimiento de los visitantes de escritorio y móviles a una página web:

         1. Copie la etiqueta de seguimiento de vista de página, que se denomina &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. Proporcione la etiqueta al anunciante o al contacto del sitio web para la implementación.

            Es posible que el departamento de TI u otro grupo del anunciante tenga que programar la implementación de etiquetas o que se le informe al respecto.
      * Para hacer un seguimiento de los usuarios expuestos a una unidad de publicidad en dispositivos de escritorio, móviles o CTV:

         1. Copie la etiqueta de seguimiento de impresión, que se denomina &quot;[!UICONTROL Desktop or mobile ads].&quot;

         1. Agregue la etiqueta a [!UICONTROL Pixel] para cada anuncio relevante o para la [!UICONTROL Event Pixels] de la sección [[!UICONTROL Tracking] configuración para cada ubicación correspondiente](/help/dsp/campaign-management/placements/placement-settings.html#placement-tracking).


Una vez implementada la etiqueta de seguimiento, puede utilizar el segmento en los destinos o exclusiones de audiencia para cualquier ubicación.

>[!TIP]
>
>Realice un seguimiento del tamaño del segmento a medida que se realiza el seguimiento de los usuarios.

>[!MORELIKETHIS]
>
>* [Acerca de la gestión de público](audience-about.md)
>* [Cree e implemente un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Crear una audiencia reutilizable](reusable-audience-create.md)
>* [Configuración de audiencia](audience-settings.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- I'll add x-ref to ad settings later.-->
