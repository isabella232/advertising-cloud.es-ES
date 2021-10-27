---
title: Configuración del destino del informe
description: Consulte los detalles necesarios para los destinos de informes, por tipo de destino.
feature: DSP Custom Reports
source-git-commit: ff14691fd2b6fa56c303dca3ac0e4c897c322f72
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# Configuración del destino del informe

Los detalles requeridos para los destinos de informes que no son de correo electrónico varían según el tipo de destino.

>[!NOTE]
>
> También puede enviar sus informes personalizados a los destinatarios de correo electrónico, que no necesitan un destino de informe guardado. Puede especificar destinatarios de correo electrónico, en lugar de destinos guardados, dentro de la configuración del informe.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Un nombre que le ayudará a identificar el destino.

**[!UICONTROL S3 Bucket URL]:** Ruta de acceso completa a la carpeta en la [!DNL Amazon Simple Storage Service] (S3) para el que se cargará el informe. Ejemplo: `s3://adcloud_account/reports`

**[!UICONTROL Access Key ID]:** El ID de clave de acceso a ([!DNL Amazon S3]) depósito (proporcionado por [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** La clave de acceso secreto a ([!DNL Amazon S3]) depósito (proporcionado por [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Un nombre que le ayudará a identificar el destino.

**[!UICONTROL Server]:** El nombre de host del servidor.

**[!UICONTROL Port]:** Número de puerto que se va a usar en el servidor. El valor predeterminado es *[!UICONTROL 21]*.

**[!UICONTROL Username]:** El nombre de usuario para iniciar sesión en el servidor.

**[!UICONTROL Password]:** La contraseña para iniciar sesión en el servidor.

**[!UICONTROL Path (Optional)]:** La ruta del servidor a la que se cargarán los archivos.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Un nombre que le ayudará a identificar el destino.

**[!UICONTROL Server]:** El nombre de host del servidor.

**[!UICONTROL Port]:** Número de puerto que se va a usar en el servidor. El valor predeterminado es *[!UICONTROL 21]*.

**[!UICONTROL Username]:** El nombre de usuario para iniciar sesión en el servidor.

**[!UICONTROL Password]:** La contraseña para iniciar sesión en el servidor.

**[!UICONTROL Path (Optional)]:** La ruta del servidor a la que se cargarán los archivos.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Un nombre que le ayudará a identificar el destino.

**[!UICONTROL Server]:** El nombre de host del servidor.

**[!UICONTROL Port]:** Número de puerto que se va a usar en el servidor. El valor predeterminado es *[!UICONTROL 21]*.

**[!UICONTROL Username]:** El nombre de usuario para iniciar sesión en el servidor.

**[!UICONTROL Password]:** La contraseña para iniciar sesión en el servidor.

**[!UICONTROL Path (Optional)]:** La ruta del servidor a la que se cargarán los archivos.

>[!MORELIKETHIS]
>
>* [Acerca de [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Cree un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Editar un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Eliminar un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)

