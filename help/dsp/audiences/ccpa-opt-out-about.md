---
title: Acerca de los [!UICONTROL CCPA Opt-out-of-Sale] segmentos e informes
description: Obtenga información sobre la creación de segmentos para rastrear los ID de solicitudes de exclusión de venta de CCPA y cómo recuperar informes de los ID.
feature: CCPA, Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Acerca de los [!UICONTROL CCPA Opt-out-of-Sale] segmentos e informes

Puede realizar un seguimiento de los ID de usuario procedentes de solicitudes de exclusión de venta de consumidores en su sitio web, según la Ley de privacidad del consumidor de California (CCPA), [creando e implementando un segmento de exclusión de la venta de CCPA](ccpa-opt-out-segment-create.md). Los usuarios permanecen en segmentos de exclusión de la venta de la CCPA indefinidamente.

Una vez implementada la etiqueta de píxeles de segmento, Advertising Cloud empezará a recopilar un grupo de ID en nombre del anunciante.

## Informes de exclusión de ventas del consumidor

Advertising Cloud genera informes mensuales de los ID que los clientes han enviado para solicitudes de exclusión de venta de la cuenta. Los datos consolidan las solicitudes capturadas mediante segmentos de exclusión de la venta de CCPA creados en Advertising Cloud DSP y cualquier envío realizado mediante la API de Privacy Service.  Los informes se generan el primer día de cada mes del mes anterior. Por ejemplo, la lista mensual de usuarios de junio está disponible el 1 de julio.

Cada informe está disponible como un archivo de texto separado por tabuladores comprimido en formato GZIP. Los ID de usuario capturados en segmentos de exclusión de la venta de la CCPA se identifican por segmento y por anunciante.

Puede [recuperar los vínculos a los informes mensuales](ccpa-opt-out-segment-report-retrieve.md) que se crearon en los tres meses anteriores, ya sea desde Advertising Cloud DSP o mediante Advertising Cloud [!DNL Trafficking API]. Cada vínculo es válido durante siete días, pero se actualiza cada vez que un cliente intenta recuperar uno.

>[!MORELIKETHIS]
>
>* [Compatibilidad de Adobe Advertising Cloud con la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión del consumidor](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [Creación e implementación de un  [!UICONTROL CCPA Opt-Out-of-Sale] segmento](ccpa-opt-out-segment-create.md)
>* [Recuperar informes de exclusión de ventas de consumidores](ccpa-opt-out-segment-report-retrieve.md)
>* [Acerca de la gestión de público](audience-about.md)

