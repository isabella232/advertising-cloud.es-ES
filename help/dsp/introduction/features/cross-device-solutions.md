---
title: Soluciones entre dispositivos
description: Obtenga más información sobre las funciones entre dispositivos.
feature: DSP Introduction
exl-id: 29f8ec41-35a6-4a29-a638-82a2929a8fe6
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# Soluciones entre dispositivos

La integración de Advertising DSP con [!DNL LiveRamp] permite ampliar la audiencia a todos los dispositivos conocidos de una persona, no solo a los dispositivos de su marca. La integración también proporciona restricción de frecuencia y medición de atribución en todos los dispositivos.

Al utilizar un gráfico de dispositivos basado en personas compatible, puede:

* Haga coincidir las audiencias de los canales y dispositivos para enviar anuncios a personas y hogares, en lugar de a dispositivos.
* Equilibrar la exposición publicitaria mediante la comprensión y restricción de la frecuencia entre individuos.
* Pruebe estrategias que expongan y conviertan audiencias entre canales o dispositivos.

## Ventajas de [!DNL LiveRamp] Gráfico de dispositivos

* Proporciona un grupo de datos determinísticos, que incluye datos de clientes sin conexión

* Proporciona cobertura uniforme entre ID de cookies e ID de dispositivos móviles

* Incluye datos procedentes principalmente de los Estados Unidos

* Es libre de restricción de frecuencia y medición de atribución

* Precio de 0,35 CPM de USD para impresiones extendidas (impresiones que se entregan únicamente mediante el uso de la variable [!DNL LiveRamp] gráfico de dispositivos en lugar de en dispositivos encontrados dentro de los segmentos de audiencia de destino)

   La tasa se refleja en la tarjeta de tasa de la cuenta.

## Administración de frecuencia basada en personas

La administración de frecuencias basada en personas permite especificar límites de frecuencia a nivel de persona, en lugar de a nivel de dispositivo, para un control de exposición real de medios.

### Activar la administración de frecuencia basada en personas

* **Campañas:** Al crear una nueva campaña, puede especificar una [!UICONTROL Cross-Device Level] configuración. Habilitar &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; y seleccione un gráfico de dispositivos. El gráfico de dispositivos especificado se utiliza tanto para la segmentación entre dispositivos en el nivel de ubicación como para la administración de frecuencias basada en personas en el nivel de campaña, paquete y ubicación. Los límites de frecuencia se aplican a todos los dispositivos conocidos de una persona.

Para obtener más información, consulte [Configuración de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Una vez guardada una campaña, no se puede cambiar su [!UICONTROL Cross Device Level] configuración.

* **Paquetes:**  Opcionalmente, puede establecer límites de frecuencia adicionales en el nivel del paquete. DSP respetará el límite de frecuencia más estricto de la jerarquía de campañas.

* **Ubicaciones:** Si lo desea, puede establecer límites de frecuencia adicionales en el nivel de ubicación. DSP respetará el límite de frecuencia más estricto de la jerarquía de campañas.

## Segmentación basada en personas

La segmentación basada en personas le permite encontrar clientes en equipos de escritorio y móviles.

### Activar Segmentación basada en personas

* **Campañas:** Al crear una nueva campaña, puede especificar una [!UICONTROL Cross-Device Level] configuración. Habilitar &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; y seleccione un gráfico de dispositivos. El gráfico de dispositivos especificado se utiliza tanto para la segmentación entre dispositivos en el nivel de ubicación como para la administración de frecuencias basada en personas.

Para obtener más información, consulte [Configuración de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Ubicaciones:** Cuando selecciona segmentos de audiencia para una colocación en una campaña con un gráfico de dispositivos especificado, una [!UICONTROL Cross-Device Targeting] permite ampliar los objetivos a todos los dispositivos conocidos de una persona (según el gráfico de dispositivos especificado en la configuración de campaña), incluso a los dispositivos que no están en los segmentos especificados.

### Configuración de informes para segmentación basada en personas

Puede incluir las métricas siguientes en los informes personalizados:

* **Impresiones extendidas:** (En el [!UICONTROL Build Your Report] sección bajo [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) El volumen de impresiones incrementales que se entrega aprovechando un gráfico de dispositivos (y que no se encuentra dentro de los segmentos de audiencia originales). Esta métrica también se utiliza para calcular las tarifas aplicables asociadas con el uso de un gráfico de dispositivos de terceros.

   Para determinar el coste de las impresiones extendidas durante un período de tiempo, ejecute un informe personalizado que incluya la variable [!UICONTROL Extended Impressions] y luego multiplicar el número total de impresiones extendidas por 0,00035 $ (0,35 $/1000 impresiones).

   El coste agregado también se incluye en la variable [!UICONTROL Billable Other Net Spend] en [!UICONTROL Metrics] > [!UICONTROL Spend]), aunque esa métrica también incluye otras tarifas de campaña que podría haber añadido.

* **Device Graph:** (En el [!UICONTROL Build Your Report] sección bajo [!UICONTROL Dimensions] > [!UICONTROL Campaign]) El gráfico de dispositivos seleccionado para una campaña, paquete o ubicación en particular.

## Medición de atribución basada en personas

*Anunciantes con solo seguimiento de conversión de publicidad de Adobe*

Con la atribución basada en personas, puede atribuir conversiones que se produjeron en un dispositivo diferente al dispositivo en el que se produjo la exposición al contenido. La medición de atribución basada en personas está disponible en DSP, [!DNL Adobe Advertising Creative]y [!DNL Adobe Advertising Search] para anunciantes que hayan implementado píxeles de conversión de publicidad de Adobe en sus sitios.

### Habilitar la medición de atribución basada en personas

Si desea activar la medición de atribución entre dispositivos, póngase en contacto con su [!DNL Adobe] equipo de la cuenta.

### Configurar informes de conversión para la atribución de conversión entre dispositivos

#### Configuración de informes de conversión

Cuando un gráfico de dispositivo está habilitado para la medición de atribución, la variable [!UICONTROL Conversion] El informe incluye un [!UICONTROL Cross-Device Breakout] , que le permite incluir hasta tres columnas independientes para cada métrica de conversión, entre las que se incluyen:

* &lt;*Conversión*>[!UICONTROL (tp)]: Incluye las conversiones totales (personas totales), que incluyen conversiones entre dispositivos y entre dispositivos (si corresponde). En el informe, &quot;[!UICONTROL (tp)]&quot; se anexa al nombre de la métrica de conversión, al tipo de regla y a los tipos de conversión en la ruta de conversión (por ejemplo, &quot;Responses(le)(tl)(tp)&quot;).

* &lt;*Conversión*>[!UICONTROL (sd)]: (Opcional) Solo incluye conversiones para las que se rastreó un solo dispositivo en la ruta de conversión. En el informe, &quot;[!UICONTROL (sd)]&quot; se anexa al nombre de la métrica de conversión, el tipo de regla y los tipos de conversión en la ruta de conversión (por ejemplo, &quot;Responses(le)(tl)(sd)&quot;).

* &lt;*Conversión*>[!UICONTROL (xd)]: (Opcional) Solo incluye conversiones para las que se ha realizado un seguimiento de más de un dispositivo en la ruta de conversión. En el informe, &quot;[!UICONTROL (xd)]&quot; se anexa al nombre de la métrica de conversión, el tipo de regla y los tipos de conversión en la ruta de conversión (por ejemplo, &quot;Responses(le)(tl)(xd)&quot;).

#### Cómo interpretar el informe de conversión

Si ordena el porcentaje de conversiones totales entre dispositivos ([!UICONTROL (xd)]/[!UICONTROL (tl)]) de mayor a menor, comprenderá lo que está impulsando conversiones entre dispositivos superiores a la media. Puede utilizarlo para informar a su estrategia creativa o de segmentación a fin de que la mensajería y la inversión de canal coincidan con el comportamiento del usuario.

* Paquetes : ver qué paquetes generan la mayor cantidad de conversiones totales y cuáles tienen un alto porcentaje de conversiones entre dispositivos. Esto puede ayudarle a comprender dónde concentrar el gasto.

* Ubicaciones : Compare el rendimiento de la ubicación y la atribución (por ejemplo, un anuncio web móvil puede generar conversiones en el escritorio). Sin un gráfico del dispositivo para la atribución, puede perder el impacto de una ubicación web móvil en las conversiones del escritorio, o puede quedar enterrado si la mayoría de los usuarios convierte en escritorio y no en web móvil.

* Anuncios : Descubra qué anuncios generan mayores conversiones y cuantifique su valor y su impacto tanto en los navegadores web como en los entornos de aplicaciones móviles.

* Sitios : optimice los sitios en lugar de excluirlos manualmente por completo. Si un sitio web genera conversiones entre dispositivos, puede ver en qué dispositivos se produce este comportamiento.

* Ofertas : mejore la optimización manual comprobando qué ofertas de inventario proporcionan conversiones entre dispositivos y luego decidiendo si debe ampliar el objetivo para incluir más dispositivos y canales en esas ofertas.

>[!MORELIKETHIS]
>
>* [Configuración de informes](/help/dsp/reports/report-settings.md)
>* [Configuración de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)

