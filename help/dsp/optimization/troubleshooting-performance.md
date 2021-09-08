---
title: Resolución de problemas del rendimiento
description: Consulte problemas comunes de rendimiento y vea cómo solucionarlos.
feature: Optimization
exl-id: adb32257-dede-4623-9840-33221c218443
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Resolución de problemas del rendimiento

| Problema | Posible causa | Acciones que hay que emprender |
| --- | --- | --- |
| Sin gasto en colocación | La ubicación no incluye anuncios o los anuncios no están activos. | Compruebe que todos los anuncios esperados estén adjuntos a la ubicación y que estén aprobados y activos.<br><br>Además, compruebe si la ubicación incluye un programa de anuncios personalizado, que puede limitar el período de vuelo de cada anuncio. Para ver la programación de anuncios de una ubicación en la vista Ubicaciones, haga clic en **[!UICONTROL ...]>[!UICONTROL Ad schedule]** junto al nombre de la ubicación. |
|  | Las fechas afectadas no están dentro de las fechas de vuelo configuradas. | Compruebe que las fechas de vuelo sean válidas en los niveles de campaña, paquete y ubicación &#x200B; s. |
|  | El objetivo presupuestario se ha cumplido o no es lo suficientemente alto. | Compruebe la configuración del presupuesto en los niveles de campaña, paquete y ubicación. |
|  | La cuenta no tiene suficiente financiamiento. | Para ver si la cuenta está suficientemente financiada, vaya a **[!UICONTROL Settings]>[!UICONTROL Account]** y observe la cantidad de [!UICONTROL Usable Funds]. Si necesita añadir más fondos, póngase en contacto con el administrador de cuentas de Adobe. |
|  | No hay inventario disponible. | Compruebe si los orígenes de inventario especificados ([!UICONTROL Public], [!UICONTROL Private] o [!UICONTROL On Demand]) son:<ul><li>Configure correctamente.</li><li>Activo y enviando mediante subastas.</li><li>Compatible con el tipo de anuncio y colocación aplicable.</li></ul><br>Si todos los orígenes de inventario son válidos y están activos, establezca como objetivo fuentes de inventario adicionales o todas las fuentes de inventario siempre que sea posible. |
|  | No hay usuarios disponibles. | Compruebe que los objetivos de audiencia especificados incluyan suficientes usuarios activos. Si no lo hacen, amplíe los objetivos añadiendo más audiencias. |
| Baja inversión en ubicación | La sección [!UICONTROL Non Bids] del informe de diagnósticos de ubicación muestra las posibles razones por las que la colocación no se ofertó. | [Revise el  [!UICONTROL Non Bids] ](/help/dsp/campaign-management/reports/placement-diagnostics.md) informe para comprender por qué no se pujó la ubicación.   <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | La ubicación utiliza [filtros de oferta previa](/help/dsp/campaign-management/placements/placement-settings.md) que limitan las ofertas. | Reduzca en un 5% los umbrales de los filtros previos a la oferta para evaluar el equilibrio de gasto y rendimiento. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Tenga en cuenta que el uso de varios objetivos de ubicación, como filtros de oferta previa, geográficos, inventario y audiencias, puede limitar de forma acumulativa la oferta y el gasto. |
|  | La colocación tiene una baja tasa de ganancia. | Aumente el [!UICONTROL Max Bid] para mejorar la tasa de ganancia.<br><br><b>NOTA:</b>  Los precios de inventario pueden variar en función de la orientación de la ubicación.<br><br>Una tasa de 10% de ganancia se considera saludable. |
|  | Hay un número bajo de inventarios disponibles. | Segmente fuentes de inventario adicionales o todas ellas si es posible.<br><br>Tenga en cuenta que el uso de varios objetivos de ubicación, como filtros de oferta previa, geográficos, inventario y audiencias, puede limitar de forma acumulativa la oferta y el gasto. |
|  | Hay un número bajo de usuarios disponibles. | Compruebe que los objetivos de audiencia especificados incluyan suficientes usuarios activos. Si no lo hacen, amplíe los objetivos añadiendo más audiencias.<br><br>Tenga en cuenta que el uso de varios objetivos de ubicación, como filtros de oferta previa, geográficos, inventario y audiencias, puede limitar de forma acumulativa la oferta y el gasto. |
|  | El paquete incluye un gran número de ubicaciones activas. | Reduzca el número de ubicaciones activas dentro del paquete o aumente el presupuesto general del paquete.<br><br>Si el paquete tiene muchas ubicaciones, pero no presupuesto suficiente, DSP puede que no pueda asignar un presupuesto suficiente a cada ubicación. Cada ubicación debe tener la oportunidad de gastar al menos 2 USD/día. Por ejemplo, si su paquete tiene un presupuesto de 10 USD/día, entonces es mejor incluir cinco o menos ubicaciones. &#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md)

