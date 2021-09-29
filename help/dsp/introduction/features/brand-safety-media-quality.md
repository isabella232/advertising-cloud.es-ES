---
title: Seguridad de la marca y calidad de los medios
description: Obtenga más información sobre la seguridad de la marca y las funciones de calidad de los medios.
feature: DSP Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: cebe80fa8ed4f6410a7ea3ee7be6e0bf03631a49
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 0%

---

# Seguridad de la marca y calidad de los medios

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSP proporciona un conjunto de funciones de protección de marca para garantizar que cada una de las campañas llegue a usuarios reales en un entorno seguro para la marca.

Nuestro equipo de Vigilancia del Fraude trabaja estrechamente con socios líderes del sector, como [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] y [!DNL WhiteOps], para depurar cuidadosamente el inventario en nuestra plataforma. Mediante la administración proactiva de nuestro suministro, DSP garantiza que todos los anunciantes de la plataforma estén protegidos contra el tráfico no humano (bots, rastreadores, tráfico del centro de datos y fraude) y que se entreguen únicamente en contextos seguros para la marca.

Además de proporcionar una gestión de calidad central, creemos en que los anunciantes puedan diseñar los controles que se ajusten a su marca. Adobe Advertising Cloud ofrece integraciones con [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud] y [!DNL Peer39], lo que garantiza que cada anunciante pueda elegir el nivel deseado de protección contra el fraude, filtrado contextual y targeting de palabras clave.

## Iniciativas de calidad de Advertising Cloud DSP

### Verificación de inventario con compatibilidad con [!DNL Ads.txt]

[[!DNL Ads.txt], which stands for [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) es una iniciativa lanzada por el  [!DNL Interactive Advertising Bureau] ([!DNL IAB]) en junio de 2017 para facilitar la representación adecuada del inventario en el mercado abierto, combatiendo así fuentes ilegítimas de tráfico y falsificación de dominios. Los editores y distribuidores participantes declaran públicamente las empresas autorizadas para vender su inventario digital y la naturaleza de esas relaciones, manteniendo una `ads.txt` página en el nivel superior del dominio (como `example.com/ads.txt`).

DSP admite [!DNL ads.txt] leyendo el archivo `ads.txt` de cada publicador y dándole la opción de comprar solo de [!DNL ads.txt] vendedores verificados. Por ejemplo, al hacer coincidir los vendedores que vemos en el acceso `nytimes.com` al archivo `ads.txt` del New York Times, podemos identificar cuáles son legítimos y cuáles no, y bloquearemos los infractores si la ubicación está configurada para comprar solamente a vendedores verificados. <!-- can we actually mention NY Times? -->

Puede establecer controles [!DNL ads.txt] predeterminados para cada anunciante<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> y, opcionalmente, [personalizar la configuración de cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md) para:

* comprar inventario solo de vendedores directos autorizados de un dominio

* comprar inventario solo a vendedores y distribuidores directos autorizados de un dominio

* priorizar la compra de inventario desde los vendedores y distribuidores directos autorizados de un dominio

* comprar inventario de todos los vendedores

### Vigilancia del fraude de plataforma

DSP ha creado potentes herramientas y sistemas internos para administrar el fraude en nuestra plataforma, en asociación con los principales proveedores del sector, como [!DNL Whiteops] y [!DNL Integral Ad Science].

Además, Adobe trabaja estrechamente con [!DNL IAB] y [!DNL TAG] para garantizar un bloqueo sólido y estándar del sector para proteger a nuestros anunciantes, aprovechando herramientas como [!DNL ads.txt] (consulte la sección anterior), la lista [!DNL IAB] Bots and Spiders y la lista [!DNL TAG] IP del centro de datos.

Gracias a nuestro enfoque multidimensional de la calidad, nuestro equipo supervisa las anomalías y los patrones de tráfico no válidos, lo que garantiza menos del 3 % de tráfico no válido en el inventario protegido. Cualquier inventario sospechoso, incluido el inventario de dominios específicos o de editores o vendedores específicos, se bloquea inmediatamente en toda la plataforma.

### Asignación de inventario, Niveles y Categorización

La asignación de inventario es el proceso detallado de revisión e incorporación necesario para todo el inventario nuevo antes de añadirlo a nuestra plataforma. Este proceso está diseñado para garantizar la seguridad y calidad de todo el inventario de DSP.

* **Asignación:** nuestro equipo de inventario revisa cada dominio cuidadosamente, evaluando aspectos como:

   * Seguridad de la marca

   * Verificación del tipo de anuncio

   * Contenido genérico, dominios duplicados y servicio de publicidad falsa

* **Organización en niveles:** examinamos holísticamente la presencia de marca en el ecosistema general para clasificar el inventario en diferentes niveles. Puede [dirigir sus colocaciones](/help/dsp/campaign-management/placements/placement-settings.md) a estos niveles para el nivel de alcance deseado:

   * **[!UICONTROL T1]** - Nombres de marcas, sitios internacionalmente reconocibles

   * **[!UICONTROL T2]** : sitios de aspecto Bueno que son actuales, están actualizados, no tienen contenido generado por el usuario y, por lo general, no tienen reconocimiento global

   * **[!UICONTROL T3]** - Contenido generado por el usuario y contenido de nicho

* **Categorización de sitios:** para garantizar una segmentación y un bloqueo de contenido sencillo, etiquetamos cada propiedad con una categoría de sitio definida por Advertising Cloud basada en el contenido de la propiedad. Puede [establecer como objetivo o excluir estas categorías de sitio para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md) en función de los objetivos de ubicación.

### Compatibilidad completa con el bloqueo de sitios

Advertising Cloud DSP proporciona una lista de sitios bloqueados globalmente y la opción de crear listas de sitios bloqueados personalizadas para anunciantes y cuentas.

#### Lista de sitios bloqueados globalmente de Advertising Cloud DSP

Advertising Cloud DSP mantiene una lista de sitios bloqueados globalmente de los sitios considerados inseguros para ejecutar anuncios. Esta lista contiene sitios con contenido objetable (como odio o terror) y sitios infectados por bots, pre-roll falso, dominios sin coincidencia y otra actividad fraudulenta.

Como parte de nuestra iniciativa de seguridad de marca para erradicar las actividades que defraudan a los anunciantes, todos los sitios se analizan usando las medidas de la lista de sitios bloqueados del gráfico. Todos los sitios que no pasan las comprobaciones de seguridad de marca se agregan a la lista de sitios bloqueados globalmente. Dado que Advertising Cloud DSP administra esta lista de forma dinámica, los sitios pueden entrar o salir de la lista en cualquier momento, según el último análisis de seguridad de marca.

Cuando se incluye un sitio en la lista de sitios bloqueados globalmente como destino de ubicación, el sitio se marca con un signo de exclamación rojo (!). Esto indica que las publicidades no se ejecutarán en el sitio marcado.

#### Listas de sitios bloqueados a nivel de cuenta y anunciante

Los usuarios también pueden mantener las listas de sitios bloqueados a nivel de cuenta y de anunciante<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, que se utilizan automáticamente para todas las ubicaciones. La lista de sitios bloqueados de nivel inferior se aplica además de la lista de sitios bloqueados globalmente.

## Integraciones de terceros

### Filtrado contextual

El filtrado contextual le permite segmentar o bloquear oportunidades de publicidad en función del contexto de la página en la que serviría la publicidad. Adobe proporciona filtrado contextual mediante integraciones con los principales proveedores del sector: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] y [!DNL Peer39]. Algunos ejemplos de filtros actuales son [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] y [!UICONTROL G-rated Sites].

Puede establecer controles de filtro contextuales predeterminados para cada anunciante<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> y, opcionalmente, [personalizar la configuración de cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Al utilizar esta función, pueden aplicarse tarifas adicionales.

![Logotipo ](/help/dsp/assets/comscore-logo.png) ![ComscoreLogotipo DoubleVerifyLogotipo de ](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science ](/help/dsp/assets/ias-logo.png) ![logoPeer39](/help/dsp/assets/peer39-logo.png)

### Bloqueo de fraude de oferta previa

Aproveche nuestras integraciones de terceros con [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] y [!DNL Peer39] para bloquear el tráfico no humano de sus campañas. Estas integraciones proporcionan capacidades de bloqueo previo a la oferta líderes en el sector para minimizar el tráfico no válido general y sofisticado (GIVT y SIVT) en sus campañas.

Puede establecer controles predeterminados de bloqueo de fraude de oferta para cada anunciante<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> y, opcionalmente, [personalizar la configuración para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Al utilizar esta función, pueden aplicarse tarifas adicionales.

Para obtener más información sobre la funcionalidad, póngase en contacto directamente con el proveedor preferido o póngase en contacto con el administrador de cuentas de Adobe.

![Logotipo ](/help/dsp/assets/comscore-logo.png) ![ComscoreLogotipo DoubleVerifyLogotipo de ](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science ](/help/dsp/assets/ias-logo.png) ![logoPeer39](/help/dsp/assets/peer39-logo.png)

### Viewability Pre-Bid {#pre-bid-viewability}

Los filtros de visualización de ofertas anteriores ofrecidos por nuestros socios líderes en el sector [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) y [!DNL Integral Ad Science] permiten a los anunciantes garantizar que sus campañas cumplan con los objetivos de rendimiento de visualización deseados en todo el inventario de vídeo y visualización.

Puede establecer filtros de visualización predeterminados para cada anunciante<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> y, opcionalmente, [personalizar la configuración de cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Al utilizar esta función, pueden aplicarse tarifas adicionales.

![Logotipo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo de Oracle Advertising ](/help/dsp/assets/oracle-advertising-logo.png) ![Logotipo de integración de Ad Science](/help/dsp/assets/ias-logo.png)

### Segmentación de temas

DSP segmentación por temas le permite dirigirse o bloquear listas de palabras clave aprovechando nuestros socios contextuales líderes en la industria [!DNL Comscore] y [!DNL Oracle Data Cloud] ([!DNL Grapeshot]).

La segmentación por temas le ayuda a garantizar que los anuncios se proporcionen siempre en un entorno que se ajuste a su marca, ya sea bloqueando contenido dañino o asegurando que se gaste en un contexto que garantice un bueno resultado.

La segmentación por temas requiere que cree segmentos de temas directamente con [!DNL Comscore] o [!DNL Grapeshot] (mediante [!DNL Oracle Data Cloud]). Una vez creados en la plataforma del socio, puede [dirigirse o excluir un ID de segmento en la sección[!UICONTROL  Audience Targeting] para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). Se pueden aplicar tarifas adicionales para esta función.

Para empezar, póngase en contacto con su proveedor preferido o con el administrador de cuentas de Adobe.

![Logotipo de Comscore ](/help/dsp/assets/comscore-logo.png) ![logoGrapeshot](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP se ha asociado con [!DNL DoubleVerify] para ofrecer su solución de segmentación [!DNL Authentic Brand Safety], que le permite crear un conjunto centralizado de requisitos de seguridad de marca para dirigirse a todas las plataformas de compra con fines de coherencia.

Una vez que haya creado un segmento de seguridad de marca [!DNL DoubleVerify] con el objetivo necesario, puede utilizarlo en DSP para replicar las reglas de bloque posteriores a la oferta con ofertas previas en los entornos web.

Puede especificar un [!DNL DoubleVerify] ID de segmento para cada anunciante<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> y, opcionalmente, [habilitar o deshabilitar [!UICONTROL Authentic Brand Safety] para cada ubicación](/help/dsp/campaign-management/placements/placement-settings.md). DSP factura su cuenta por el uso del ID de segmento.

Para obtener más información sobre la funcionalidad, póngase en contacto directamente con [!DNL DoubleVerify] o póngase en contacto con el administrador de cuentas de Adobe.

![Logotipo DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
