# SDD Base IA

**Base de referencia para aplicar desarrollo guiado por especificaciones (SDD) con asistencia de IA en otros proyectos.**

Este repositorio contiene instrucciones y formatos que un agente de IA puede leer y adaptar al proyecto en el que estés trabajando. Puedes usarlo para inicializar un proyecto o para migrar uno existente a SDD. No tienes que copiar esta plantilla encima del proyecto: clónala en una ubicación accesible y dile al agente dónde está.

---

## 📁 Estructura del proyecto

```
.
├── AGENTS.md             # Instrucciones para el agente IA (metodología SDD)
├── docs/
│   ├── constitution.md   # (por crear) Principios innegociables del proyecto
│   ├── architecture.md   # (por crear) Resumen arquitectónico
│   └── sdd-init.md       # Guía de inicialización paso a paso
├── specs/
│   └── NNN-feature/      # (por crear) Carpeta por funcionalidad
│       ├── spec.md       # Especificación de la funcionalidad
│       ├── plan.md       # Plan técnico detallado
│       ├── tasks.md      # Tareas atómicas con criterios de aceptación
│       └── contract.md   # (opcional) Interfaces compartidas
└── README.md
```

---

## 🧠 ¿Qué es SDD?

**Specification-Driven Development** es una metodología que prioriza la especificación formal antes de la implementación. Cada ciclo sigue estas fases:

| Fase | Descripción |
|------|-------------|
| **1. Constitución** | Definir principios innegociables del proyecto |
| **2. Arquitectura** | Documentar el stack y la estructura actual |
| **3. Especificación** | Redactar el QUÉ y el POR QUÉ (no el CÓMO) |
| **4. Clarificación** | Revisar la especificación con ojo crítico (QA) |
| **5. Planificación** | Definir el CÓMO: módulos, datos, contratos |
| **6. Tareas** | Dividir en tareas de 20-30 min con criterios verificables |
| **7. Implementación** | Codificar tarea por tarea, tests primero |
| **8. Gestión de cambios** | Ante nuevos requisitos, actualizar la spec primero |

> 📖 Para más detalle, consulta [`docs/sdd-init.md`](docs/sdd-init.md).

---

## 🚀 Cómo empezar

1. **Clona este repositorio** en una ubicación accesible para tu agente de IA. Esta será la ruta de referencia de la base SDD.
2. **Abre el repositorio de tu proyecto** con el agente de IA. Puede ser nuevo o tener ya código y documentación.
3. **Copia uno de los prompts de abajo** y reemplaza las rutas y el nombre del proyecto. El agente leerá esta base y seguirá sus instrucciones en el repositorio objetivo.
4. **Continúa el trabajo en tu proyecto** siguiendo la estructura SDD y las instrucciones que el agente adapte.

Los textos siguientes son prompts para el agente, no comandos de terminal. En ambos casos, `[RUTA_BASE_SDD]` es la ruta donde clonaste este repositorio y `[RUTA_PROYECTO]` la ruta del proyecto objetivo.

### Inicializar un proyecto

Usa este prompt cuando quieras aplicar la base SDD en un proyecto nuevo o que todavía no tenga esta estructura:

> Inicializa el proyecto **[NOMBRE_PROYECTO]**, ubicado en `[RUTA_PROYECTO]`, usando como referencia la base SDD de `[RUTA_BASE_SDD]`. Lee sus instrucciones y formatos, y adáptalos a este proyecto; no copies contenido de ejemplo como si describiera el proyecto. Primero revisa el estado y los archivos existentes. Sigue los puntos de aprobación definidos en la base y no sobrescribas archivos existentes sin consultarme.

### Migrar un proyecto existente

Usa este prompt cuando el proyecto ya tenga código, documentación o convenciones propias. El agente debe revisar el estado actual y **preguntarte antes de migrar**, ofreciendo estas dos opciones:

1. Migrar y adaptar el contenido actual a la estructura SDD.
2. Conservar el contenido actual bajo `archive/` como referencia y preparar la estructura SDD por separado.

> Migra el proyecto existente **[NOMBRE_PROYECTO]**, ubicado en `[RUTA_PROYECTO]`, usando como referencia la base SDD de `[RUTA_BASE_SDD]`. Antes de mover, modificar o crear archivos, revisa el proyecto y explícame qué contenido encontraste. Luego pregúntame si prefiero (1) migrar y adaptar todo el contenido actual a la estructura SDD o (2) conservarlo bajo `archive/` como referencia y preparar la estructura SDD por separado. Espera mi respuesta antes de actuar, preserva el contenido y no sobrescribas ni elimines archivos sin mi aprobación.

En la opción `archive/`, el contenido se conserva para consulta y reconocimiento del proyecto; no debe tratarse automáticamente como documentación vigente.

---

## 🤖 Uso con tu agente de IA

Esta base puede usarse con cualquier aplicación o *harness* de codificación con IA que utilices. Abre en esa aplicación el repositorio de tu proyecto y usa los prompts de la sección [Cómo empezar](#-cómo-empezar), indicando la ruta a esta base para que el agente lea y adapte sus instrucciones y formatos al contexto real del proyecto.

Al iniciar una sesión, el agente debe comprobar si existe la estructura SDD (`specs/` y `docs/constitution.md`). Si falta, debe seguir [`docs/sdd-init.md`](docs/sdd-init.md) y sus puntos de aprobación. Si ya existe, debe leer la constitución, revisar la arquitectura e identificar la especificación aplicable antes de modificar código.

Consulta [`AGENTS.md`](AGENTS.md) para ver las reglas que describen el comportamiento esperado del agente.

---

## 📐 Convenciones

- **Idioma:** Español (documentación, mensajes de commit, código)
- **Especificaciones:** Usar notación EARS para requisitos funcionales (RF-x)
- **Tareas:** Máximo 20-30 minutos por tarea, con checkbox y criterio "Hecho cuando:"
- **Tests primero:** Escribir tests antes del código de implementación
- **Sin sobreingeniería:** Solo lo necesario para cumplir el requerimiento actual

---

## 🛠️ Comandos

Este repositorio no incluye comandos ejecutables de inicialización o migración: esos flujos se realizan con los prompts de la sección [Cómo empezar](#-cómo-empezar). Los comandos para ejecutar, probar o formatear deben definirse en el `AGENTS.md` del proyecto objetivo.

*(Pendiente de definir según el proyecto específico)*

| Acción | Comando |
|--------|---------|
| Ejecutar | `<por definir>` |
| Tests | `<por definir>` |
| Lint/formato | `<por definir>` |

---

## 📄 Licencia

*(Agrega aquí la licencia de tu proyecto)*