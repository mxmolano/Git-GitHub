# 03 -Descargar y clonar repositorios

## 🚀 ¿Qué significa clonar un repositorio?

Clonar un repositorio significa descargar el código completo de un proyecto desde GitHub (u otra plataforma) a tu computadora. Esto crea una copia exacta del proyecto para que puedas estudiarlo, modificarlo, colaborar o trabajar en él de forma local.

Es el primer paso cuando quieres colaborar en un proyecto existente o aprender de su código.

---

## 📝 Pasos para clonar un repositorio

1. Ingresa al repositorio en GitHub que deseas clonar.

2. Haz clic en el botón verde `Code` y copia la URL que aparece (puede ser HTTPS o SSH; en esta guía usamos **HTTPS**).

3. Abre tu terminal o PowerShell en la carpeta donde quieres guardar el proyecto.

4. Escribe el siguiente comando y presiona **Enter**:

    ```bash
    git clone URL-del-repositorio
    ```

    📌 Reemplaza URL-del-repositorio por la URL que copiaste en el paso 2.

    ✅ Ejemplo:

    ```bash
    git clone https://github.com/mxmolano/Git-GitHub.git  
    ```
--- 
### Actualizar el repositorio
Enviar tus cambios al repositorio remoto
Cuando hayas hecho cambios y quieras subirlos a GitHub:

```bash
git push origin main
# Esto envía tus cambios (commits) al repositorio remoto en la rama main.
```

Recibir cambios desde el repositorio remoto
Si alguien más hizo cambios o quieres actualizar tu copia local:

```bash
git pull origin main
# Esto descarga y aplica los últimos cambios del repositorio remoto.
```

---
## 💡 Consejos útiles
✔️ Revisa en qué carpeta estás antes de clonar, para no clonar en un lugar equivocado.

✔️ Si no tienes Git instalado, instálalo desde `git-scm.com`.

✔️ Si al hacer push te pide usuario y contraseña, probablemente el repositorio requiere autenticación. Usa un token personal (PAT) si trabajas con HTTPS.

✔️ Es buena práctica hacer git pull antes de empezar a trabajar, para tener la última versión del proyecto.


## 🔑 Comandos Claves

**Clonar un repositorio remoto**
```bash
git clone https://github.com/tuusuario/tu-repo.git
```

**Enviar cambios locales al repositorio remoto**
```bash
git push origin main
```
**Recibir cambios del repositorio remoto**
```bash
git pull origin main
```

-
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

#

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
