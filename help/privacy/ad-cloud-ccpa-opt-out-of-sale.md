---
title: Compatibilidad de Adobe Advertising Cloud con la Ley de Privacidad del Consumidor de California y la Ley n.º 58; Compatibilidad con la exclusión de ventas del consumidor
description: Obtenga información sobre la compatibilidad para capturar solicitudes de exclusión de venta de clientes.
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 0%

---

# Compatibilidad de Adobe Advertising Cloud con la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión de ventas del consumidor

*Para el Demand Side Platform de Adobe Advertising Cloud*

>[!IMPORTANT]
>
>El contenido de este documento no constituye asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte con su asesor legal para obtener asesoramiento sobre la Ley de Privacidad del Consumidor de California.

La Ley de Privacidad del Consumidor de California (CCPA) es la nueva ley de privacidad de California, que entró en vigor el 1 de enero de 2020. La CCPA otorga a los residentes de California nuevos derechos con respecto a su información personal e impone responsabilidades de protección de datos a ciertas entidades que operen en California. La CCPA otorga a los consumidores el derecho de acceder a sus datos y eliminarlos, así como el derecho de exclusión de determinadas actividades que pueden considerarse &quot;vendedoras&quot; de información personal a terceros.

Como empresa, determinará los datos personales que Adobe Experience Cloud procesa y almacena en su nombre.

Como proveedor de servicios, Adobe Advertising Cloud proporciona asistencia a su empresa para que cumpla con las obligaciones que le impone la CCPA y que son aplicables al uso de los productos y servicios de Advertising Cloud, incluida la gestión de las solicitudes de los consumidores de acceso y eliminación de información personal y la gestión de las solicitudes de los consumidores de exclusión de la venta de información personal.

Este documento describe cómo el Demand Side Platform de Adobe Advertising Cloud (DSP), como proveedor de servicios, admite el derecho del consumidor a excluirse de la &quot;venta&quot; de &quot;información personal&quot;, tal como define cada término la CCPA. Incluye información sobre cómo comunicar las solicitudes de exclusión de la venta a Advertising Cloud y cómo recuperar informes de las solicitudes de exclusión de la venta de su organización.

Para obtener información sobre cómo Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform) y Media Optimizer DCO admiten los derechos de acceso y eliminación de información personal de los consumidores, consulte [Adobe Advertising Cloud Support for the California Consumer Privacy Act (Compatibilidad de con la privacidad del consumidor de California): Compatibilidad con acceso y eliminación de datos del consumidor](/help/privacy/ad-cloud-ccpa-access-delete.md).

Para obtener más información sobre los servicios de privacidad de Adobe para la CCPA, consulte el [Centro de privacidad de Adobe](https://www.adobe.com/privacy/ccpa.html).

## Comunicar a Advertising Cloud las solicitudes de exclusión de la venta de los consumidores

Puede comunicar las solicitudes de exclusión de la venta de los consumidores mediante:

* un segmento de exclusión de CCPA creado en Advertising Cloud DSP
* la API de Adobe Experience Platform Privacy Service

### Método 1: Comunicar las solicitudes de exclusión de CCPA mediante un segmento [!UICONTROL CCPA Opt-Out-of-Sale] en Advertising Cloud DSP

>[!NOTE]
>
>Los usuarios permanecen en segmentos de exclusión de la venta de la CCPA indefinidamente.

1. Inicie sesión en la cuenta del anunciante en Advertising Cloud DSP en [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Cree un segmento de exclusión de la venta de la CCPA e implemente el píxel del segmento para capturar las solicitudes](/help/dsp/audiences/ccpa-opt-out-segment-create.md) de exclusión.

### Método 2: Comunicar las solicitudes de exclusión de CCPA mediante la API de Adobe Experience Platform Privacy Service

*A los anunciantes se les asignó únicamente un ID de organización de Experience Cloud (ID de organización de IMS)*

1. Implemente una biblioteca JavaScript para recuperar las cookies del cliente. La misma biblioteca, `AdobePrivacy.js`, se utiliza para todas las soluciones de Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Las solicitudes a algunas soluciones de Adobe Experience Cloud no requieren la biblioteca JavaScript, pero las solicitudes a Advertising Cloud sí la requieren.

   Debe implementar la biblioteca en la página web desde la que los clientes pueden enviar solicitudes de exclusión de la venta, como el portal de privacidad de su empresa. La biblioteca de ayuda a recuperar las cookies de Adobe (ID de área de nombres: `gsurferID`) para poder enviar estas identidades como parte de solicitudes de exclusión de venta a través de la API de Adobe Experience Platform Privacy Service.

1. Identifique su ID de organización de IMS y asegúrese de que esté vinculado a sus cuentas de Advertising Cloud.

   Un ID de organización de IMS es una cadena alfanumérica de 24 caracteres anexada a @AdobeOrg. A la mayoría de los clientes de Adobe Experience Cloud se les ha asignado un ID de organización de IMS. Si el equipo de marketing o el administrador interno del sistema de Adobe no conocen el ID de organización de IMS de su organización o no están seguros de si se ha aprovisionado, póngase en contacto con el servicio de atención al cliente de Adobe en gdprsupport@adobe.com. Necesitará el ID de organización de IMS para enviar solicitudes a la API de privacidad.

   >[!IMPORTANT]
   >
   >Póngase en contacto con el representante de Advertising Cloud de su empresa para confirmar que todas las cuentas de Advertising Cloud de su organización (incluidas las cuentas [!DNL DSP] o anunciantes, [!DNL Search] cuentas y [!DNL Creative] o [!DNL DCO] cuentas) están vinculadas a su ID de organización de IMS.

1. Utilice la API de Adobe Experience Platform Privacy Service para [enviar solicitudes de exclusión de venta](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) a Advertising Cloud en nombre de los consumidores y para comprobar el estado de las solicitudes existentes.

   Consulte el apéndice siguiente para ver un ejemplo de una solicitud de exclusión de la venta.

   >[!NOTE]
   Si su empresa tiene varios ID de organización de servicio de Adobe Experience Cloud Identity Management (ID de organización de IMS), debe enviar solicitudes de API independientes para cada uno. Sin embargo, puede realizar una solicitud de API a varias subsoluciones de Advertising Cloud ([!DNL Search], [!DNL Creative], [!DNL DSP] y [!DNL DCO]), con una cuenta por cada subsolución.

Todos estos pasos son necesarios para recibir asistencia de Advertising Cloud. Para obtener más información sobre estas y otras tareas relacionadas que debe realizar con Adobe Experience Platform Privacy Service, y dónde encontrar los elementos que necesita, consulte [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Recuperación de informes de consumidores que enviaron solicitudes de exclusión de venta

Advertising Cloud genera informes mensuales de los ID que los clientes han enviado para solicitudes de exclusión de venta de la cuenta. Cada informe está disponible como un archivo de texto separado por tabuladores comprimido en formato GZIP. Los datos consolidan las solicitudes capturadas mediante segmentos de exclusión de la venta de CCPA creados en Advertising Cloud DSP y cualquier envío realizado mediante la API de Privacy Service. Los ID de usuario capturados en segmentos de exclusión de la venta de la CCPA se identifican por segmento y por anunciante. Los informes se generan el primer día de cada mes del mes anterior. Por ejemplo, la lista mensual de usuarios de junio está disponible el 1 de julio.

Puede recuperar vínculos a los informes mensuales creados en los tres meses anteriores, ya sea desde Advertising Cloud DSP o mediante Advertising Cloud [!DNL Trafficking API]. Cada vínculo es válido durante siete días, pero se actualiza cada vez que un cliente intenta recuperar uno.

### Método 1: Recuperar informes de exclusión de ventas del consumidor dentro de Advertising Cloud DSP

1. Inicie sesión en la cuenta del anunciante en Advertising Cloud DSP en [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Recupere los informes](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Método 2: Recuperar informes de exclusión de ventas de consumidores con Advertising Cloud [!DNL Trafficking API]

Esta función está disponible para las organizaciones que utilizan [!DNL Trafficking API]. Consulte la documentación de [!DNL Trafficking API] para obtener más información.

Si su organización no utiliza el [!DNL Trafficking API] pero está interesada en obtener más información, póngase en contacto con el administrador de cuentas de Adobe.

## Apéndice: Ejemplo de solicitud [!UICONTROL CCPA Opt-Out-of-Sale] para usuarios de API de Privacy Service

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

donde:

* `"namespace": "AdCloud"` indica el espacio de la  `AdCloud` cookie y el valor correspondiente es el ID de la cookie del cliente recuperado de  `AdobePrivacy.js`
* `"include": ["AdCloud"]` indica que la solicitud se aplica a Advertising Cloud
