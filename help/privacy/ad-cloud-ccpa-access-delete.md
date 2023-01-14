---
title: 'Compatibilidad de Adobe Advertising con la Ley de Privacidad del Consumidor de California : Compatibilidad con el acceso y la eliminación de datos del consumidor'
description: Obtenga información sobre los tipos de solicitudes de datos compatibles, los valores de campo y configuración necesarios, y ejemplos de solicitudes de acceso a API que utilizan ID de productos heredados y campos de datos devueltos.
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# Soporte publicitario de Adobe para la Ley de Privacidad del Consumidor de California: Compatibilidad con el acceso y la eliminación de datos del consumidor

*Para [!DNL Adobe Advertising Search]; DSP publicitario de Adobe; Creativo de publicidad de Adobe; y Adobe Advertising DCO*

>[!IMPORTANT]
>
>El contenido de este documento no constituye asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte con su asesor legal para obtener asesoramiento sobre la Ley de Privacidad del Consumidor de California.

La Ley de Privacidad del Consumidor de California (CCPA) es la nueva ley de privacidad de California, que entró en vigor el 1 de enero de 2020. La CCPA otorga a los residentes de California nuevos derechos con respecto a su información personal e impone responsabilidades de protección de datos a ciertas entidades que operen en California. La CCPA otorga a los consumidores el derecho de acceder a su información personal y eliminarla, así como el derecho de exclusión de determinadas actividades que pueden considerarse &quot;vendedoras&quot; de información personal a terceros.

Como empresa, determinará los datos personales que Adobe Experience Cloud procesa y almacena en su nombre.

Como proveedor de servicios, Adobe Advertising proporciona asistencia a su empresa para que cumpla con las obligaciones que le impone la CCPA y que son aplicables al uso de los productos y servicios de Adobe Advertising, incluida la gestión de solicitudes de acceso y eliminación de información personal y la gestión de solicitudes de exclusión de la venta de información personal.

Este documento describe cómo [!DNL Advertising Search]; Advertising Creative; DSP publicitario (Demand Side Platform); y [!DNL Advertising DCO] — como proveedores de servicios — apoyar los derechos de los consumidores a acceder y suprimir información personal mediante el Adobe [!DNL Experience Platform Privacy Service API] y [!DNL Privacy Service UI].

Para obtener información sobre cómo la DSP publicitaria admite el derecho del consumidor a excluirse de la venta de información personal, consulte [Soporte publicitario de Adobe para la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión del consumidor](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md).

Para obtener más información sobre los servicios de privacidad de Adobe para la CCPA, consulte la [Centro de privacidad de Adobe](https://www.adobe.com/privacy/ccpa.html).

## Tipos de solicitudes de datos compatibles con la publicidad de Adobe

Adobe Experience Platform permite a las empresas realizar las siguientes tareas:

* Acceda a los datos de nivel de cookie de un consumidor o a los datos de nivel de ID de dispositivo (para anuncios en aplicaciones móviles) dentro de [!DNL Search], [!DNL Creative], [!DNL DSP]o [!DNL DCO].
* Eliminar datos de nivel de cookie almacenados dentro de [!DNL Search], [!DNL Creative], [!DNL DSP]o [!DNL DCO] para los consumidores que utilicen un navegador; o eliminar datos de nivel de ID almacenados en [!DNL DSP] para consumidores que usan aplicaciones en dispositivos móviles.
* Compruebe el estado de una solicitud o de todas las solicitudes existentes.

## Configuración necesaria para enviar solicitudes de publicidad de Adobe

Para realizar solicitudes de acceso y eliminación de información personal del consumidor de la publicidad de Adobe, deberá:

1. Implemente una biblioteca JavaScript para recuperar y eliminar las cookies del cliente. La misma biblioteca, `AdobePrivacy.js`, se utiliza para todas las soluciones de Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Las solicitudes a algunas soluciones de Experience Cloud no requieren la biblioteca JavaScript, pero las solicitudes de Adobe de publicidad sí lo requieren.

   Debe implementar la biblioteca en la página web desde la que los clientes pueden enviar solicitudes de acceso y eliminación, como el portal de privacidad de su empresa. La biblioteca de ayuda a recuperar las cookies de Adobe (ID de área de nombres: `gsurferID`) para poder enviar estas identidades como parte de las solicitudes de acceso y eliminación a través de la función [!DNL Adobe Experience Platform Privacy Service API].

   Cuando el cliente solicita eliminar datos personales, la biblioteca también elimina la cookie del cliente del explorador del cliente.

   >[!NOTE]
   >
   >La eliminación de datos personales es diferente a la exclusión, que detiene la segmentación de un usuario final con segmentos de audiencia. Sin embargo, cuando un consumidor solicita eliminar datos personales de [!DNL Creative], [!DNL DSP]o [!DNL DCO], la biblioteca también envía una solicitud a Adobe Advertising para excluir al cliente de la segmentación. Para anunciantes con [!DNL Search], le recomendamos que proporcione un vínculo a los clientes de [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), que explica cómo desactivar la segmentación de segmentos de audiencia.

1. Identifique su ID de organización de Experience Cloud y asegúrese de que esté vinculado a sus cuentas publicitarias de Adobe.

   Un ID de organización de Experience Cloud es una cadena alfanumérica de 24 caracteres anexada a &quot;@AdobeOrg&quot;. A la mayoría de los clientes Experience Cloud se les ha asignado un ID de organización. Si el equipo de marketing o el administrador interno del sistema de Adobe no conocen su ID de organización o no están seguros de si se ha aprovisionado, póngase en contacto con el servicio de atención al cliente de Adobe en gdprsupport@adobe.com. Necesitará el ID de organización para enviar solicitudes a la API de privacidad mediante el `imsOrgID` espacio de nombres.

   >[!IMPORTANT]
   >
   >Póngase en contacto con el representante publicitario de Adobe de su empresa para confirmar que todas las cuentas publicitarias de Adobe de su organización, incluidas [!DNL DSP] cuentas o anunciantes, [!DNL Search] cuentas y [!DNL Creative] o [!DNL DCO] cuentas: están vinculadas a su ID de organización de Experience Cloud.

1. Utilice cualquiera de las opciones [API de Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (para solicitudes automatizadas) o [IU de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (para solicitudes ad hoc) presentar solicitudes de acceso y eliminación de información personal a Adobe Advertising en nombre de los consumidores, y comprobar el estado de las solicitudes existentes.

   Para anunciantes que tienen una aplicación móvil para interactuar con clientes e iniciar campañas con [!DNL DSP], deberá descargar los SDK para móviles preparados para la privacidad para el Experience Cloud. Los SDK móviles permiten a las empresas establecer indicadores de estado de exclusión y recuperar el ID del dispositivo del consumidor (ID de espacio de nombres: `deviceID`) y enviar solicitudes a la API de Privacy Service. La aplicación móvil necesitará una versión 4.15.0 o buena del SDK.

   Al enviar una solicitud de acceso de consumidor, la API de Privacy Service devuelve la información de un consumidor en función de la cookie o el ID de dispositivo especificados, que debe devolver al consumidor.

   Cuando envía una solicitud de eliminación de consumidor, el ID de cookie o ID de dispositivo y todos los datos de costes, clics e ingresos asociados con la cookie se eliminan del servidor.

   >[!NOTE]
   Si su empresa tiene varios ID de organización de Experience Cloud, debe enviar solicitudes de API independientes para cada uno. Sin embargo, puede realizar una solicitud de API a varias subsoluciones de publicidad de Adobe ([!DNL Search], [!DNL Creative], [!DNL DSP]y [!DNL DCO]), con una cuenta por subsolución.

Todos estos pasos son necesarios para recibir soporte de la Publicidad de Adobe. Para obtener más información sobre estas y otras tareas relacionadas que debe realizar con Adobe Experience Platform Privacy Service, y dónde encontrar los elementos que necesita, consulte [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Valores de campo requeridos en solicitudes JSON de publicidad de Adobe

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*su ID de organización de Experience Cloud*>

&quot;usuarios&quot;:

* `"key":` &lt;*normalmente el nombre del cliente*>

* `"action":` o `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (lo que indica el espacio de cookies de adcloud)

   * `"value":` &lt;*el valor de ID de cookie del cliente real recuperado de`AdobePrivacy.js`*>

* `"include": **adCloud**` (que es el producto de Adobe que se aplica a la solicitud)

* `"regulation": **ccpa**` (que es la norma de privacidad que se aplica a la solicitud)

## Ejemplo de solicitud enviada por un consumidor mediante un ID de usuario publicitario de Adobe recuperado de AdobePrivacy.js

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
}
```

## Campos de datos que se devuelven para solicitudes de acceso

El siguiente es un ejemplo de una respuesta de acceso a información personal para la publicidad de Adobe.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
