---
title: Códigos de error para [!DNL FreeWheel] Envíos de publicidad
description: Haga referencia a los códigos de error devueltos para los envíos de anuncios a [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 2%

---

# Códigos de error para [!DNL FreeWheel] Envíos de publicidad

Los mensajes de error para los envíos de anuncios fallidos pueden provenir de Advertising Cloud DSP o de [!DNL FreeWheel]. Los mensajes de error se muestran en la sección [!UICONTROL API Response] en la columna [[!UICONTROL Freewheel Status] cuadro de diálogo](freewheel-check-status.md).

## Errores internos de Advertising Cloud DSP

| Mensaje de error | Descripción | Pasos siguientes |
|--- |--- |--- |
| [!DNL Se espera una respuesta de estado de [!DNL FreeWheel]] | [!DNL FreeWheel] aún no ha respondido que el envío se haya realizado correctamente o que haya fallado. | Vuelva a comprobar el estado en 10 minutos. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] no acepta anuncios del Reino Unido sin números de reloj asignados. | Asigne un número de reloj a la publicidad y vuelva a enviarla. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | El transcodificador no había terminado de transcodificar la publicidad cuando intentaste enviarla. | Espere diez minutos y vuelva a enviar la publicidad. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | El acuerdo presentado no se configura como un acuerdo garantizado programático. [!DNL FreeWheel] solo acepta ofertas garantizadas. | Configure el ID de acuerdo como una oferta garantizada mediante programación. El anuncio se envía automáticamente a [!DNL FreeWheel] al guardar la colocación predeterminada garantizada mediante programación al final del flujo de trabajo de ID de acuerdo. |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | El ID de la oferta enviada no existe o no está activo en el extremo del Adobe. | Asegúrese de que la oferta esté activa y luego vuelva a enviarla. |
| [!DNL \[public_id=]\&lt;deal>] no existe | El id. de la oferta enviada no existe en el [!DNL FreeWheel] final. | Póngase en contacto con su [!DNL FreeWheel] representante para confirmar el ID de la oferta. |
| [!DNL Ad with identifier] \&lt;*nombre del anuncio*\> [!DNL was not found.] | La clave de publicidad enviada no existe o no está activa en el final del Adobe. | Busque la clave de publicidad correcta y luego vuelva a enviarla. |
| [!DNL Pending Submission] | La presentación sigue pendiente. | Actualice la página. |

{style=&quot;table-layout:auto&quot;}

## Errores de API de FreeWheel

| Código | Significado | Descripción | Pasos siguientes |
|--- |--- |--- |--- |
| 401 | No autorizado | Credenciales de acceso incorrectas, faltantes o no válidas. | Póngase en contacto con su [!DNL Adobe] administrador de cuentas. |
| 403 | Prohibido | El servidor entendió la solicitud, pero se niega a autorizarla. | Póngase en contacto con su [!DNL Adobe] administrador de cuentas. |
| 404 | No encontrado | El recurso solicitado no está disponible. Si no se encuentra el ID creativo en la operación de PUT, se devuelve un error 404. | Póngase en contacto con su [!DNL Adobe] administrador de cuentas. |
| 405 | Método no permitido | Se ha realizado una solicitud de un recurso utilizando un método de solicitud no admitido por ese recurso (por ejemplo, utilizando GET en un método que requiere que el POST envíe los datos o utilizando un PUT en un recurso de solo lectura). | Póngase en contacto con su [!DNL Adobe] administrador de cuentas. |
| 408 | Tiempo de espera de solicitud | Se agotó el tiempo de espera mientras se procesaba esta solicitud. Los tiempos de espera suelen deberse a solicitudes simultáneas de acceso exclusivo a determinados recursos. | Vuelva a enviar la solicitud cuando reciba este estado. Si el problema persiste, póngase en contacto con su [!DNL Adobe] administrador de cuentas. |
| 422 | Entidad no procesable | Recurso no válido. Este error ocurre cuando el cuerpo de la solicitud no es válido o el recurso creado/actualizado no es válido (por ejemplo, si no se encontró el ID de acuerdo). Consulte [Errores de la API 422 de FreeWheel](#freewheel-422-errors) para obtener más información. | Póngase en contacto con su [!DNL Adobe] administrador de cuentas. |
| 500 | Error interno del servidor | Error del sistema de API. | Póngase en contacto con su [!DNL Adobe] administrador de cuentas. |

{style=&quot;table-layout:auto&quot;}

## Errores de la API 422 de FreeWheel {#freewheel-422-errors}

| Código | Código HTTP | Descripción |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | Los datos de la solicitud tienen un formato json no válido. Consulte el mensaje de error para obtener más información. |
| DATA_VALIDATION_FAILURE | 422 | A los datos de la solicitud les faltan campos obligatorios o tienen un tipo de datos no válido. Consulte el mensaje de error para obtener más información. |
| DATA_DEAL_INVALID | 422 | La operación está configurada incorrectamente o no existe. Consulte el mensaje de error para obtener más información. |
| DATA_DEAL_GET_FAILURE | 422 | No se encontró el acuerdo o su configuración tiene un problema. Consulte el mensaje de error para obtener más información. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | La dirección URL creativa no es válida. Consulte el mensaje de error para obtener más información. |
| DATA_CREATIVE_LINK_FAILURE | 422 | El creativo no estaba vinculado a los nodos de unidad de publicidad de la oferta. Consulte el mensaje de error para obtener más información. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | El creativo no se actualizó. Consulte el mensaje de error para obtener más información. |
| DATA_DSP_GET_FAILURE | 422 | El DSP no existe en el sistema. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | El elemento creativo no se desvinculaba de las unidades de publicidad. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | El creativo no se eliminó. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | No se detectó la dirección URL. |
| DATA_ENTITY_NOT_FOUND | 422 | El creativo no existe. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Visión General de la Configuración de Ofertas Programáticas Garantizadas en FreeWheel](/help/dsp/inventory/freewheel-overview.md)
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Enviar una publicidad para un acuerdo garantizado programático a FreeWheel](/help/dsp/inventory/freewheel-submit.md)
>* [Compruebe el estado de las publicidades para [!DNL FreeWheel] Ofertas garantizadas mediante programación](/help/dsp/inventory/freewheel-check-status.md)

