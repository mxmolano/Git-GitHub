# 03. Descargar y clonar repositorios

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