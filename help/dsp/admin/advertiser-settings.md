---
title: Configuración de la cuenta del anunciante
description: Consulte las descripciones de la configuración del anunciante disponible.
source-git-commit: ee5621329aacf54777d28fa1c1f3d50949824cee
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 0%

---

# Configuración de la cuenta del anunciante

*No disponible para usuarios de solo lectura*

## [!UICONTROL General] Configuración

**[!UICONTROL Advertiser Name]:** El nombre del anunciante.

**[!UICONTROL Category]:** Categoría en la que opera el negocio del anunciante. La categoría se comunica a los editores cuando realiza una oferta en el inventario. Asegúrese de elegir una categoría que se ajuste a sus publicidades, o los editores pueden rechazar las publicidades.

>[!NOTE]
>
>Si selecciona *[!UICONTROL Other]*, el anunciante no podrá acceder a DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** La página principal del anunciante o la URL del sitio web principal (comenzando por `http://` o `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Solo cuentas de anunciante nuevas) Pone a disposición del anunciante todas las fuentes de intercambio privadas configuradas para la cuenta de DSP de la organización.

### [!UICONTROL Adobe IMS IDs]

Los anunciantes con productos adicionales de Adobe Experience Cloud pueden compartir datos entre algunos productos utilizando el [!DNL Organization ID] para Experience Cloud. Puede configurar integraciones de productos específicas en la [!UICONTROL Integrations] para obtener más información.

**[!UICONTROL Account IMS org and ID]:** (Anunciantes con productos Experience Cloud adicionales con licencia a través de una cuenta Experience Cloud con varios anunciantes); (opcional) el Experience Cloud de la cuenta [!DNL Organization ID].

**[!UICONTROL Advertiser IMS org and ID]:** (Anunciantes con licencias directas para productos Experience Cloud adicionales; (opcional) el Experience Cloud del anunciante [!DNL Organization ID].

### [!UICONTROL Integrations]

(Opcional) Productos de Experience Cloud adicionales vinculados a la cuenta de DSP. Los productos deben estar asociados al mismo Experience Cloud [!DNL Organization ID] en el [!UICONTROL Adobe IMS IDs] para obtener más información.

**[!UICONTROL Adobe Media Optimizer]:** (Anunciantes con Advertising Cloud Search o que utilizan píxeles de conversión de Advertising Cloud) A [!DNL Search] cuenta con la que DSP intercambiar datos de atribución.

**[!UICONTROL Adobe Device Co-op or 3rd Party Graph]:** (Anunciantes que utilizan píxeles de conversión de Advertising Cloud; (opcional) puede usar un gráfico del dispositivo para la medición de atribución basada en personas desde la configuración de cuenta del anunciante en Advertising Cloud Search.

>[!NOTE]
>
> * La atribución de dispositivo solo está disponible para conversiones rastreadas mediante el servicio de seguimiento de conversión de Advertising Cloud, no para conversiones rastreadas por Adobe Analytics.
> * También puede seleccionar un gráfico de dispositivos basado en personas para la segmentación entre dispositivos y la administración de frecuencia en la variable [nivel de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md). A continuación, puede configurar la segmentación entre dispositivos en la variable [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md) y los límites de frecuencia adicionales en el [nivel de paquete](/help/dsp/campaign-management/packages/package-settings.md) y [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md). La segmentación entre dispositivos y la administración de frecuencias no requieren medición de atribución a nivel de anunciante; en su lugar, funcionan con el gráfico del dispositivo especificado en la configuración de la campaña.


**[!UICONTROL Adobe Analytics]:** (Anunciantes con Adobe Analytics; opcional; solo aplicable a los datos recopilados mediante etiquetas de seguimiento de conversión de Advertising Cloud que incluyan un [!DNL EF Redirect] y solo token) Uno o más [!DNL Analytics] grupos de informes a los que DSP enviarán datos que recopila de editores y socios de suministro. Analytics también enviará los datos que recopila del sitio del cliente a DSP.

Para que los datos aparezcan en los grupos de informes, la variable [!DNL Search] configuración de nivel de anunciante en &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; debe estar habilitado. Además, el [!DNL Analytics] debe configurarse para recibir datos de Advertising Cloud. <!-- from Advertising Cloud or DSP in particular? Add cross-reference to file in Integrations section. -->

>[!WARNING]
>
>Si elimina un grupo de informes previamente vinculado, ya no DSP intercambiarán datos con ese grupo. Espere ver las fluctuaciones de los datos. <!-- Fluctuations where? Clarify -->

**[!UICONTROL Adobe Analytics Cloud]:** (Anunciantes con Adobe Audience Manager o Adobe Analytics; opcional) Un Audience Manager o [!DNL Analytics] cuenta desde la cual DSP extraerá metadatos de segmento, datos de jerarquía y datos de audiencia únicos para todas las audiencias de Adobe del anunciante. Esto incluye datos para:

* segmentos del Audience Manager
* [!DNL Analytics] segmentos que se publican en Adobe Experience Cloud
* Segmentos que se crean en Adobe Experience Cloud usando la variable [!DNL People core service]
* Segmentos que se crean en Adobe Experience Platform y se envían a Advertising Cloud mediante Audience Manager

La sincronización inicial tarda unas 24 horas. Después, los datos se sincronizan en tiempo real con un retraso de uno a dos segundos.
<!-- I don't think this is true anymore:
Segment membership data is sent to Advertising Cloud only after one of the following:

* The segment is targeted in an Advertising Cloud placement or audience library
* The segment is added to the Advertising Cloud batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Configuración

Si lo desea, puede configurar los objetivos predeterminados para las nuevas ubicaciones del anunciante. Los usuarios pueden anular los objetivos predeterminados para cualquier ubicación nueva.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** El país predeterminado para la segmentación geográfica de cada ubicación. Los usuarios pueden cambiar el país y configurar targeting geográfico más específico para cada ubicación.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Cualquier audiencia o segmento que se va a suprimir de forma predeterminada. Los usuarios pueden cambiar las exclusiones de cada ubicación.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

Tipos de [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]y [!DNL Peer39] filtros contextuales que se van a aplicar. Puede anular la configuración de nivel del anunciante en la variable [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de contexto de inventario que se van a bloquear de forma predeterminada. Pueden aplicarse tarifas adicionales.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Opcional) Uno o más tipos de atributos de inventario a los que dirigirse de forma predeterminada. Pueden aplicarse tarifas adicionales.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de atributos de inventario que se van a bloquear de forma predeterminada. Pueden aplicarse tarifas adicionales.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Opcional) El grado de contenido adulto para el que se bloquean los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (predeterminado), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Pueden aplicarse tarifas adicionales.

**[!UICONTROL Alcohol Content]:** (Opcional) El grado de contenido de alcohol para el que se bloquean los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (predeterminado), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Pueden aplicarse tarifas adicionales.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Tipos de sitios para bloquear según tráfico fraudulento y actividades sospechosas medidas mediante [!DNL DoubleVerify], [!DNL Integral Ad Science]y [!DNL Peer39]. Puede anular la configuración de nivel del anunciante en la variable [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** De forma predeterminada, bloquea todo el tráfico no válido al 100 %, incluido el tráfico en dispositivos secuestrados, para nuevas ubicaciones. Pueden aplicarse tarifas adicionales.

**[!UICONTROL Also block sites with]:** (Opcional) Un nivel adicional de fraude y tráfico no válido que hará que los DSP bloqueen las publicidades de forma predeterminada:  *[!UICONTROL None]* (el valor predeterminado, que no bloquea el tráfico adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* o *[!UICONTROL >25% Average Fraud/IVT levels]*. Pueden aplicarse tarifas adicionales.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de fraude que harán que los DSP bloqueen las publicidades de forma predeterminada: *[!UICONTROL Fraud]* (que bloquea todos los sitios con fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* y/o *[!UICONTROL Fraud: Zero Ads]*. Pueden aplicarse tarifas adicionales.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Opcional) Tipo de actividad sospechosa de un sitio web o aplicación que hará que los DSP bloqueen los anuncios de forma predeterminada: *[!UICONTROL None]* (el valor predeterminado, que no bloquea anuncios basados en actividades sospechosas), *[!UICONTROL Suspicious Activity - High Risk]* o *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Pueden aplicarse tarifas adicionales.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** De forma predeterminada, ¿qué nivel de [[!DNL Ads.txt] filtrado previo a la oferta](https://iabtechlab.com/ads-txt-about/) para usar mediante el uso de las [!DNL Authorized Digital Sellers] lista:
* *[!UICONTROL Opt out of ads.txt (default)]*: Para comprar inventario de todos los vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Para priorizar la compra de inventario de vendedores y distribuidores directos autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: Para comprar inventario únicamente a vendedores y distribuidores directos autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: Para comprar inventario únicamente a vendedores directos autorizados de un dominio.

Puede anular la configuración de nivel de anunciante en la variable [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** De forma predeterminada, habilita un filtro posterior a la oferta en tiempo real para garantizar que la publicidad se muestre en los sitios a los que se dirige el anunciante. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] solo clientes; (opcional) el ID de segmento de seguridad de marca asociado con el [!DNL DoubleVerify] cuenta.

**[!UICONTROL Enable Authentic Brand Safety]:** (Opcional) De forma predeterminada, habilita [!DNL DoubleVerify] Seguridad de marca auténtica, que bloquea las impresiones después de la oferta mediante las reglas de seguridad de marca personalizadas configuradas para el ID de segmento especificado. DSP factura su cuenta por el uso del ID de segmento.

Puede anular la configuración de nivel del anunciante en el nivel de ubicación.

>[!MORELIKETHIS]
>
>* [Crear una cuenta de anunciante](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
