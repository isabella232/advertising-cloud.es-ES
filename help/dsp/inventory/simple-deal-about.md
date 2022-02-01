---
title: Cree un [!UICONTROL Simple Ad Serving] Acuerdo
description: Obtenga información sobre [!UICONTROL Simple Ad Serving] trata el uso de píxeles de seguimiento de eventos.
feature: DSP Simple Ad Serving
source-git-commit: 7d236b7eabe061c813ad83d34e333dbd169c867a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Acerca de [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] proporciona informes y entrega de anuncios garantizados y sin decisiones para un editor específico y un único tipo de anuncio que utiliza una sola ubicación dedicada. Uso [!DNL Simple Ad Serving] cuando el editor no puede ejecutar la operación mediante ID de acuerdo. El editor gestiona todos los objetivos, el ritmo del presupuesto y los límites de frecuencia. Ejecute estas ofertas a través de píxeles de seguimiento de eventos.

con [!UICONTROL Simple Ad Serving], el editor (servidor del sitio) proporciona cada anuncio directamente y DSP un píxel de seguimiento de eventos para enviarlo al editor, que necesita implementar el píxel y el tráfico de los anuncios de DSP. Según el tipo de inventario, los píxeles de evento miden los eventos de impresión, pulsación y vídeo reproducido.

Están disponibles los siguientes tipos de anuncios:

* anuncio previo a la emisión estándar de escritorio
* tableta y anuncio previo a la emisión estándar para móviles
* anuncio previo estándar de TV conectado
* visualización
* audio

Puede crear un [!UICONTROL Simple Ad Serving] en el [!UICONTROL Inventory] > [!UICONTROL Deals] vista. DSP genera automáticamente una ubicación con el subtipo &quot;[!DNL Simple ad serving]&quot; para el anuncio. La ubicación se dirige a la oferta, pero no permite objetivos, presupuestos o límites de frecuencia adicionales. Puede editar solo algunas de las configuraciones de la oferta, como el nombre de la oferta, el CPM, las impresiones y las fechas de vuelo.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] las colocaciones no cumplen con los fondos utilizables de la cuenta ni con los presupuestos de campañas y paquetes. Sin embargo, se hace un seguimiento del gasto y se cuenta para esos presupuestos. Incluso cuando el CPM es de 0 $, siempre se realiza un seguimiento de los datos de evento.

>[!MORELIKETHIS]
>
>* [Cree un [!UICONTROL Simple Ad Serving] Acuerdo](simple-deal-create.md)
>* [[!UICONTROL Simple Ad Serving] Configuración](simple-deal-settings.md)
>* [Ver píxeles de seguimiento de eventos para un [!UICONTROL Simple Ad Serving] Acuerdo](simple-deal-show-pixels.md)

