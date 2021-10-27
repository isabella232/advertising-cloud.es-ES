---
title: Acerca de los informes personalizados
description: Obtenga información sobre las opciones para crear informes personalizados manualmente o mediante plantillas de informe preconfiguradas.
feature: DSP Custom Reports
exl-id: 59fc1894-1c9d-451d-b644-5640dd311547
source-git-commit: ff14691fd2b6fa56c303dca3ac0e4c897c322f72
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Acerca de los informes personalizados

Los informes personalizados permiten personalizar el contenido y el envío de los datos del informe mediante las dimensiones de la campaña (como el anunciante, la ubicación, los sitios o los geos) y las métricas que más le importan. Puede:

* Configure completamente los informes de rendimiento de las campañas a nivel granular.
* Elija entre plantillas de informe preconfiguradas y, opcionalmente, personalícelas más adelante.

Puede generar informes una vez o programarlos para que se generen diariamente, semanalmente o mensualmente a las 3:00 en el huso horario especificado. Una vez generado el informe, se envía a cada destinatario de correo electrónico especificado o a los vínculos [destinos de informe](/help/dsp/reports/report-destinations/report-destination-about.md) de los siguientes tipos:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL (en versión beta)

>[!NOTE]
>
>También puede ver los datos bajo demanda en todos los niveles de una campaña (campaña, paquete, ubicación o publicidad) [dentro de la vista de administración de campañas correspondiente](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tipos de informes disponibles

* **[!UICONTROL Custom]:** Este informe es una plantilla en blanco que puede usar para crear su propio informe personalizado utilizando la mayoría de las dimensiones y métricas. [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo]y [!UICONTROL Site] los informes son variaciones de esta plantilla con columnas preseleccionadas y dimensiones para sus respectivos casos de uso.

* Plantillas de informe preconfiguradas

   * **[!UICONTROL Billing]:** Utilice este informe para comprender las métricas de facturación clave, como las métricas de gasto para la facturación de medios por campaña.

      >[!NOTE]
      >
      >Este informe incluye datos sobre el segmento de facturación. Si a un usuario o dispositivo se le presenta una impresión que pertenece a varios segmentos, solo se le atribuye la impresión a un segmento facturable.

   * **[!UICONTROL Conversion]:** Utilice este informe para comprender el rendimiento de sus campañas en función de las métricas de conversión capturadas mediante el seguimiento de conversión de Advertising Cloud. Este informe incluye atribución multitáctil.

   * **[!UICONTROL Device]:** Utilice esta plantilla rellenada previamente para ver las métricas clave por dimensiones relacionadas con el dispositivo.

   * **[!UICONTROL Frequency (by Impression)]:** Utilice este informe para comprender la distribución de impresiones mostradas a visitantes únicos (por ejemplo, cuántos visitantes únicos vieron una impresión, dos impresiones, tres impresiones, etc.). Los datos están disponibles por ubicación o campaña.

      >[!NOTE]
      >
      >* Los datos estarán disponibles después del 1 de marzo de 2019.
      >* La frecuencia se calcula sobre la base de un muestreo de datos.
      >* En algunos inventarios, los editores no pasan un identificador de dispositivo, lo que impide el seguimiento de la frecuencia. Este informe solo incluye las impresiones para las que estaba disponible un identificador de dispositivo.


   * **[!UICONTROL Frequency (by App/Site)]:** Utilice este informe para comprender a cuántos usuarios únicos se ha llegado por aplicación o por sitio. También puede ver cuántos usuarios únicos llegaron a través de una aplicación o sitio en particular (&quot;usuarios únicos distintos&quot;).

      >[!NOTE]
      >
      >* Los datos estarán disponibles a partir del 15 de noviembre de 2018.
      >* Para algunos inventarios privados, los editores no pasan un identificador de dispositivo, lo que impide el seguimiento de frecuencia.


   * **[!UICONTROL Geo]**: Utilice esta plantilla rellenada previamente para ver las métricas clave por dimensiones geográficas.

   * **[!UICONTROL Margin]:** Utilice este informe para ver métricas clave como margen, beneficio y otras métricas de gasto por campaña o ubicación.

   * **[!UICONTROL Segment]:** Utilice esta plantilla rellenada previamente para ver las métricas clave por segmento.

      >[!NOTE]
      >
      >* El objetivo de este informe es mostrar el rendimiento de los distintos segmentos segmentados. Utiliza los datos de pertenencia a segmentos. Cuando se produce una impresión en una persona o dispositivo que pertenece a dos o más segmentos objetivo, este informe incluye una fila para cada segmento. Por este motivo, es posible que los totales de este informe no coincidan con la entrega real.
      >* Las métricas de conversión y los datos de objetivo personalizados para segmentos están disponibles a partir del 2 de agosto de 2019. El resto de los datos de los segmentos estará disponible a partir del 1 de junio de 2018.


   * **[!UICONTROL Site]:** De forma predeterminada, incluye métricas estándar, gasto neto total de medios y gasto neto total facturable por sitio.

## Informes entre cuentas {#cross-account-reporting}

Cualquier organización con varias cuentas de DSP puede, opcionalmente, habilitar los datos entre cuentas en los informes personalizados según las necesidades de la organización. Por ejemplo, puede dar a la Cuenta A acceso a los datos de la Cuenta B y darle acceso a los datos de la Cuenta C (pero no a los de la Cuenta A). Para habilitar y configurar esta función, póngase en contacto con su administrador de cuentas de.

Una vez que la función esté habilitada para su organización, puede [filter](report-settings.md) cualquiera de los siguientes tipos de informes por cuenta:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]y [!UICONTROL Conversion].

La configuración de su cuenta en [!UICONTROL Settings] > [!UICONTROL Account] indican a) las otras cuentas cuyos datos están disponibles en su cuenta y b) las otras cuentas que pueden acceder a los datos de su cuenta.

>[!MORELIKETHIS]
>
>* [Crear un informe personalizado](/help/dsp/reports/report-create.md)
>* [Configuración de informes personalizados](/help/dsp/reports/report-settings.md)
>* [Acerca de los informes en la plataforma](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)
>* [Acerca de [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)

