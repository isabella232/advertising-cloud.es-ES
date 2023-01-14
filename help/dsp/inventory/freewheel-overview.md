---
title: Información general sobre la configuración de ofertas PG en [!DNL Freewheel]
description: Obtenga información sobre los requisitos previos y los pasos adicionales necesarios para ejecutar anuncios para ofertas garantizadas mediante programación con editores en [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: acf8351b-88fb-4f18-8fca-9a2d6674cdec
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Información general sobre la configuración de ofertas garantizadas mediante programación en [!DNL Freewheel]

Configuración de acuerdos garantizados programáticos con editores en [!DNL Freewheel] requiere permisos y pasos adicionales.

>[!PREREQUISITES]
>
>Trabaje con su [!DNL Adobe] el equipo de la cuenta para garantizar que su [!DNL DSP] tiene los siguientes permisos:
>
>* Permiso para usar la variable [!DNL FreeWheel] flujo de trabajo garantizado por programación, que es necesario para enviar una publicidad para una oferta garantizada por programación a [!DNL FreeWheel].
>
>* (Si trabaja con editores del Reino Unido que requieren un [!DNL Clearcast] número de reloj con cada anuncio) Permiso para incluir números de reloj en sus anuncios.


## Flujo de trabajo

1. Cree una publicidad con el tipo de medio especificado en la oferta.

   Para algunos editores del Reino Unido, debe incluir un [!DNL Clearcast] número de reloj con su anuncio.

1. [Aceptar el ID de la oferta](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) que ya ha negociado con un editor en [!DNL Freewheel] uso de la bandeja de entrada Deal ID.

   Después de aceptar la oferta, siga las indicaciones para 1) seleccionar la publicidad que desea usar para la oferta y 2) crear una ubicación predeterminada garantizada programáticamente para servir la publicidad.

1. [Enviar la publicidad a [!DNL Freewheel]](freewheel-submit.md)

   El anuncio debe enviarse y aprobarse antes de ejecutarse.

1. [Comprobar el estado de envío de la publicidad](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Enviar una publicidad para un acuerdo garantizado programático a [!DNL Freewheel]](freewheel-submit.md)
>* [Compruebe el estado de las publicidades para [!DNL FreeWheel] Ofertas garantizadas mediante programación](freewheel-check-status.md)
>* [Códigos de error para [!DNL Freewheel] Envíos de publicidad](freewheel-error-codes.md)

