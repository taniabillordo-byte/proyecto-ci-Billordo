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
