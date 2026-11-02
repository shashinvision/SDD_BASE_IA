# AGENTS.md

## Proyecto
<!-- Completar al adaptar la plantilla: propósito, arquitectura y tecnologías principales. -->

## Comandos
<!-- Completar con comandos reales del proyecto. No inventar comandos. -->
- Ejecutar: `<comando>`
- Tests: `<comando>`
- Lint/formato: `<comando>`

## Convenciones
- Idioma de la documentación y la comunicación: español.
- <!-- Completar: versión del lenguaje, convenciones de nombres y formato. -->

## Inicio de sesión
Antes de trabajar, comprobar si existen `docs/constitution.md`, `docs/architecture.md` y la carpeta `specs/`.

### Constitución o `specs/` ausentes
- Leer `docs/sdd-init.md` y seguir el proceso de inicialización definido allí.
- No asumir que una estructura parcial está inicializada ni reemplazar documentos existentes.
- Respetar los puntos de aprobación de la guía; no avanzar de fase ni crear documentos sin la aprobación correspondiente.
- Si la solicitud es solo de análisis, revisión o propuesta, limitarse a leer y proponer; no iniciar la inicialización.

### Proyecto inicializado
1. Leer `docs/constitution.md`.
2. Revisar `docs/architecture.md`. Si falta, señalarlo y acordar su actualización; no inventar el estado arquitectónico.
3. Identificar la especificación aplicable:
   - Usar la que indique el usuario; o
   - Si existe una sola candidata clara, usarla.
   - Si hay varias candidatas o ninguna, preguntar antes de asumir.
4. Leer `spec.md` y los documentos de plan, tareas o contratos necesarios para el trabajo solicitado.

## Trabajo
- Leer la constitución y la especificación aplicable antes de cambiar código.
- Implementar solo el alcance solicitado; no adelantar tareas ni añadir abstracciones o dependencias innecesarias.
- Si un requisito contradice la especificación o implica cambiarla, aclarar el cambio y actualizar primero la documentación según el proceso SDD.
- No modificar código cuando la solicitud sea de análisis, revisión o propuesta.
- No hacer commits, borrar archivos ni modificar el historial de Git sin instrucción explícita.

## Verificación y cierre
- Ejecutar las pruebas y comprobaciones pertinentes e informar los comandos y resultados reales.
- Si no corresponden —por ejemplo, ante un cambio solo documental—, indicarlo y justificarlo.
- Actualizar `tasks.md` y otros documentos solo cuando el trabajo realizado afecte su contenido.
- Antes de cerrar una fase, comprobar que especificación, plan, tareas y contratos reflejen el estado real.
- No afirmar que una implementación está verificada si no se ejecutaron las comprobaciones.
