---
title: Compatibilidad de Adobe Advertising Cloud con el Reglamento General de Protección de Datos
description: Obtenga información sobre los tipos de solicitudes de datos compatibles, los valores de campo y configuración necesarios, y ejemplos de solicitudes de acceso a API que utilizan ID de productos heredados y campos de datos devueltos
feature: GDPR
exl-id: 304d88d0-d63d-4b32-8d4d-c61ba2409adc
source-git-commit: 2e0395dc1e5aa52adc83c1aaea49793fd5555390
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Compatibilidad de Adobe Advertising Cloud con el Reglamento General de Protección de Datos

*Para Adobe Advertising Cloud Search, Adobe Advertising Cloud Creative, Adobe Advertising Cloud DSP y Adobe Media Optimizer DCO*

>[!IMPORTANT]
>
>El contenido de este documento no constituye asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte con su asesor jurídico para obtener asesoramiento sobre el Reglamento General de Protección de Datos.

El Reglamento General de Protección de Datos (RGPD), una ley vigente desde el 25 de mayo de 2018, otorga a todas las personas (interesados) dentro de las fronteras de la Unión Europea (UE) el control de sus datos personales y simplifica el entorno regulatorio para las empresas internacionales. Esta ley se aplica a todas las empresas (responsables del tratamiento de datos) que ofrecen bienes o servicios a personas que se encuentran dentro de los límites de la UE, supervisan o recopilan datos personales de personas que se encuentren dentro de ellos en el momento en que se procesan sus datos personales, independientemente de la ubicación comercial del responsable del tratamiento de datos.

Adobe Experience Cloud actúa como procesador de datos de cualquier dato personal que reciba y almacene en nombre de sus clientes. Como responsable del tratamiento de datos, determinará qué datos personales Adobe Experience Cloud trata y almacena en su nombre.

En este documento se describe cómo Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform) y Media Optimizer DCO admiten los derechos de acceso y eliminación de datos del RGPD de sus interesados mediante la API de Adobe Experience Platform Privacy Service y la IU de Privacy Service.

Para obtener más información sobre el significado del RGPD para su empresa, consulte [RGPD y su empresa](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Tipos de solicitudes de datos compatibles con Advertising Cloud

Adobe Experience Platform permite a las empresas realizar las siguientes tareas:

* Acceda a los datos de nivel de cookie de un interesado o a los datos de nivel de ID de dispositivo (para anuncios en aplicaciones móviles) dentro de [!DNL Search], [!DNL Creative], [!DNL DSP]o [!DNL DCO].
* Eliminar datos de nivel de cookie almacenados dentro de [!DNL Search], [!DNL Creative], [!DNL DSP]o [!DNL DCO] para interesados que utilicen un explorador; o eliminar datos de nivel de ID almacenados en [!DNL DSP] para interesados que usen aplicaciones en dispositivos móviles.
* Compruebe el estado de una solicitud o de todas las solicitudes existentes.

## Configuración necesaria para enviar solicitudes para Advertising Cloud

Para realizar solicitudes de acceso y eliminación de datos para Advertising Cloud, deberá:

1. Implemente una biblioteca JavaScript para recuperar y eliminar las cookies de los interesados. La misma biblioteca, `AdobePrivacy.js`, se utiliza para todas las soluciones de Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Las solicitudes a algunas soluciones de Adobe Experience Cloud no requieren la biblioteca JavaScript, pero las solicitudes a Advertising Cloud sí la requieren.

   Debe implementar la biblioteca en la página web desde la que los interesados pueden enviar solicitudes de acceso y eliminación, como el portal de privacidad de su empresa. La biblioteca de ayuda a recuperar las cookies de Adobe (ID de área de nombres: `gsurferID`) para poder enviar estas identidades como parte de las solicitudes de acceso y eliminación a través de la API de Adobe Experience Platform Privacy Service.

   Cuando el interesado solicita la eliminación de datos personales, la biblioteca también elimina la cookie del interesado del explorador del interesado.

   >[!NOTE]
   >
   >La eliminación de datos personales es diferente a la de la exclusión, que detiene la segmentación de un usuario final con segmentos de audiencia. Sin embargo, cuando un interesado solicita la eliminación de datos personales de [!DNL Creative], [!DNL DSP]o [!DNL DCO], la biblioteca también envía una solicitud a Advertising Cloud para excluir al interesado de la segmentación de segmentos. Para anunciantes con [!DNL Search], le recomendamos que proporcione un vínculo a los interesados [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), que explica cómo desactivar la segmentación de segmentos de audiencia.

1. Identifique su ID de organización de Experience Cloud y asegúrese de que esté vinculado a sus cuentas de Advertising Cloud.

   Un ID de organización de Experience Cloud es una cadena alfanumérica de 24 caracteres anexada a &quot;@AdobeOrg&quot;. A la mayoría de los clientes Experience Cloud se les ha asignado un ID de organización. Si el equipo de marketing o el administrador interno del sistema de Adobe no conocen su ID de organización o no están seguros de si se ha aprovisionado, póngase en contacto con el servicio de atención al cliente de Adobe en gdprsupport@adobe.com. Necesitará el ID de organización para enviar solicitudes a la API de privacidad mediante el `imsOrgID` espacio de nombres.

   >[!IMPORTANT]
   >
   >Póngase en contacto con el representante de Advertising Cloud de su empresa para confirmar que todas las cuentas de Advertising Cloud de su organización, incluidas [!DNL DSP] cuentas o anunciantes, [!DNL Search] cuentas y [!DNL Creative] o [!DNL DCO] cuentas: están vinculadas a su ID de organización de Experience Cloud.

1. Utilice cualquiera de las opciones [API de Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (para solicitudes automatizadas) o [IU de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (en el caso de solicitudes ad hoc) para enviar solicitudes de acceso y eliminación a Advertising Cloud en nombre de los interesados, y para comprobar el estado de las solicitudes existentes.

   Para los anunciantes que tengan una aplicación móvil para interactuar con interesados y para iniciar campañas con el DSP, deberá descargar los SDK para móviles preparados para la privacidad para el Experience Cloud. Los SDK móviles permiten que los controladores de datos establezcan indicadores de estado de exclusión, recuperen el ID del dispositivo del sujeto de datos (ID del área de nombres: deviceID) y envíe solicitudes a la API de Privacy Service. La aplicación móvil necesitará una versión 4.15.0 o buena del SDK.

   Al enviar la solicitud de acceso de un interesado, la API del Privacy Service devuelve la información de un interesado en función de la cookie o el ID de dispositivo especificados, que después debe devolver al interesado.

   Al enviar la solicitud de eliminación de un sujeto de datos, el ID de cookie o ID de dispositivo y todos los datos de costes, clics e ingresos asociados con la cookie se eliminan del servidor.

   >[!NOTE]
   Si su empresa tiene varios ID de organización de Experience Cloud, debe enviar solicitudes de API independientes para cada uno. Sin embargo, puede realizar una solicitud de API a varias subsoluciones de Advertising Cloud ([!DNL Search], [!DNL Creative], [!DNL DSP]y [!DNL DCO]), con una cuenta por subsolución.

Todos estos pasos son necesarios para Advertising Cloud. Para obtener más información sobre estas y otras tareas relacionadas que debe realizar con Adobe Experience Platform Privacy Service, y dónde encontrar los elementos que necesita, consulte [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Valores de campo requeridos en solicitudes JSON de Advertising Cloud

&quot;contexto de empresa&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*su valor de ID de organización de IMS*>

`"users":`

* `"key":` &lt;*normalmente el nombre del interesado*>

* `"action":` o `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (que indica que la variable [!DNL adcloud] espacio de cookies)

   * `"value":` &lt;*el valor de ID de cookie del sujeto de datos real recuperado de`AdobePrivacy.js`*>

* `"include": **adCloud**` (que es el producto de Adobe que se aplica a la solicitud)

* `"regulation": **gdpr**` (que es la norma de privacidad que se aplica a la solicitud)

## Ejemplo de solicitud enviada por el sujeto de datos mediante un ID de usuario de Advertising Cloud recuperado de `AdobePrivacy.js`

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
    "regulation":"gdpr"
}
}
```

## Campos de datos que se devuelven para solicitudes de acceso

El siguiente es un ejemplo de respuesta de acceso para Advertising Cloud.

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
