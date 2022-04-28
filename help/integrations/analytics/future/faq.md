---
title: Preguntas frecuentes
description: xxx
source-git-commit: ca19836d5918c69161c4d850a65eaff311249225
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Preguntas frecuentes xxx

## title

https://adobeadcloud.zendesk.com/agent/tickets/14214 De forma predeterminada, Adobe Analytics informa de todos los eventos capturados en cada informe. &quot;[!UICONTROL Unspecified]&quot; representan eventos de finalización de formularios que no estaban conectados a Advertising Cloud. Por ejemplo, en el informe Plataforma de publicidad , las conversiones orgánicas o impulsadas por una campaña de correo electrónico caerían en &quot;sin especificar&quot;.

Puede usar el filtro para eliminar eventos no especificados de los informes eliminando la marca de verificación de la opción &quot;Incluir no especificado (ninguno)&quot;. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323 Coloque las etiquetas de eventos de Analytics en las mismas zonas que los píxeles de Ad Cloud para asegurarse de que XXX coinciden.

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323

P: Durante nuestra auditoría de seguridad interna, ciertas funciones se marcaron como problemas de seguridad que habilitamos cuando integramos Ad Cloud en nuestra instalación existente de Adobe Analytics.

La integración en cuestión está entre AdCloud y Adobe Audience Manager. Esta función aumenta la tasa de coincidencia del ID de visitante entre AdCloud y Adobe Audience Manager. Para ello, envía solicitudes de red a pagead.l.doubleclick.net, star-mini.c10r.facebook.com y pug88000nf.pubmatic.com para determinar si estos servicios tienen un ID de visitante existente que se pueda aprovechar. Estas son las solicitudes de red que se han marcado como un riesgo de seguridad y que se producen en todos los visitantes del sitio.

Nuestro auditor nos pide que deshabilitemos esta función. ¿Qué sucede si bloqueamos esas solicitudes de red?

A: Comprobamos con nuestro producto y mencionaron que los píxeles en cuestión tienen el propósito de aumentar las tasas de coincidencia de cookies entre Ad Cloud, socios específicos de inventario/SSP (con respecto a DSP) y AAM.  Si se eliminan, el cliente puede ver algún nivel de tasa de coincidencia reducida entre AAC/AAM y los socios de inventario para los que están los píxeles respectivos, pero no esperarían que fuera sustancial.

En Ad Cloud Search, vemos que el ID de Experience Cloud de la organización está configurado para Mathworks, pero nuestro equipo de productos no ve la configuración de Mathworks para activar audiencias en Ad Cloud. ¿Utiliza Adobe Audience Manager para enviar audiencias a Ad Cloud Search? Si no es así, la eliminación de estos elementos no afectará al flujo de trabajo actual. AAM Servicio de atención al cliente puede ayudarle con la eliminación de estos píxeles si no desea que se activen.

