---
source-git-commit: 0654347afd1caf5e9bd8ccabf41a8a591e604df5
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---
# Documentación colaborativa para Advertising Cloud

Este es el repositorio de documentación para Adobe Advertising Cloud, incluidos documentos de DSP y entre productos. (Más adelante, incluirá documentos para la búsqueda y, posiblemente, (?) para creativos).

**Nota: Esta página no se publica en la documentación de cara al cliente.**

## TOC

+ `TOC.md` en la raíz de cualquier guía del usuario proporciona a la organización los temas que contiene la guía.
+ Cada guía del usuario tiene un `TOC.md`, en la que puede ordenar todas las páginas o temas según sea necesario.


## Guía del usuario

+ La introducción a la guía del usuario se denomina `overview.md`
+ Cada tema de la guía del usuario tiene su propio directorio.
   + Si hay un tema en la guía llamado *Implementación*, el directorio correspondiente es `/implementation`
+ Todos los recursos de imagen se almacenan en `/assets` en la raíz de la guía del usuario.
   + Todas las imágenes del `/assets` se localizará.
   + Cualquier imagen de `/no-localize` no se localizará (hay una sorpresa). Esto se puede usar para garantizar en versiones localizadas que los recursos específicos no se reproducen innecesariamente.

## Metadatos de nivel de guía del usuario

+ Los metadatos que describen la guía del usuario se almacenan en la variable `TOC.md`. Esto incluye:
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

+ [Contribución de guías de creación **específicamente para Advertising Cloud**](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=EfficientFrontier&amp;title=Contributing+Author+Guidelines+for+Advertising+Cloud+Help)
+ [Creación colaborativa para todos los redactores de Adobe](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/home.html)

Consulte también:

+ contribuyente.md Para obtener información general sobre cómo contribuir a la documentación.

<!-- * guidelines.md For an overview on what is expected in contributions and how to compose your documentation contributions. -->
+ code-of-behavior.md Para obtener una descripción general de los estándares de comportamiento que esperamos que se realicen al contribuir a este proyecto de documentación.
