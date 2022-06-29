---
title: Uso [!DNL Roku] Inventario
description: 'Obtenga información sobre DSP asociación con [!DNL Roku], incluidas las opciones de inventario, los proveedores de seguimiento de terceros aprobados y las prácticas recomendadas para [!DNL Roku]ubicaciones específicas de . '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Uso [!DNL Roku] Inventario

Advertising Cloud DSP proporciona funciones únicas para la publicidad en [!DNL Roku].

## Advertising Cloud DSP y [!DNL Roku] Asociación

Roku y Advertising Cloud DSP tienen una asociación única que coincide con su [!DNL DSP] audiencias a [!DNL Roku] ID para segmentación de audiencia determinista 1:1 en [!DNL Roku] inventario.

Fuera del propio DSP de Roku (OneView), Advertising Cloud DSP solo tiene acceso a estas capacidades de segmentación. Advertising Cloud DSP también es el único DSP con permiso para medir [!DNL Roku] al lado de todos los demás inventarios de TV conectada (CTV). Porque [!DNL Roku] no comparte todas las señales estándar de píxeles de impresión y RTB, ningún otro DSP puede dirigirse o medir en el suministro de CTV vendido por Roku.

## [!DNL Roku] Opciones de inventario

Puede: a) configurar ID de acuerdos privados directamente con [!DNL Roku] y, a continuación, introduzca los datos del ID de la oferta en DSP o b) visite la [!DNL On Demand] Galería para suscribirse [!DNL Roku] perfiles:

>[!NOTE]
>
>[!DNL Roku] el inventario no está disponible en mercados abiertos ni en intercambios.

* Para sus ofertas privadas, [configuración de información sobre los ID de oferta en DSP](/help/dsp/inventory/deal-id-create.md) y luego target &quot;[!UICONTROL Roku Network – Audience]&quot; y &quot;[!UICONTROL The Roku Channel – Audience]&quot; dentro de [!DNL Roku] ubicaciones.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Puede [suscríbase a lo siguiente [!DNL Roku] inventario dentro de [!DNL On Demand] Galería](/help/dsp/inventory/on-demand-inventory-subscribe.md)y, a continuación, establezca como objetivo cualquiera de los acuerdos aprobados dentro de [!DNL Roku] ubicaciones:

   * &quot;[!UICONTROL Roku Network – Audience]&quot; para el inventario en el [!DNL Roku] ecosistema con socios de contenido premium, como [!DNL The CW], [!DNL ABC]y [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; para [!DNL Roku] contenido de aplicación propiedad y gestionada (O&amp;O).

### Ventajas de personalizar los mercados privados con [!DNL Roku]

Las ofertas privadas permiten personalizar los parámetros de la oferta según sus necesidades.

* **Precio negociado:** Trabaje con el [!DNL Roku] equipo de ventas para negociar y estructurar un acuerdo que satisfaga las necesidades de su campaña.

* **Prioridad de escalado:** Los mercados privados (PMP) reciben mayor prioridad que las ofertas permanentes (por ejemplo, [!DNL On Demand] ofertas).

* **Administración de frecuencia:** La variable [!DNL Roku] el límite de frecuencia predeterminado es un (1) anuncio por 30 minutos por usuario, pero puede personalizar el límite por hora, día, semana, mes o período de vuelo completo.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Segmentación de datos:** [!DNL Roku] las audiencias se crean a partir de [!DNL Roku] señales de dispositivo y TV, datos rastreados por [!DNL The Roku Channel] (como afinidad de género de TV, comportamiento de transmisión por secuencias de TV y estado de suscripción de cable), y datos adicionales de la variable [!DNL Roku] sistema de administración de la relación con los clientes (CRM).

* **[!DNL Roku]Segmentación de contenido:** Las ofertas privadas pueden dirigirse a aplicaciones por género, aplicación de la lista de bloqueados de la aplicación, eventos estacionales y de prueba, y programas dentro de [!DNL The Roku Channel] solo.

## [!DNL Roku] Ubicaciones

En DSP campañas, [crear [!DNL Roku]-ubicaciones específicas](/help/dsp/campaign-management/placements/placement-create.md) utilizando el tipo de colocación &quot;[!UICONTROL Connected TV (Roku)].&quot; Incluir [!DNL Roku] ubicaciones en [!DNL Roku]-paquetes específicos con objetivos definidos.

Cada [!DNL Roku] La ubicación debe ser de al menos uno [!DNL Roku] oferta o fuente. Para usar la coincidencia de audiencia única de DSP con [!DNL Roku], incluya uno o más segmentos de audiencia que se puedan comparar con el [!DNL Roku] conjunto de datos determinísticos (incluido).

### [!DNL Roku]-Proveedores de seguimiento de terceros aprobados

[!DNL Roku] las ubicaciones pueden incluir píxeles de eventos de terceros y píxeles de conversión de los siguientes proveedores:  [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]y [!DNL Research Now].

### Prácticas recomendadas por estrategia de colocación

Las siguientes son las prácticas recomendadas para [!DNL Roku]ubicaciones específicas de .

Para maximizar el alcance incremental:

* Suprimir audiencias expuestas en [!DNL Roku O&O] excluyendo audiencias a las que ya ha llegado mediante [!DNL The Roku Channel].

* Suprimir audiencias expuestas en [!DNL All Roku] excluyendo audiencias a las que ya ha llegado en todo el [!DNL Roku] plataforma.

Para una configuración más rápida:

* Segmente ofertas existentes y siempre activas para [!DNL The Roku Channel] en [[!DNL On Demand] Inventario](/help/dsp/inventory/on-demand-inventory-subscribe.md) acceso rápido [!DNL Roku] inventario propiedad y explotado.
* Segmente ofertas existentes y siempre activas para [!DNL Roku Network] en [[!DNL On Demand] Inventario](/help/dsp/inventory/on-demand-inventory-subscribe.md) para alcanzar rápidamente la escala en todo el [!DNL Roku] plataforma.

Para la escala máxima:

* Personalización de un [!DNL Roku] mercado privado para acceso prioritario a [!DNL Roku] oferta a un precio negociado.

>[!MORELIKETHIS]
>
>* [Crear manualmente detalles de ID de acuerdo](/help/dsp/inventory/deal-id-create.md)
> * [Suscribirse y solicitar acceso a [!DNL On Demand] Ofertas de inventario Premium](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Crear una colocación](/help/dsp/campaign-management/placements/placement-create.md)

