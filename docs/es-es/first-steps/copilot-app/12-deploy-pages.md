---
title: "Lección 12 - Despliega el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su pull request y comprobar que Space Quiz está disponible."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica Space Quiz para que cualquiera pueda acceder a él mediante GitHub Pages. Copilot puede preparar el flujo de trabajo y guiarte durante el despliegue, pero sigues siendo responsable de revisar los cambios y confirmar que el sitio está disponible.

En esta lección:

- pedirás a Copilot que configure un despliegue en GitHub Pages.
- revisarás el flujo de trabajo y el pull request antes de fusionarlo.
- seguirás el despliegue y comprobarás el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero las personas aún necesitan una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages lo hace accesible desde una URL pública sin añadir un servidor ni dependencias de ejecución.

## Pide a Copilot que despliegue el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este mensaje:

```plaintext
Habilita GitHub Pages para este repositorio. Crea un flujo de trabajo de GitHub Actions que compile el sitio web si es necesario y lo despliegue en GitHub Pages. Añade un README que describa la aplicación y cómo ejecutarla localmente si aún no existe. Crea un pull request con estos cambios y fusiónalo cuando superen las comprobaciones obligatorias. Supervisa el despliegue hasta que se complete correctamente y, después, indica la URL final del sitio web publicado. Si no tienes permiso para habilitar Pages o fusionar el pull request, dime exactamente qué tengo que aprobar o hacer; no informes de que se ha completado hasta que el sitio esté disponible.
```

![Diagrama de tres etapas: un pull request de space-quiz fusionado; una ejecución correcta de GitHub Actions Deploy website con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz publicado en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este mensaje pide al agente que cree y fusione un pull request y cambie la configuración de Pages del repositorio. Antes de continuar, revisa el diff, los permisos de despliegue y las solicitudes de aprobación de GitHub.

## Revisa el flujo de trabajo y comprueba el despliegue

1. Confirma que el README solo se añade si el repositorio aún no tiene uno.
2. Revisa los cambios del pull request, incluidos los pasos de compilación y despliegue del flujo de trabajo.
3. Fusiónalo solo después de que se superen las comprobaciones obligatorias del pull request.
4. Sigue la ejecución de despliegue de GitHub Actions hasta que se complete correctamente.
5. Abre la URL indicada y confirma que se carga Space Quiz.

Si el agente no puede habilitar Pages o fusionar el pull request, sigue las instrucciones concretas que te proporcione. No des la tarea por completada hasta que el despliegue se complete correctamente y el sitio esté disponible.

## Resumen y siguientes pasos

Space Quiz ya está disponible como sitio web y has comprobado el despliegue en lugar de confiar únicamente en el informe del agente. Continúa con la [Lección 13: Revisión y siguientes pasos][next-lesson].

[next-lesson]: ../13-review/
