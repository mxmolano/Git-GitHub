# 01. Control de Versiones y Git

---

### 📌 Concepto de versión

Una **versión** es el estado único de un proyecto en un momento específico. A medida que el proyecto avanza, se generan versiones para registrar el progreso.

Ej. Desarrollo de una Investigacion:
* v1: Hipótesis
* v2: Introducción
* v3: Desarrollo
* v4: Fin de desarrollo
* v5: Conclusiones
* v6: Resumen

---

### 📌 Importancia del control de versiones

El control de versiones es clave porque:

* Los proyectos suelen tener múltiples archivos
* Participan varias personas
* Evolucionan de forma continua

**Ventajas**:
- ✅ Acceso a versiones 
- ✅ Facilita el trabajo en equipo
- ✅ Mejora la productividad
- ✅ Copias de seguridad automáticas
- ✅ Facilita la identificación y reversión de errores

---

### 📌 Tipos de control de versiones

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

### 📌 ¿Qué es Git?

**Git** es un sistema de control de versiones distribuido (creado en 2005 por Linus Torvalds).

Características:

✅ Gratuito
✅ Eficiente y rápido
✅ Código abierto
✅ Manejo avanzado de ramas y fusiones
✅ Copias completas en cada máquina

---

### 📌 ¿Qué es GitHub?

**GitHub** es una plataforma en la nube que aloja proyectos usando Git.

Características:

✅ Almacenamiento de proyectos en la nube
✅ Colaboración y trabajo en equipo
✅ Gestión de issues y tareas
✅ CI/CD (Integración / entrega continua)
✅ Interfaz web amigable

---

### 📌 Git vs GitHub

| Git                                  | GitHub                                  |
| ------------------------------------ | --------------------------------------- |
| Sistema de control de versiones      | Plataforma para compartir proyectos Git |
| Gratuito                             | Planes gratuitos y de pago              |
| Hecho por la comunidad (open source) | Empresa (Microsoft)                     |
| Uso en terminal                      | Uso en navegador web                    |


---

### 📌 Creación de cuenta en GitHub

1. Ir a [github.com](https://github.com)
2. Crear cuenta gratuita
3. Confirmar correo electrónico
4. Completar el perfil básico

---

### 📌 Instalación de Git

En Windows:

1. Descargar: [git-scm.com](https://git-scm.com/)
2. Ejecutar el instalador (opciones por defecto)
3. Verificar instalación:

```bash
git --version
```

---

### 📌 Configuración inicial de Git

Configurar nombre y correo:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
```

---
