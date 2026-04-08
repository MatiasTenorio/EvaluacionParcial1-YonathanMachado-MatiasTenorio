
# Pipeline de Despliegue - Evaluación Parcial 1

## Justificación del Modelo de Ramas (GitFlow)

Hemos seleccionado **GitFlow** porque nos permite mantener un control estricto sobre las versiones de producción (`main`) mientras colaboramos continuamente en un entorno seguro (`develop`). Esto facilita la integración de nuevas características y la resolución rápida de errores críticos en producción.

## Guía de Buenas Prácticas para el Equipo

### 1. Naming de Ramas

* **Características nuevas:** `feature/<nombre-breve-de-la-tarea>` (Ej: `feature/agregar-login`)
* **Errores críticos en producción:** `hotfix/<nombre-del-error>` (Ej: `hotfix/caida-base-datos`)

### 2. Mensajes de Commit

Utilizamos Convencional Commits:

* `feat: añade nueva funcionalidad`
* `fix: corrige un error`
* `docs: actualizaciones en documentación`
* `ci: cambios en los archivos de configuración de integración continua`

### 3. Flujos de Merge y Revisiones

* Todo cambio debe integrarse mediante un **Pull Request (PR)**.
* Los PR de `feature/` se dirigen a `develop`.
* Los PR de `hotfix/` se dirigen a `main` y luego se sincronizan con `develop`.

### 4. Estructura de Carpetas

* `/docs`: Archivos de documentación y diagramas.
* `/.github/workflows`: Archivos de configuración de GitHub Actions.
* `/src`: Código fuente (futuros microservicios).