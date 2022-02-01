---
title: Acerca de la gestión de público en Advertising Cloud DSP
description: Obtenga información sobre las funciones de gestión de público.
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# Acerca de la gestión de público en Advertising Cloud DSP

En Advertising Cloud DSP, puede crear y administrar segmentos de audiencia y conjuntos de audiencias, que puede usar como destinatarios para sus ubicaciones:

* Puede recopilar sus propios datos de audiencia de origen creando e implementando segmentos. Posteriormente, puede redirigirse a los usuarios del segmento mediante anuncios o evitar que los usuarios del segmento reciban anuncios. Puede crear los siguientes tipos de segmentos:

   * [Segmentos personalizados](/help/dsp/audiences/custom-segment-create.md) para rastrear a) usuarios expuestos a anuncios de dispositivos de escritorio, móviles y CTV y b) usuarios que visitan páginas web específicas.

   * [Segmentos de exclusión de CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) para realizar un seguimiento de los ID de usuario procedentes de solicitudes de exclusión de venta de consumidores en su sitio web, según la Ley de privacidad del consumidor de California (CCPA). Puede recuperar informes mensuales de los ID de usuario a partir de solicitudes de exclusión de venta.

      Para obtener más información sobre la compatibilidad de Advertising Cloud con las solicitudes de exclusión de CCPA, consulte [Compatibilidad de Adobe Advertising Cloud con la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión del consumidor](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html).

* Puede crear una biblioteca de audiencias de [audiencias reutilizables](/help/dsp/audiences/reusable-audience-create.md). Las audiencias guardadas se componen de cualquiera de los segmentos de audiencia disponibles y de cualquiera de las otras audiencias guardadas. Cualquier cambio que realice en una audiencia guardada se aplicará automáticamente a todas las ubicaciones que segmenten o excluyan la audiencia y a todas las demás audiencias que incluyan la audiencia guardada.

   Las audiencias guardadas permiten a los planificadores de medios agrupar las audiencias según sea necesario, incluyendo y excluyendo varios segmentos mediante lógica booleana compleja. El tamaño de cada segmento individual y el tamaño total de la audiencia se indican a medida que crea una audiencia. Los ejecutores de Campaign pueden seleccionar una o más audiencias guardadas como destinos de ubicación en lugar de configurar manualmente los destinos de audiencia para cada ubicación.

También hay disponibles tipos de audiencia adicionales para la segmentación de ubicación.

## Importación de segmentos de datos de origen y de terceros

Advertising Cloud DSP puede importar sus propios segmentos de datos de origen desde su plataforma de administración de datos (DMP) y proporcionarlos a cualquier conjunto de anunciantes, según sea necesario.

Advertising Cloud DSP también puede importar segmentos de terceros personalizados, incluidas combinaciones complejas de segmentos de terceros. Puede proporcionar los segmentos a cualquier conjunto de anunciantes, según sea necesario.

Póngase en contacto con su [!DNL Adobe] equipo de cuenta para obtener más información.

## Audiencias disponibles como destinos de colocación

Puede dirigir las ubicaciones a todos los tipos de audiencias siguientes.

* Todos los conjuntos de audiencias creados por el usuario que se guardaron en Advertising Cloud DSP.

* Todos los segmentos de audiencia creados por el usuario que se crearon en Advertising Cloud DSP:

   * Segmentos personalizados para usuarios que visitaron páginas web específicas y usuarios expuestos a impresiones de anuncios específicos.

   * Segmentos de audiencia de exclusión de la venta de CCPA para usuarios que han enviado solicitudes de exclusión de la venta en su sitio web, según la Ley de privacidad del consumidor de California (CCPA).

* Todos los segmentos de datos de origen importados.

* Todos los segmentos de datos de terceros personalizados importados.

* (Ubicaciones dirigidas solo a EE. UU.) [Todos los segmentos de datos de terceros disponibles para clientes de Advertising Cloud DSP de más de 30 proveedores](/help/dsp/audiences/third-party-data-providers.md), incluyendo [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast], y muchos más.

   Puede dirigirse a segmentos específicos, que se dirigen a usuarios según los datos de audiencia (por ejemplo, usuarios con datos demográficos, intereses o intenciones específicos y/o perfiles de comportamiento). Puede examinar por proveedor y categoría de datos, buscar segmentos por nombre o ID de segmento, o filtrar los resultados por proveedor de datos, tamaño total del segmento, recuento del explorador web o recuento de dispositivos.

   Los segmentos de terceros incurren en tarifas adicionales, que se indican junto al nombre de cada segmento.

* (Anunciantes con Adobe Experience Cloud, Adobe Audience Manager o Adobe Analytics que solo usan etiquetas de conversión de JavaScript de Advertising Cloud) Todos los segmentos de audiencia de origen, segundo o terceros disponibles creados en Adobe Experience Cloud, creados en Audience Manager o publicados en Adobe Experience Cloud desde Audience Manager o [!DNL Analytics].

   Los precios para el uso de los segmentos se negocian previamente y no son visibles en Advertising Cloud.  <!-- Verify -->

   Los segmentos de Adobe Experience Cloud están disponibles aproximadamente una hora después de crearlos o publicarlos en Adobe Experience Cloud. Los segmentos procedentes directamente de Audience Manager están disponibles unas 24 horas después de crearlos. <!-- Verify all -->

   >[!NOTE]
   >
   >Consulte la documentación para [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html)y [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) para obtener información sobre la configuración y recopilación de datos para segmentos en esas soluciones.

## Datos de tamaño de audiencia

Dentro de la configuración de audiencia y la configuración de ubicación guardadas, puede ver datos detallados sobre el tamaño de la audiencia:

* Se muestra el tamaño total y activo de la audiencia deduplicada en todos los segmentos seleccionados y las audiencias guardadas, y puede ver los detalles por tipo de dispositivo (explorador, móvil o TV conectada).

   ![el tamaño de audiencia combinado](/help/dsp/assets/audience-size.png)

* Para segmentos individuales y audiencias guardadas, el tamaño total de audiencia y el CPM (cuando corresponda) se muestran junto al nombre del segmento. Puede ver más detalles sobre el segmento, incluido el tamaño por tipo de dispositivo (explorador, móvil o TV conectada). Para audiencias guardadas, el tamaño total es el total deduplicado.

   ![el tamaño del segmento individual](/help/dsp/assets/audience-size-segment.png)

## Vistas de audiencias

### La vista Todas las audiencias

En el [!UICONTROL All Audiences] vista o Biblioteca de audiencias, puede guardar y administrar audiencias reutilizables, que incluyen grupos de segmentos de audiencia e incluso otras audiencias guardadas. Las audiencias se pueden usar como destinos para varias ubicaciones. El número de ubicaciones en las que se utiliza cada audiencia se indica junto al nombre de la ubicación.

Puede editar, clonar, eliminar, exportar o compartir cualquier audiencia.

### La vista Segmentos

En el [!UICONTROL Segments] todos los usuarios pueden crear segmentos personalizados adicionales.

La variable [!UICONTROL Segments] la vista también enumera los siguientes tipos de segmentos:

* Todos los segmentos personalizados creados por el usuario están disponibles para el usuario.

   Puede ver las etiquetas de seguimiento de cualquiera de los segmentos personalizados que ha creado y compartir esos segmentos con otros usuarios. También puede editar o eliminar los segmentos personalizados que ha creado.

   No puede editar ni compartir segmentos personalizados que otros usuarios hayan compartido con usted.

* Todos los segmentos de origen importados disponibles para el usuario.

   No puede editar ni compartir segmentos de origen que se hayan compartido con usted. Póngase en contacto con su [!DNL Adobe] equipo de cuenta si necesita compartir segmentos de origen con usuarios adicionales.

* Todos los segmentos de terceros personalizados disponibles para el usuario.

   No puede editar ni compartir segmentos de terceros que se compartieron con usted. Póngase en contacto con su [!DNL Adobe] equipo de cuenta si necesita compartir segmentos de terceros con usuarios adicionales.

>[!MORELIKETHIS]
>
>* [Crear una audiencia reutilizable](reusable-audience-create.md)
>* [Configuración de audiencia](audience-settings.md)
>* [Sintaxis para la lógica del segmento de audiencia](audience-segment-logic-syntax.md)
>* [Crear e implementar un segmento personalizado](custom-segment-create.md)
>* [Cree e implemente un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)

