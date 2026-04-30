# Practico 4: Automatización de CI con GitHub Actions

## Integrantes
* Tania Billordo

## Lenguaje Elegido
* **.NET 8.0 (C#)**

## Explicación del Workflow
El flujo de trabajo configurado en `.github/workflows/dotnet.yml` realiza las siguientes acciones:
1. **Disparador:** Se activa en cada `push` o `pull request` a la rama principal.
2. **Entorno:** Utiliza una máquina virtual con la última versión de Ubuntu.
3. **Setup:** Instala el SDK de .NET 8.0.
4. **Validación:** Ejecuta `dotnet restore` para las dependencias y `dotnet build` para asegurar que el proyecto compila correctamente.

## Estado del Build
![.NET Core CI](https://github.com/taniabillordo-byte/proyecto-ci-Billordo/actions/workflows/dotnet.yml/badge.svg)

## Evidencia de Trabajo Colaborativo (Pull Request)
Se realizó un Pull Request para integrar cambios desde la rama `feature-tania-cambios`. El sistema de CI validó la propuesta antes de permitir la fusión.

## Cómo ejecutar el proyecto
1. Clonar el repositorio.
2. Ejecutar el comando: `dotnet run --project AppConsola/AppConsola.csproj`

# Práctico 5: Triggers y Automatización de GitHub Actions
En esta etapa se configuraron 6 disparadores (triggers) específicos para automatizar diferentes eventos del ciclo de vida del desarrollo:

* Push: Se activa al subir cambios a la rama principal.

* Pull Request: Se dispara al abrir una solicitud de extracción hacia principal.

* Issues: Se ejecuta automáticamente al crear un nuevo Issue.

* Issue Comment: Configurado con un filtro para activarse únicamente cuando se comenta dentro de un Pull Request.

* Workflow Dispatch (Manual): Permite la ejecución manual desde la pestaña Actions, incluyendo un menú de selección de nivel de alerta (Informativo, Advertencia, Crítico).

* Schedule (Programado): Ejecución automática configurada mediante cron para activarse cada 5 minutos.
