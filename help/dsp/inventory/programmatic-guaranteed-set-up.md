---
title: Configuración de un acuerdo garantizado programático
description: Aprenda a configurar un acuerdo garantizado mediante programación (PG) que haya negociado con un editor.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: 81b1074f86685f863f89a07ecd33e892e4933512
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configuración de un acuerdo garantizado programático

*[Solo plataformas de suministro compatibles](programmatic-guaranteed-about.md)*

Después de negociar un acuerdo de garantía programática (PG) con un publicador admitido, puede configurar el acuerdo dentro de DSP utilizando la variable [!DNL Deal ID inbox] o introduciendo manualmente los detalles de la operación.

>[!NOTE]
>
> Para las ofertas PG, el editor gestiona todo el ritmo del presupuesto, el límite del presupuesto y la segmentación. Todos los SSP que permiten PG a través de DSP confirman que el editor puede configurar límites presupuestarios.
>
> Configuración de acuerdos garantizados programáticos con editores en [!DNL FreeWheel] requiere permisos y pasos adicionales. Consulte &quot;[Información general sobre la configuración de ofertas garantizadas mediante programación en [!DNL FreeWheel]](freewheel-overview.md)&quot; para obtener más información.

## Configure un acuerdo garantizado mediante programación usando la variable [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Este es el método preferido para [!DNL FreeWheel], [!DNL Google Authorized Buyers]y [!DNL Magnite DV+].

1. [Aceptar el acuerdo](deal-id-inbox-accept.md).

1. Después de guardar la oferta, seleccione las publicidades que se utilizarán para la oferta y cree una colocación predeterminada garantizada mediante programación (PG), según se le solicite.

   La creación de una colocación de PG predeterminada para la oferta es obligatoria para entregar el 100% de su compra. Este tipo de ubicación no tiene segmentación, por lo que DSP devolver una oferta a cada solicitud de oferta del editor.

   * Si acepta una única oferta, se le redirige automáticamente al flujo de trabajo de creación de ubicación predeterminada de PG.

      Todo [!DNL FreeWheel] las ofertas se proponen como una única operación.

   * Si está aceptando una propuesta con varios ID de oferta de PG, identifique cada ubicación predeterminada de PG que necesita crear. Una vez que haya creado todas las ubicaciones necesarias, el botón Continuar estará activado.

1. (Opcional) Para dirigir la operación PG a ubicaciones adicionales, PG o que no sean PG, haga clic en ![Menú Opciones](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

>[!NOTE]
>
>Es posible adjuntar varias ubicaciones que admitan distintos tipos de (CTV, escritorio, audio, etc.) al mismo trato.

## Configuración manual de un acuerdo garantizado programático

Utilice este método para todos los demás SSP.

1. [Configuración manual de los detalles del ID de la oferta](deal-id-create.md).

1. Después de guardar la oferta, seleccione las publicidades que se utilizarán para la oferta y cree una colocación predeterminada de PG, según se le solicite.

   La creación de una colocación predeterminada de PG para la oferta es obligatoria para entregar el 100% de su compra. Este tipo de ubicación no tiene segmentación, por lo que DSP devolver una oferta a cada solicitud de oferta del editor.

1. (Opcional) Para dirigir la operación PG a ubicaciones adicionales, PG o que no sean PG, haga clic en ![Menú Opciones](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

>[!NOTE]
>
>Es posible adjuntar varias ubicaciones que admitan distintos tipos de (CTV, escritorio, audio, etc.) al mismo trato.


>[!MORELIKETHIS]
>
>* [Acerca de los Ofertas Garantizadas mediante Programación](programmatic-guaranteed-about.md)
>* [Sugerencias para negociar un acuerdo garantizado mediante programación](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Enviar una publicidad para un acuerdo garantizado programático con [!DNL FreeWheel]](freewheel-submit.md)
>* [Aceptar un acuerdo en la bandeja de entrada del Deal ID](deal-id-inbox-accept.md)
>* [Crear manualmente detalles de ID de acuerdo](deal-id-create.md)
>* [Socios de SSP](ssp-partners.md)
>* [Descripción general de las funciones de inventario](inventory-overview.md)

