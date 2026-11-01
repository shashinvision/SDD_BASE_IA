# AGENTS.md — <proyecto>

## Proyecto
<2-3 frases: qué es, arquitectura, tecnologías principales.>

## Comandos
- Ejecutar: `<comando>`
- Tests: `<comando>`
- Lint/formato: `<comando>`

## Estilo y convenciones
<Versión del lenguaje, convenciones de nombres, idioma del código y de los mensajes, formato.>

## Verificación inicial (Muy Importante)
Al comenzar cualquier sesión, verifica si existe la estructura SDD (la carpeta `specs/` y el archivo `docs/constitution.md`).
- **Si NO existe:** Estás en un proyecto nuevo. DEBES leer obligatoriamente el archivo `docs/sdd-init.md` y ejecutar sus fases paso a paso para inicializar el proyecto.
- **Si SÍ existe:** NO leas `docs/sdd-init.md`. Ve directamente a:
  1. Leer `docs/constitution.md`.
  2. Revisar `docs/architecture.md` (si no existe, generarlo con el resumen arquitectónico actual).
  3. Leer la spec activa en `specs/NNN-feature/spec.md`.
  4. Consultar solo los archivos necesarios para la tarea actual.

## Reglas del día a día
- Leer la constitución y la spec activa antes de tocar código.
- Evitar sobreingeniería: implementar solo lo necesario para cumplir el requerimiento.
- No añadir abstracciones, patrones o dependencias innecesarias.
- Mejoras relevantes fuera de alcance: consultar antes de implementar.
- No anticipar funcionalidades futuras salvo que sean necesarias para la solución actual.
- No afirmar que una implementación fue exitosa sin haber ejecutado las comprobaciones.
- No hacer commits, borrar archivos ni modificar el historial de Git sin instrucción explícita.

## Al terminar cualquier tarea
- Ejecutar los tests (o justificar por qué no aplican) y mostrar el resultado.
- Actualizar `tasks.md` y los documentos afectados.
- Antes de cerrar una fase: verificar que tareas, contratos y especificaciones reflejen el estado real de la implementación.