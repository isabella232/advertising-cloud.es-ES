---
title: Uso de [!DNL Roku] Inventory
description: 'Obtenga información sobre DSP asociación con ubicaciones específicas de [!DNL Roku], including inventory options, approved third-party tracking vendors, and best practices for [!DNL Roku]. '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Uso del inventario [!DNL Roku]

Advertising Cloud DSP proporciona funciones únicas para la publicidad en [!DNL Roku].

## La asociación de Advertising Cloud DSP y [!DNL Roku]

Roku y Advertising Cloud DSP tienen una asociación única que coincide con sus [!DNL DSP] audiencias en [!DNL Roku] ID para la segmentación de audiencia determinística 1:1 en el inventario [!DNL Roku].

Fuera del propio DSP de Roku (OneView), Advertising Cloud DSP solo tiene acceso a estas capacidades de segmentación. Advertising Cloud DSP también es el único DSP con permiso para medir el suministro [!DNL Roku] junto al resto del inventario de TV conectada (CTV). Dado que [!DNL Roku] no comparte todas las señales estándar de RTB y píxeles de impresión, ningún otro DSP puede dirigirse o medir en el suministro de CTV vendido por Roku.

## [!DNL Roku] Opciones de inventario

Puede: a) configurar los ID de acuerdo privados directamente con [!DNL Roku] e introducir los datos del ID de acuerdo en DSP o b) visitar la Galería [!DNL On Demand] para suscribirse a los perfiles [!DNL Roku]:

>[!NOTE]
>
>[!DNL Roku] el inventario no está disponible en mercados abiertos ni en intercambios.

* Para sus ofertas privadas, [configurará información sobre los ID de la oferta en DSP](/help/dsp/inventory/deal-id-create.md) y luego dirigirá &quot;[!UICONTROL Roku Network – Audience]&quot; y &quot;[!UICONTROL The Roku Channel – Audience]&quot; dentro de las ubicaciones [!DNL Roku].<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Puede [suscribirse a la siguiente [!DNL Roku] inventory within the [!DNL On Demand] Galería](/help/dsp/inventory/on-demand-inventory-subscribe.md) y luego dirigirse a cualquiera de las ofertas aprobadas dentro de [!DNL Roku] ubicaciones:

   * &quot;[!UICONTROL Roku Network – Audience]&quot; para inventario en todo el ecosistema [!DNL Roku] con socios de contenido premium, como [!DNL The CW], [!DNL ABC] y [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; para el contenido de la aplicación [!DNL Roku] que se posee y gestiona (O&amp;O).

### Ventajas de personalizar Mercados Privados con [!DNL Roku]

Las ofertas privadas permiten personalizar los parámetros de la oferta según sus necesidades.

* **Precio negociado:** trabaje con el equipo de  [!DNL Roku] ventas para negociar y estructurar un acuerdo que satisfaga las necesidades de su campaña.

* **Prioridad de la escala:** los mercados privados (PMP) reciben mayor prioridad que las ofertas permanentes (como las  [!DNL On Demand] ofertas).

* **Administración de frecuencia:** el límite de frecuencia  [!DNL Roku] predeterminado es un (1) anuncio por 30 minutos por usuario, pero puede personalizar el límite por hora, día, semana, mes o período de vuelo completo.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Segmentación de datos:** [!DNL Roku] las audiencias se crean a partir de señales de  [!DNL Roku] dispositivo y TV, datos rastreados por  [!DNL The Roku Channel] (como afinidad de género de TV, comportamiento de transmisión por TV y estado de suscripción de cable) y datos adicionales del sistema de administración de la relación con los  [!DNL Roku] clientes (CRM).

* **[!DNL Roku]Segmentación de contenido:** las ofertas privadas pueden dirigirse a aplicaciones por género, aplicación de la lista de bloqueados de la aplicación, eventos de temporada y de tentpole, y mostrarse  [!DNL The Roku Channel] solo en.

## [!DNL Roku] Ubicaciones

En DSP campañas, [creará  [!DNL Roku] ubicaciones específicas](/help/dsp/campaign-management/placements/placement-create.md) utilizando el tipo de ubicación &quot;[!UICONTROL Connected TV (Roku)]&quot;. Incluirá [!DNL Roku] ubicaciones en paquetes específicos de [!DNL Roku] con objetivos definidos.

Cada ubicación [!DNL Roku] debe dirigirse al menos a una [!DNL Roku] oferta o fuente. Para aprovechar la coincidencia de audiencias únicas de DSP con [!DNL Roku], incluya uno o más segmentos de audiencia que se puedan comparar con el conjunto de datos determinísticos [!DNL Roku] (integrado).

### [!DNL Roku]-Proveedores de seguimiento de terceros aprobados

[!DNL Roku] las ubicaciones pueden incluir píxeles de eventos de terceros y píxeles de conversión de los siguientes proveedores:   [!DNL Acxiom],  [!DNL comScore],  [!DNL Data Plus Math],  [!DNL Experian],  [!DNL Factual],  [!DNL Kantar],  [!DNL Marketing Evolution],  [!DNL Neustar],  [!DNL Nielsen],  [!DNL Nielsen Catalina Solutions],  [!DNL NinthDecimal],  [!DNL Oracle],  [!DNL Placed],  [!DNL Polk] y  [!DNL Research Now].

### Prácticas recomendadas por estrategia de colocación

A continuación se indican las prácticas recomendadas para las ubicaciones específicas de [!DNL Roku].

Para maximizar el alcance incremental:

* Elimine las audiencias expuestas en [!DNL Roku O&O] excluyendo las audiencias a las que ya ha llegado mediante [!DNL The Roku Channel].

* Elimine las audiencias expuestas en [!DNL All Roku] excluyendo las audiencias a las que ya ha llegado en la plataforma [!DNL Roku].

Para una configuración más rápida:

* Segmente las ofertas existentes y siempre activas para [!DNL The Roku Channel] en [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md) para acceder rápidamente al [!DNL Roku] inventario que se posee y se gestiona.
* Segmente ofertas existentes y siempre activas para [!DNL Roku Network] en [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md) para lograr rápidamente escalas en la plataforma [!DNL Roku].

Para la escala máxima:

* Personalice un [!DNL Roku] mercado privado para obtener acceso prioritario a [!DNL Roku] suministro a un precio negociado.

>[!MORELIKETHIS]
>
>* [Crear manualmente detalles de ID de acuerdo](/help/dsp/inventory/deal-id-create.md)
> * [Suscribirse y solicitar acceso  [!DNL On Demand] a ofertas de inventario Premium](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Crear una colocación](/help/dsp/campaign-management/placements/placement-create.md)

