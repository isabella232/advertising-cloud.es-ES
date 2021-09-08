---
source-git-commit: d3e36cef27fce533e9435717d428d54b982fd427
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---
# Documentación colaborativa para Advertising Cloud

Este es el repositorio de documentación para Adobe Advertising Cloud, que incluye documentos entre productos, DSP y TV. (Más adelante, incluirá documentos para Creative y Buscar).

**Nota: Esta página no se publica en la documentación de cara al cliente.**

## TOC

+ `TOC.md` en la raíz de cualquier guía del usuario proporciona a la organización los temas que contiene la guía.
+ Cada guía del usuario tiene una `TOC.md` única, en la que puede ordenar todas las páginas o temas según sea necesario.


## Guía del usuario

+ La introducción a la guía del usuario se llama `overview.md`
+ Cada tema de la guía del usuario tiene su propio directorio.
   + Si hay un tema en la guía llamado *Implementation*, el directorio correspondiente es `/implementation`
+ Todos los recursos de imagen se almacenan en `/assets` en la raíz de la guía del usuario.
   + Todas las imágenes del directorio `/assets` se localizarán.
   + Las imágenes del directorio `/no-localize` no se localizarán (hay una sorpresa). Esto se puede usar para garantizar en versiones localizadas que los recursos específicos no se reproducen innecesariamente.

## Metadatos de nivel de guía del usuario

+ Los metadatos que describen la guía del usuario se almacenan en `TOC.md`. Esto incluye:
   + producto: nombre del producto/capacidad.
   + cloud: nube a la que pertenece este producto.
   + audience: audiencia o arquetipo a la que se dirige la guía.
   + user-guide: nombre de la guía del usuario.

## Metadatos de nivel de página

+ Los metadatos necesarios para describir un documento se almacenan como parte de cada página individual. Esto incluye:
   + title: título de la página
   + description: descripción de la página
   + seo-title: título alternativo seo
   + seo-description: título alternativo para propósitos de SEO
   + short-title: (campo opcional)
   + index (sí/no): la plataforma de búsqueda de Adobe indexará la página
   + translate (sí/no): esta página se localizará
   + beta: ¿este producto está en fase beta?
   + redirigir: se puede usar para crear una referencia a una nueva página si es necesario
   + doc-type: referencia (predeterminado) / solución de problemas / desarrollador / tutorial / kb / whitepaper

## Más información

Para obtener más instrucciones de publicación, guías de estilo, ejemplos y otros recursos, consulte:

+ [Contribución de directrices de autor  **específicas para Advertising Cloud**](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=EfficientFrontier&amp;title=Contributing+Author+Guidelines+for+Advertising+Cloud+Help)
+ [Creación colaborativa para todos los redactores de Adobe](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/home.html)

Consulte también:

+ contribuyente.md Para obtener información general sobre cómo contribuir a la documentación.

<!-- * guidelines.md For an overview on what is expected in contributions and how to compose your documentation contributions. -->
+ code-of-behavior.md Para obtener una descripción general de los estándares de comportamiento que esperamos que se realicen al contribuir a este proyecto de documentación.
