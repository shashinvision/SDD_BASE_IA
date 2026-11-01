## Inicialización del SDD

- Al comenzar a trabajar en un proyecto, revisar la estructura existente, `AGENTS.md` y la documentación disponible para determinar si existe una estructura SDD.
- Si el proyecto no tiene SDD y el requerimiento necesita planificación formal, crear el directorio `/plan` y los documentos necesarios antes de implementar.
- Para casos de uso que requieran un SDD completo, utilizar como estructura inicial:
  - `plan.md`: estrategia, arquitectura, fases y enfoque de implementación.
  - `spec.md`: requisitos funcionales, reglas de negocio y criterios de aceptación.
  - `contract.md`: contratos, interfaces, API y estructuras de datos relevantes.
  - `tasks.md`: tareas, dependencias, estado y verificaciones.
- Crear documentos con contenido coherente con el requerimiento. No generar archivos vacíos ni inventar requisitos, contratos o decisiones que no estén definidos.
- Si existe documentación parcial, reutilizarla y completarla en lugar de duplicarla.
- Si el proyecto ya tiene un SDD, respetar su estructura y convenciones. Crear únicamente los documentos que falten y sean necesarios.
- Para tareas pequeñas que no requieran planificación formal, no crear toda la estructura SDD innecesariamente.
- Si faltan decisiones críticas para definir la solución, solicitar aclaraciones antes de asumirlas.

## Uso de SDD

- El directorio `/plan` es la fuente de verdad para la planificación, especificaciones, contratos y tareas del caso de uso.
- Al inicio de cada sesión, revisar `AGENTS.md` y los documentos principales del SDD disponibles: `plan.md`, `spec.md`, `contract.md` y `tasks.md`. Si alguno no existe, aplicar las reglas de inicialización anteriores cuando corresponda.
- Después de la revisión inicial, consultar únicamente los archivos y las secciones necesarios para la tarea actual. No releer toda la documentación en cada interacción si no es necesario.
- Antes de implementar cambios relevantes, comprender los requisitos, las decisiones de diseño, los contratos y las tareas relacionadas.
- Mantener actualizada la documentación cuando la implementación modifique requisitos, alcance, diseño, arquitectura, contratos o comportamiento definido.
- Mantener `tasks.md` sincronizado con el avance real. Marcar una tarea como completada únicamente cuando esté implementada y verificada; registrar bloqueos y pendientes cuando corresponda.
- Mantener la trazabilidad entre historias de usuario, requisitos, contratos y tareas.
- Registrar las decisiones de diseño y arquitectura relevantes, incluyendo su justificación cuando sea necesaria para comprender la solución.
- Seguir los estándares, las guías de estilo, los patrones y las prácticas establecidos en el proyecto.
- Dividir las historias de usuario en tareas pequeñas, independientes y verificables.
- Si una tarea depende de otra, identificar explícitamente la dependencia y completar únicamente las tareas previas estrictamente necesarias.
- No ampliar el alcance para resolver dependencias o mejoras que no sean necesarias. Si una dependencia implica un cambio significativo de alcance, consultar antes de continuar.
- No eliminar documentos simplemente porque sus tareas estén completadas o porque haya aumentado el tamaño de la documentación. Conservar la documentación vigente y utilizar Git para mantener el historial.
- Si un documento queda obsoleto, actualizarlo o retirarlo solo cuando corresponda, verificando que la información relevante esté preservada y que no existan referencias vigentes que dependan de él.

## Importante

- Evitar la sobreingeniería. Implementar únicamente lo necesario para cumplir el requerimiento solicitado.
- No agregar abstracciones, patrones, componentes, dependencias o refactorizaciones innecesarias.
- Si se detecta una mejora relevante fuera del alcance solicitado, no implementarla directamente. Consultarla antes.
- Dividir el trabajo en tareas de aproximadamente 20–30 minutos de trabajo humano como máximo, siempre que sea viable. Si una tarea requiere más tiempo, dividirla cuando sea posible sin generar fragmentación artificial.
- Cada tarea debe tener un objetivo claro, criterios de aceptación y un resultado verificable.
- Formular como máximo 6 preguntas por tarea cuando se necesiten aclaraciones, priorizando las que bloqueen la implementación.
- Si existen varias alternativas, elegir la solución más simple que cumpla correctamente el requerimiento.
- No anticipar funcionalidades futuras salvo que sean necesarias para la solución actual.
- No afirmar que una implementación o validación fue exitosa sin haber realizado las comprobaciones correspondientes.
- Al finalizar cada tarea, revisar si es necesario actualizar `tasks.md` y los documentos afectados, evitando cambios documentales innecesarios.
- Antes de finalizar una fase, verificar que las tareas, los contratos y las especificaciones reflejen el estado real de la implementación.
- No realizar commits, eliminar archivos ni modificar el historial de Git sin una instrucción explícita del usuario.
 