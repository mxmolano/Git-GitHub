# 02. Manejo de Repositorios

## 📌 ¿Qué es un repositorio de Git?

Un **repositorio de Git** es una carpeta en el computador que contiene una subcarpeta llamada `.git`, donde se almacena toda la información relacionada con las versiones del proyecto.  
Esta subcarpeta suele estar oculta por defecto, pero se puede visualizar utilizando el comando:

```bash
dir /a
```

---

### Áreas de Git

1. **Área de trabajo** → Lo que estamos modificando actualmente
2. **Área de staging** → Cambios preparados para ser guardados (pero aún no en historial)
3. **Área de repositorio** → Cambios guardados en el historial de versiones (commits)

---

## 👀 Repositorios locales y remotos

* **Local** → En el computador personal (desarrollo, pruebas, commits)
* **Remoto** → En un servidor (GitHub, GitLab, Bitbucket) — acceso compartido

---

## 📌 Creación de repositorios

Pasos básicos:

1. Crear el repositorio local en el computador:

   ```bash
   git init
   ```

2. Crear el repositorio remoto en GitHub

3. Conectar el local con el remoto:

   ```bash
   git remote add origin https://github.com/tuusuario/tu-repo.git
   ```

---
## 🔑 Comandos Claves de Git
Esta sección contiene los comandos más comunes que vas a utilizar en tu trabajo diario con Git y GitHub, organizados por categorías.  
Cada comando va explicado, con su función y un ejemplo del posible resultado.

---
#### 🖥️ 1. Navegación en terminal (Windows)

Cambia de carpeta
```bash
cd carpeta
```

Lista todos los archivos y carpetas (incluyendo ocultos, como .git)
```bash
dir /a
```
---
#### 🗂️ 2. Inicialización de repositorio Git

Inicializa un repositorio Git en la carpeta actual
```bash
git init

# Resultado: Initialized empty Git repository in C:/ruta/.git/
```

---

#### 🔍 3. Estado del repositorio

Muestra el estado actual del repositorio
```bash
git status

# Resultado:
# - Archivos cambiados (modified)
# - Archivos en staging (ready to commit)
# - Archivos no rastreados (untracked)
# - Commits pendientes por subir (push)
```

---

#### ➕ 4. Preparar archivos (Staging)

Agrega un archivo específico al staging
```bash
git add README.md

# Resultado: el archivo queda preparado para el próximo commit
```

Agrega todos los archivos cambiados al staging
```bash
git add .

# Resultado: todos los archivos preparados para commit
```

---

#### 💾 5. Guardar cambios (Commit)

Guarda los cambios preparados en un commit con mensaje
```bash
git commit -m "mensaje del commit"

# Resultado:
# [main abc123] mensaje del commit
# N files changed, insertions(+), deletions(-)
```

---

#### 📜 6. Ver historial de commits
Muestra el historial de commits
```bash
git log

# Resultado: lista de commits con hash, autor, fecha y mensaje
```

---

#### 🌿 7. Gestión de ramas

Renombra la rama actual a 'main'
```bash
git branch -m main
# Resultado: la rama actual ahora se llama 'main'
```

---

#### 🌐 8. Repositorio remoto (GitHub)

Agrega un repositorio remoto (GitHub)
```bash
git remote add origin https://github.com/tuusuario/tu-repo.git

# Resultado: conexión establecida entre local y remoto
```

Sube los commits a la rama 'main' en el remoto
```bash
git push -u origin main

# Resultado:
# Branch 'main' set up to track remote branch 'main' from 'origin'.
# Subida completada
```
