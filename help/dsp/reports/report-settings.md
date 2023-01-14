---
title: Configuración de informes personalizados
description: Consulte las descripciones de la configuración de informes personalizada.
feature: DSP Custom Reports
exl-id: 1d37fc96-0f9b-4eb2-ba8d-9534f627adaf
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 0%

---

# Configuración de informes personalizados

**[!UICONTROL Name]** El nombre del informe. La longitud máxima es de 180 caracteres.

**[!UICONTROL Report Type]** Tipo de informe: *[!UICONTROL Custom]* (que incluye las opciones más disponibles), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]* o *[!UICONTROL Site]*.

## [!UICONTROL Apply Filters] Sección

**[!UICONTROL Timezone]:** Zona horaria de los informes.

**[!UICONTROL Observe Daylight Savings Time]:** Considera el horario de verano en los tiempos de informe.

**\[Intervalo de fechas\]:** El intervalo de fechas para el que se van a generar datos. La cantidad de días disponibles varía según el informe y las dimensiones seleccionadas. Elija una:

* **[!UICONTROL Previous N days]:** Incluye datos de un número específico de días antes de hoy.

* **[!UICONTROL Custom]:** Incluye datos entre fechas de inicio y finalización específicas. Para informar de los datos hasta el día anterior, seleccione **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** Incluye datos del mes del calendario anterior.

**[!UICONTROL Add Filters]:** (Opcional) Dimensiones adicionales según las cuales filtrar los datos, independientemente de si las dimensiones se incluyen como columnas en el informe: *[!UICONTROL Account]*,\* *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Placement]*, *[!UICONTROL Ad]*, *[!UICONTROL Ad Type]*, *[!UICONTROL Video]*, *[!UICONTROL Video Duration]*, *[!UICONTROL Country]* y *[!UICONTROL Package]*.

\* *[!UICONTROL Account]* solo está disponible para los siguientes tipos de informes cuando su organización está configurada para [informes entre cuentas](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]y [!UICONTROL Conversion]. Póngase en contacto con su [!DNL Adobe] equipo de cuentas para obtener más información sobre los informes entre cuentas.

Para aplicar uno o más filtros, haga lo siguiente:

* Seleccione una dimensión, seleccione el operador (*es igual que* o *no es igual a*) y, a continuación, seleccione el valor aplicable. Por ejemplo, para devolver datos solo de anuncios previos a la publicación, especifique &quot;[!UICONTROL Ad Type equals Preroll].&quot;
* (Opcional) Agregue criterios adicionales al filtro.
* (Opcional) Añada filtros adicionales, cada uno con uno o más criterios.

## [!UICONTROL Build Your Report] Sección

**[!UICONTROL Select To Add As Report Headers]:**  Las columnas de datos, o encabezados, que se incluirán en el informe. Para agregar una columna, expanda la categoría y seleccione la casilla de verificación situada junto al nombre de la columna. Todas las métricas no disponibles están deshabilitadas. Las categorías de datos disponibles incluyen:

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] (ordenado por anunciante)
* [!UICONTROL Custom Goals] (ordenado por anunciante)

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Orden de los encabezados de columna. Puede arrastrar y soltar cualquier columna para personalizar el orden.

## [!UICONTROL Multi-Touch Conversion Options] Sección

**[!UICONTROL Format]:** Si se va a generar un informe en *[!UICONTROL CSV]* (valores separados por comas) o *[!UICONTROL Tab]* (valores separados por tabulaciones).

**[!UICONTROL Report Headers]:** Si lo hace *[!UICONTROL Include]* o *[!UICONTROL Do Not Include]* encabezados de columna.

**[!UICONTROL Attribution Rule Settings]:** (Todos [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]y [!UICONTROL Site] informes con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] columnas; anunciantes con Adobe (solo seguimiento de conversión de publicidad) Dentro del informe, cómo atribuir datos de conversión en una serie de eventos que conducen a una conversión. Puede elegir más de una regla si desea comparar las diferencias entre las reglas.

>[!NOTE]
>
>Las rutas de conversión incluyen todas las impresiones y clics dentro de las ventanas de retrospectiva de clics o impresiones del anunciante, que están configuradas en [!DNL Adobe Advertising Search]. Los clics tienen preferencia sobre las impresiones durante la atribución de conversión. Cualquier clic en una ruta de conversión recibe crédito completo en función de la regla de atribución. Las impresiones reciben crédito solo cuando no se realiza un seguimiento de ningún clic en la ruta de conversión.

* *[!UICONTROL Last Event]:* Atributos conversiones al último clic o impresión en la ruta de conversión.

* *[!UICONTROL Weight Last More]:* Atribuye conversiones a todos los eventos de la ruta de conversión, pero da la mayor importancia al último evento y, sucesivamente, menos importancia a los eventos anteriores.

* *[!UICONTROL Even Distribution]:* Atribuye conversiones de forma equitativa a cada evento de la ruta de conversión.

* *[!UICONTROL Weight First More]:* Atribuye conversiones a todos los eventos de la ruta de conversión, pero da la mayor importancia al primer evento y, sucesivamente, menos importancia a los eventos siguientes.

* *[!UICONTROL First Event]:* Atributos conversiones al primer clic o impresión en la ruta de conversión.

* *[!UICONTROL U-shaped]:* Atribuye la conversión a todos los eventos de la ruta de conversión, pero da mayor peso a los eventos primero y último, con una importancia sucesiva menor a los eventos de la mitad de la ruta de conversión.

* *[!UICONTROL Display Only]:*  Atributos conversiones al último clic o impresión DSP en la ruta de conversión. Esto incluye vídeo y anuncios de TV conectados, y excluye los clics en [!DNL Adobe Advertising Search] anuncios.

* *[!UICONTROL Social Only]:* Obsoleto

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

**[!UICONTROL Paths as Columns]:**  (Todos [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]y [!UICONTROL Site] informes con [!UICONTROL Conversion Metrics] o [!UICONTROL Custom Goals] (columnas) Qué tipos de conversiones informar cuando se produjeron eventos anteriores en el mismo dispositivo. Se pueden incluir hasta tres tipos. Para cada tipo seleccionado, se incluye una columna separada para cada métrica de conversión y se anexa el sufijo especificado ([!UICONTROL (tl)], [!UICONTROL (ct)]o [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Incluye conversiones atribuidas a clics (CT para pulsaciones) e impresiones (VT para visualizaciones). Las conversiones atribuidas a impresiones se multiplican por el peso de visualización especificado. El peso de visualización predeterminado es del 100 %, lo que significa que las conversiones atribuidas a impresiones se cuentan como el 100 % del valor de las conversiones atribuidas a clics.

* *[!UICONTROL With Clicks (CT)]:* Incluye solo las conversiones atribuidas a clics.

* *[!UICONTROL Impressions Only (VT)]:* Incluye solo las conversiones que se atribuyeron a impresiones porque no se rastrearon clics en la ruta de conversión.

**[!UICONTROL Conversion Reporting Based On]:**  Cómo informar de los datos de conversión:

* *[!UICONTROL Conversion Timestamp]:* (El valor predeterminado) Las conversiones se asociarán con la fecha de conversión.

* *[!UICONTROL Event Timestamp]:* Las conversiones se informarán en función de la fecha de la impresión o del clic que hayan causado la conversión, según lo determinado por el [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] Sección

**[!UICONTROL Destination Type]:** Elija uno de los siguientes tipos de destino:

* *[!UICONTROL S3]:* Para enviar el informe completado a uno o más [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), que se especificarán en la variable **[!UICONTROL Destination Name]** campo .
* *[!UICONTROL sFTP]:* Para enviar el informe completado a una o varias ubicaciones SFTP, según lo especificado en la sección **[!UICONTROL Destination Name]** campo .
* *[!UICONTROL FTP]:* Para enviar el informe completado a una o varias ubicaciones de FTP, que se especificarán en la variable **[!UICONTROL Destination Name]** campo .
* *[!UICONTROL FTP SSL](Actualmente en versión beta):* Para enviar el informe completado a una o varias ubicaciones SSL de FTP, que se especificarán en la variable **[!UICONTROL Destination Name]** campo .
* *[!UICONTROL Email]:* Para especificar las direcciones de correo electrónico a las que enviar los informes completados o las notificaciones si el informe se cancela debido a errores. Para especificar varias direcciones, sepárelas con comas o espacios.

>[!NOTE]
>
> No se puede cambiar el tipo de destino una vez guardado el informe.

**[!UICONTROL Destination Name]:** (Solo tipos de destino S3, FTP, sFTP y FTP SSL) Los nombres de los destinos de informe a los que se enviará el informe personalizado.

* Para especificar un destino existente, seleccione un nombre de destino en la lista. Puede seleccionar varios nombres de destino por separado.

* Para crear un nuevo destino:

   1. Haga clic en **Añadir nuevo destino**.

   1. Introduzca la variable [configuración de destino del informe](/help/dsp/reports/report-destinations/report-destination-settings.md)y haga clic en **Guardar**.

   1. De nuevo en la configuración del informe, haga clic en **Actualice Los Nombres De Destino.**

      El nuevo destino ya está disponible en la lista de destinos existentes y, si lo desea, puede agregarlo al informe.

**[!UICONTROL Frequency]:** (Para cada [!UICONTROL Destination Name] La frecuencia con la que se envía el informe al destino: *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]* o *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] Sección

**[!UICONTROL Send & Save]:** Cuándo enviar el informe: *[!UICONTROL On Schedule]* o *[!UICONTROL Run Now]*. Los informes programados se entregarán antes de las 9:00 en la zona horaria de la cuenta.

>[!NOTE]
>
>Puede [ejecutar un informe personalizado en cualquier momento](report-run-now.md) de la variable [!UICONTROL Reports] vista.

>[!MORELIKETHIS]
>
>* [Acerca de los informes personalizados](/help/dsp/reports/report-about.md)
>* [Crear un informe personalizado](/help/dsp/reports/report-create.md)
>* [Duplicar un informe personalizado](/help/dsp/reports/report-copy.md)
>* [Editar un informe personalizado](/help/dsp/reports/report-edit.md)
>* [Ejecutar un informe personalizado](/help/dsp/reports/report-run-now.md)
>* [Configuración de informes personalizados](/help/dsp/reports/report-settings.md)
>* [Acerca de los destinos de informe](/help/dsp/reports/report-destinations/report-destination-about.md)

* [Columnas de informe disponibles](/help/dsp/reports/report-columns.md)
