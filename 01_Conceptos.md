# 01 - Conceptos a Git y GitHub

En este módulo aprenderás las bases de **Git** y **GitHub**, dos herramientas esenciales para el control de versiones y la colaboración en proyectos de software.

---

## ¿Qué es Git?

Git es un **sistema de control de versiones distribuido**.  
Permite que varias personas trabajen en el mismo proyecto al mismo tiempo sin sobrescribir los cambios de los demás.  
Con Git puedes:

- Registrar el historial de cambios de tus archivos.
- Volver a versiones anteriores si es necesario.
- Trabajar de forma segura en equipo o individualmente.

> [!TIP]
> 💡Git funciona localmente en tu máquina y no requiere internet para su uso básico..

---
### Concepto de versión

Una **versión** es el estado único de un proyecto en un momento específico. A medida que el proyecto avanza, se generan versiones para registrar el progreso.


Ej. Desarrollo de una Investigacion:
* v1: Hipótesis
* v2: Introducción
* v3: Desarrollo
* v4: Fin de desarrollo
* v5: Conclusiones
* v6: Resumen

---

### Importancia del control de versiones

El control de versiones es clave porque:

* Los proyectos suelen tener múltiples archivos
* Participan varias personas
* Evolucionan de forma continua 

**Ventajas**:
- Acceso a versiones 
- Facilita el trabajo en equipo
- Mejora la productividad
- Copias de seguridad automáticas
- Facilita la identificación y reversión de errores

---

### Tipos de control de versiones

**Local**:

* Historial en la máquina del desarrollador
* Simple, sin colaboración directa
* Riesgo de pérdida si falla el equipo

**Centralizado** (Ej. SVN):

* Historial en un servidor central
* Coordinación entre equipo
* Dependencia del servidor (si falla, todos parados)

**Distribuido** (Ej. Git):

* Cada desarrollador tiene el historial completo
* Trabajo offline posible
* Mejor gestión de ramas y fusiones
* Respaldo automático

---

## ¿Qué es GitHub?

GitHub es una **plataforma en la nube** que almacena repositorios Git y facilita el trabajo colaborativo.  
Además de alojar el código, ofrece herramientas como:

- Pull requests para proponer y revisar cambios.
- Issues para dar seguimiento a tareas o errores.
- Proyectos para organizar y priorizar el trabajo.
- Automatizaciones y acciones (GitHub Actions).

> [!TIP]
> 💡GitHub sí requiere conexión a internet porque trabaja en la nube.


---

## Diferencias entre Git y GitHub

| Git | GitHub |
|------|--------|
| Sistema de control de versiones | Plataforma para alojar y gestionar repos Git |
| Funciona localmente en tu máquina | Funciona en la nube |
| No necesita internet para funcionar | Necesita internet para subir y colaborar |
| Se usa por terminal o herramientas GUI | Se usa por navegador web o API |

---

## Ventajas de usarlos juntos

- Permiten trabajar en equipo de forma ordenada y segura.
- Tu proyecto queda respaldado en la nube.
- Se pueden gestionar tareas, bugs y mejoras.
- Facilitan la colaboración mediante revisiones de código y pull requests.

---
## Resumen del modulo

En este resumen se recopilan los conceptos fundamentales vistos en el módulo, ofreciendo una visión clara y concisa de qué es Git, qué es GitHub, cómo se diferencian y por qué su uso conjunto es esencial para el desarrollo colaborativo de software.

| Contenido | Descripcion Clave              |
| ----------| ------------------------------ |
| **Git**                  | Control de versiones local y distribuido. Registra cambios y permite colaboración. |
| **Versión**              | Estado guardado del proyecto en un momento específico.                             |
| **Control de versiones** | Orden, historial, trabajo en equipo y recuperación de errores.                     |
| **Tipos**                | Local, centralizado y distribuido (Git).                                           |
| **GitHub**               | Plataforma en la nube para alojar y colaborar en proyectos Git.                    |
| **Git vs GitHub**        | Git es la herramienta, GitHub es la plataforma.                                      |
| **Uso conjunto**         | Desarrollo local + respaldo y colaboración en la nube.                             |

---

➡ **Siguiente módulo recomendado:** [02_Configuracion.md](02_Configuracion.md)

---
