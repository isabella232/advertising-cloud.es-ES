---
title: Configuración de un acuerdo garantizado programático
description: Aprenda a configurar un acuerdo garantizado mediante programación (PG) que haya negociado con un editor.
feature: Private Inventory, Deal IDs, Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Configuración de un acuerdo garantizado programático

*[Solo plataformas de suministro compatibles](programmatic-guaranteed-about.md)*

Después de negociar una operación con garantías programáticas (PG) con un publicador admitido, puede configurar la operación en DSP utilizando el [!DNL Deal ID inbox] o introduciendo manualmente los detalles de la operación.

>[!NOTE]
>
> Para las ofertas PG, el editor gestiona todo el ritmo del presupuesto, el límite del presupuesto y la segmentación. Todos los SSP que permiten PG a través de DSP confirman que el editor puede configurar límites presupuestarios.
>
> La configuración de ofertas garantizadas mediante programación con editores en [!DNL FreeWheel] requiere permisos y pasos adicionales. Para obtener más información, consulte &quot;[Overview of Setting up Programatic Garantied Deals in [!DNL FreeWheel]](freewheel-overview.md)&quot; (Información general sobre la configuración de ofertas garantizadas mediante programación en).

## Configurar un contrato garantizado mediante programación utilizando el [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Este es el método preferido para [!DNL FreeWheel], [!DNL Google Authorized Buyers] y [!DNL Rubicon].

1. [Acepte el trato](deal-id-inbox-accept.md).

1. Después de guardar la oferta, seleccione las publicidades que se utilizarán para la oferta y cree una colocación predeterminada garantizada mediante programación (PG), según se le solicite.

   La creación de una colocación de PG predeterminada para la oferta es obligatoria para entregar el 100% de su compra. Este tipo de ubicación no tiene segmentación, por lo que DSP devolver una oferta a cada solicitud de oferta del editor.

   * Si acepta una única oferta, se le redirige automáticamente al flujo de trabajo de creación de ubicación predeterminada de PG.

      Todas las [!DNL FreeWheel] ofertas se proponen como una única oferta.

   * Si está aceptando una propuesta con varios ID de oferta de PG, identifique cada ubicación predeterminada de PG que necesita crear. Una vez que haya creado todas las ubicaciones necesarias, el botón Continuar estará activado.

1. (Opcional) Dirija la operación PG a ubicaciones adicionales que no sean de PG.

## Configuración manual de un acuerdo garantizado programático

Utilice este método para todos los demás SSP.

1. [Configuración manual de los detalles](deal-id-create.md) del ID de la oferta.

1. Después de guardar la oferta, seleccione las publicidades que se utilizarán para la oferta y cree una colocación predeterminada de PG, según se le solicite.

   La creación de una colocación predeterminada de PG para la oferta es obligatoria para entregar el 100% de su compra. Este tipo de ubicación no tiene segmentación, por lo que DSP devolver una oferta a cada solicitud de oferta del editor.

1. (Opcional) Dirija la operación PG a ubicaciones adicionales que no sean de PG.

>[!MORELIKETHIS]
>
>* [Acerca de los Ofertas Garantizadas mediante Programación](programmatic-guaranteed-about.md)
>* [Sugerencias para negociar un acuerdo garantizado mediante programación](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Enviar una publicidad para un acuerdo garantizado programático con [!DNL FreeWheel]](freewheel-submit.md)
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Crear manualmente detalles de ID de acuerdo](deal-id-create.md)
>* [Socios de SSP](ssp-partners.md)
>* [Descripción general de las funciones de inventario](inventory-overview.md)

