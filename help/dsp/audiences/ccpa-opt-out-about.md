---
title: Acerca de [!UICONTROL CCPA Opt-out-of-Sale] Segmentos e informes
description: Obtenga información sobre la creación de segmentos para rastrear los ID de solicitudes de exclusión de venta de CCPA y cómo recuperar informes de los ID.
feature: CCPA, DSP Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Acerca de [!UICONTROL CCPA Opt-out-of-Sale] Segmentos e informes

Puede realizar un seguimiento de los ID de los usuarios procedentes de solicitudes de exclusión de venta de clientes en su sitio web, de acuerdo con la Ley de privacidad del consumidor de California (CCPA), mediante [creación e implementación de un segmento de exclusión de la venta de CCPA](ccpa-opt-out-segment-create.md). Los usuarios permanecen en segmentos de exclusión de la venta de la CCPA indefinidamente.

Una vez implementada la etiqueta de píxeles del segmento, la publicidad de Adobe empezará a recopilar un grupo de ID en nombre del anunciante.

## Informes de exclusión de ventas del consumidor

La publicidad de Adobe genera informes mensuales de los ID que los clientes han enviado para solicitudes de exclusión de venta de la cuenta. Los datos consolidan las solicitudes capturadas mediante segmentos de exclusión de venta de CCPA creados en DSP y cualquier envío realizado mediante la API de Privacy Service.  Los informes se generan el primer día de cada mes del mes anterior. Por ejemplo, la lista mensual de usuarios de junio está disponible el 1 de julio.

Cada informe está disponible como un archivo de texto separado por tabuladores comprimido en formato GZIP. Los ID de usuario capturados en segmentos de exclusión de la venta de la CCPA se identifican por segmento y por anunciante.

Puede [recuperar vínculos a los informes mensuales](ccpa-opt-out-segment-report-retrieve.md) que se crearon en los tres meses anteriores, ya sea desde dentro de DSP o mediante el uso de la DSP [!DNL Trafficking API]. Cada vínculo es válido durante siete días, pero se actualiza cada vez que un cliente intenta recuperar uno.

>[!MORELIKETHIS]
>
>* [Soporte publicitario de Adobe para la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión del consumidor](/help/privacy/ccpa-opt-out-of-sale.md)
>* [Cree e implemente un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Recuperar informes de exclusión de ventas de consumidores](ccpa-opt-out-segment-report-retrieve.md)
>* [Acerca de la gestión de público](audience-about.md)

