# SDD Base IA

**Plantilla base para desarrollo de software guiado por especificaciones (SDD) con asistencia de IA.**

Este repositorio proporciona la estructura inicial y las reglas de trabajo para proyectos que siguen la metodología **Specification-Driven Development (SDD)**, donde cada funcionalidad comienza con una especificación formal antes de escribir una sola línea de código. El agente de IA (`pi`) utiliza esta estructura para mantener trazabilidad, claridad y disciplina en cada fase del desarrollo.

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

1. **Clona este repositorio** como base para tu nuevo proyecto.
2. **Sigue la guía de inicialización** en [`docs/sdd-init.md`](docs/sdd-init.md) — el agente IA te guiará fase por fase partiendo desde la constitución.
3. **Personaliza `AGENTS.md`** con los datos reales de tu proyecto (descripción, comandos, convenciones).
4. **Comienza a desarrollar** siguiendo el ciclo SDD: cada nueva funcionalidad abre una carpeta en `specs/`.

---

## 🤖 Uso con el agente IA (`pi`)

Este proyecto está diseñado para trabajar con el agente de codificación `pi`. Al iniciar una sesión, el agente:

1. Verifica si existe la estructura SDD (`specs/` y `docs/constitution.md`).
2. Si **no existe**, lee [`docs/sdd-init.md`](docs/sdd-init.md) y ejecuta las fases de inicialización paso a paso.
3. Si **existe**, lee la constitución, la arquitectura y la especificación activa antes de tocar código.

Consulta [`AGENTS.md`](AGENTS.md) para ver las reglas detalladas del agente.

---

## 📐 Convenciones

- **Idioma:** Español (documentación, mensajes de commit, código)
- **Especificaciones:** Usar notación EARS para requisitos funcionales (RF-x)
- **Tareas:** Máximo 20-30 minutos por tarea, con checkbox y criterio "Hecho cuando:"
- **Tests primero:** Escribir tests antes del código de implementación
- **Sin sobreingeniería:** Solo lo necesario para cumplir el requerimiento actual

---

## 🛠️ Comandos

*(Pendiente de definir según el proyecto específico)*

| Acción | Comando |
|--------|---------|
| Ejecutar | `<por definir>` |
| Tests | `<por definir>` |
| Lint/formato | `<por definir>` |

---

## 📄 Licencia

*(Agrega aquí la licencia de tu proyecto)*