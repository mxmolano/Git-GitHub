# 02 - Configuración

En este módulo configurarás todo lo necesario para comenzar a trabajar con Git y GitHub, incluyendo la creación de cuenta, la instalación del software y su configuración básica. Estos pasos iniciales aseguran que tu entorno esté listo para gestionar versiones de forma eficiente y colaborar en proyectos.

---

## Creación de cuenta en GitHub

GitHub es una plataforma en la nube que te permite almacenar tus repositorios Git, colaborar con otros desarrolladores y acceder a herramientas para gestionar tus proyectos.

### Pasos para crear una cuenta:

1. Ir a [https://github.com](https://github.com)
2. Hacer clic en **Sign up**.
3. Ingresar correo, nombre de usuario y contraseña.
4. Elegir el plan **Free** (gratuito).
5. Confirmar el correo electrónico desde la bandeja de entrada.
6. (Opcional) Activar **autenticación de dos factores (2FA)** para mayor seguridad.

> [!NOTE]  
> 💡 Más adelante puedes configurar una clave SSH para mayor seguridad y comodidad al subir cambios.

---

## 📝 Instalación de Git

Git se debe instalar en tu equipo para que puedas trabajar con repositorios localmente.

---
### Windows

1. Descargar desde [git-scm.com](https://git-scm.com/download/win)
2. Ejecutar el instalador con las opciones por defecto.
3. Usar **Git Bash** como terminal recomendada.

4. Verifica la instalación, Muestra la versión instalada de Git

    ```bash
    git --version

    # El número de versión puede variar. Lo importante es que el sistema reconozca el comando sin errores.
    ```

---
### MacOS

Para instalar Git en macOS, puedes usar **Homebrew** o permitir que macOS lo instale automáticamente cuando lo necesites.

#### Opción 1: Instalar Git con Homebrew (recomendado)

1. Abre la aplicación Terminal.
2. Descarga e instala Git desde los repositorios de Homebrew 

    ```bash
    brew install git 

    # Progreso de descarga e instalación en la terminal. 
    # Al finalizar, Git queda disponible para su uso en todo el sistema.
    ```
    
3. Luego verifica si la instalación fue exitosa con:

    ```bash
    git --version

    # El número de versión puede variar. Lo importante es que el sistema reconozca el comando sin errores.
    ```


#### Opción 2: Instalación automática al verificar versión

1. Abre la Terminal y escribe:

    ```bash
    git --version

    ```
2. Acepta la instalación y espera a que finalice.

**¿Qué pasa aquí?**
Si Git **no está instalado**, macOS mostrará un mensaje emergente pidiéndote instalar las herramientas de línea de comandos.

--- 

### Linux

Linux es un sistema operativo, como Windows o macOS. Pero a diferencia de ellos, Linux tiene muchas versiones distintas, llamadas **distribuciones** (o "distros"). 

Cada distribución tiene su estilo, herramientas y forma de instalar programas. Algunas de las más populares son:

- **Ubuntu** o **Debian** → Fáciles de usar, ideales para principiantes.
- **Fedora** → Moderna, rápida y con tecnologías recientes.
- **Arch Linux** o **Manjaro** → Más avanzadas y personalizables.

> Antes de instalar Git, necesitas saber qué distribución estás usando.

### ¿Cómo saber qué distribución de Linux tienes?

1. Abre la terminal (normalmente con `Ctrl + Alt + T`).
2. Escribe:

   ```bash
   cat /etc/os-release
   ```

3. Presiona Enter. Verás algo como:

   ```text
   NAME="Ubuntu"
   ID=ubuntu
   ```

   Eso te dice qué distribución estás usando.

--- 

### Instalación de Git según la distribución

####  Distribucion 1: Ubuntu o Debian (Instalación con `apt`)

1. Abrir la terminal.

2. Actualizar la lista de paquetes del sistema:

   ```bash
   sudo apt update
   ```
   - `sudo`: ejecuta el comando con permisos de administrador.
   - `apt update`: busca actualizaciones de software disponibles.

3. Instalar Git:

   ```bash
   sudo apt install git
   ```
   - `apt install git`: descarga e instala Git desde los servidores oficiales.

4. Confirmar instalación: escribe `Y` y presiona Enter si se te pregunta.

5. Verificar la instalación:

   ```bash
   git --version

   # El número de versión puede variar. Lo importante es que el sistema reconozca el comando sin errores.
   ```

#### Distribucion 2: Fedora (Instalación con `dnf`)

1. Abrir la terminal.

2. Instalar Git con DNF:

   ```bash
   sudo dnf install git
   ```
   - `dnf install git`: descarga Git desde los repositorios de Fedora.

3. Confirmar instalación: escribe `Y` y presiona Enter si se te pregunta.

4. Verificar la instalación:

   ```bash
   git --version

   # El número de versión puede variar. Lo importante es que el sistema reconozca el comando sin errores.
   ```

#### Distribucion 3: Arch Linux o Manjaro (Instalación con `pacman`)

1. **Abrir la terminal**.

2. **Instalar Git con Pacman:**

   ```bash
   sudo pacman -S git
   ```
   - `pacman -S git`: busca e instala Git desde los repositorios de Arch.

3. **Aceptar la instalación:** presiona `Y` si se te solicita.

4. **Verificar la instalación:**

   ```bash
   git --version

   # El número de versión puede variar. Lo importante es que el sistema reconozca el comando sin errores.
   ```

---

## Configuración inicial de Git

Después de instalar Git, debes realizar algunas configuraciones básicas para que tu identidad quede registrada en los repositorios y Git se comporte correctamente según tu sistema operativo.

1. Configurar nombre y correo :

    Esto asegura que tus commits se asocien a tu identidad. Usa el mismo correo que registraste en GitHub.

    ```bash
    git config --global user.name "Tu Nombre"
    git config --global user.email "tu.email@ejemplo.com"
    ```

2. Verificar configuración actual: 

    Muestra toda la configuración activa de Git (nombre, correo, editor, colores, etc.).
    ```bash
    git config --list
    ```

3. Configurar editor por defecto (opcional):

    Esto hará que Git use VSCode cada vez que necesite abrir un mensaje de commit u otra edición

    ```bash
    git config --global core.editor "code --wait"
    ```

4. Configurar finales de línea (según sistema operativo): 

    Esto evita problemas de compatibilidad en los saltos de línea al compartir proyectos entre sistemas distintos.

    **Windows:**

    ```bash
    git config --global core.autocrlf true
    ```

    **macOS / Linux:**

    ```bash
    git config --global core.autocrlf input
    ```

5. Activar colores en la terminal:

    Mejora la legibilidad de los mensajes en consola al usar colores para distinguir estados.

    ```bash
    git config --global color.ui auto
    ```

6. Crear alias para comandos frecuentes (opcional):

    Facilitan el uso de comandos más cortos. Ej: `git st` en lugar de `git status`.

    ```bash
    git config --global alias.st status
    git config --global alias.co checkout
    git config --global alias.ci commit
    git config --global alias.br branch
    ```

---
## Resumen del modulo

En este resumen se recopilan los pasos esenciales para preparar tu entorno de trabajo con Git y GitHub. Aprendiste a crear una cuenta en GitHub, instalar Git según tu sistema operativo (Windows, macOS o Linux), y realizar las configuraciones iniciales necesarias para comenzar a trabajar con control de versiones de forma correcta y segura. Esta preparación es clave para garantizar una experiencia fluida al colaborar en proyectos de desarrollo.

| Contenido | Descripcion Clave              |
| ----------| ------------------------------ |
| **Cuenta en GitHub**                  | Crear cuenta gratuita en [GitHub](https://github.com), confirmar correo electrónico y (opcional) activar la autenticación de dos factores (2FA).    |
| **Instalación en Windows**            | Descargar desde [git-scm.com](https://git-scm.com/download/win), ejecutar el instalador con opciones por defecto y usar **Git Bash** como terminal. |
| **Instalación en macOS**              | Usar **Homebrew** con `brew install git` o permitir instalación automática al ejecutar `git --version`.                                             |
| **Instalación en Linux**              | Ejecutar en terminal:<br>• Ubuntu/Debian: `sudo apt install git`<br>• Fedora: `sudo dnf install git`<br>• Arch/Manjaro: `sudo pacman -S git`        |
| **Verificación**                      | Confirmar instalación de Git con `git --version`.                                                                                                   |
| **Configuración de usuario**          | Registrar nombre y correo con:<br>`git config --global user.name`<br>`git config --global user.email`.                                              |
| **Ver configuración actual**          | Ver ajustes activos con `git config --list`.                                                                                                        |
| **Editor por defecto**                | Configurar VSCode como editor para Git:<br>`git config --global core.editor "code --wait"`.                                                         |
| **Saltos de línea (`core.autocrlf`)** | Ajustar para evitar errores al colaborar:<br>• Windows: `true`<br>• macOS/Linux: `input`.                                                           |
| **Colores en terminal**               | Activar colores con `git config --global color.ui auto`.                                                                                            |
| **Alias de comandos**                 | Crear accesos rápidos opcionales:<br>`st` → `status`, `co` → `checkout`, `ci` → `commit`, `br` → `branch`.                                          |

---

¿Deseas que convierta esto en un bloque Markdown directamente editable?

---

➡ **Siguiente módulo recomendado:** [03_Descargar_Repositorios.md](03_Descargar_Repositorios.md)

---
