# Guía de Inicialización SDD

Si estás leyendo esto, es porque el proyecto no tiene la estructura SDD creada.
Debes seguir estas fases estrictamente. **No avances a la siguiente fase sin aprobación explícita del usuario.**

## Estructura a generar
- `docs/`: `constitution.md` y `architecture.md`.
- `specs/NNN-nombre-funcionalidad/`: `spec.md`, `plan.md`, `tasks.md` (y `contract.md` si hay interfaces compartidas).

---

### 1. Constitución (`docs/constitution.md`)
- Proponer un documento con exactamente 6 principios innegociables, cortos y verificables (máx. 15 líneas).
- Deben cubrir: simplicidad del stack, relación spec/código, separación lógica/interfaz, política de tests, persistencia de datos e idioma.
- **Regla:** Esperar la aprobación del usuario antes de escribir cualquier otra cosa.

### 2. Arquitectura (`docs/architecture.md`)
- Si el proyecto ya existe (tiene código), explorar la estructura.
- Generar un resumen arquitectónico: stack, módulos, flujo principal, puntos de entrada y deuda conocida.
- Si es un proyecto desde cero, definir la arquitectura base de acuerdo con la constitución.

### 3. Especificación (`spec.md`)
- **Regla de oro:** NO escribir código ni definir stack, arquitectura o nombres de archivos. Solo el QUÉ y el POR QUÉ.
- Entrevistar al usuario con un **máximo de 6 preguntas, de UNA en UNA**, para eliminar ambigüedades (casos límite, errores, fuera de alcance).
- Generar el documento con: contexto, usuarios, historias de usuario, requisitos funcionales (RF-x) en notación EARS en español, RNF, casos límite, fuera de alcance, criterios de finalización y dudas abiertas.

### 4. Clarificación (Revisión de la Spec)
- Actuar como un QA muy profesional.
- Listar de forma numerada: (1) ambigüedades restantes, (2) contradicciones, (3) casos límite no cubiertos, (4) conflictos con `docs/constitution.md`.
- **Regla:** Solo detectar y listar. NO proponer soluciones todavía.

### 5. Planificación (`plan.md`)
- Leer `docs/constitution.md` y `spec.md`. **NO escribir código.**
- Generar el documento con: estructura de módulos, modelo de datos (con ejemplo), pseudocódigo de algoritmos clave, contrato de la CLI/API (comandos, salidas, códigos de salida), decisiones técnicas justificadas (incluyendo la alternativa descartada) y estrategia de tests.
- Trazar explícitamente qué RF cubre cada parte del plan.

### 6. Tareas (`tasks.md`)
- Generar tareas pequeñas (**máx. 20-30 min cada una**), en estricto orden de dependencia.
- Cada tarea debe usar checkboxes, indicar los RF que cubre y tener una línea **"Hecho cuando:"** con un criterio verificable.

### 7. Implementación y Validación (Después de inicializar)
- **Regla de oro:** Implementar SOLO la tarea indicada (ej. T2). No adelantar trabajo de la siguiente tarea.
- **Tests primero:** Escribir los tests y luego el código.
- Al terminar una tarea: ejecutar tests, mostrar resultado, marcar en `tasks.md` y **PÁRATE**.
- Para validar: recorrer `spec.md` requisito por requisito (RF-1 a RF-n) indicando qué test lo cubre y su resultado.

### 8. Gestión de Cambios (Posterior)
- Ante un nuevo requisito: **NO tocar código.**
- Actualizar primero `spec.md` (nuevos RF en EARS + casos límite) y mostrar el diff de la spec al usuario.