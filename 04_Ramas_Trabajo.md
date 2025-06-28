# 04. Ramas de trabajo en Git

## 🌿 ¿Que son las Ramas de trabajo?
En Git, las **ramas** son como líneas de tiempo paralelas que permiten trabajar en nuevas características o correcciones sin afectar el código estable. Cuando terminas, puedes unir (`merge`) esos cambios a la rama principal.

## 🚀 ¿Qué es main o master?

`main` (o `master` en algunos proyectos) es el **flujo principal de trabajo**. Es donde vive la versión **estable y lista para producción** del proyecto.

⚠ **No es recomendable hacer cambios directamente en `main`**, ya que puedes afectar la estabilidad del proyecto, sobre todo en equipos de trabajo.

---

## 🔑 Comandos Claves para ramas

#### 🌿 1. Ver las ramas existentes
Muestra todas las ramas del repositorio y en cuál estás trabajando actualmente (marcada con *).

``` bash 
git branch

# * main
#   develop
```
---
#### 🔄 2. Cambiar a la rama main
Te permite moverte a la rama principal main para trabajar en ella.

```bash
git switch main

# Cambiado a rama 'main'
```
---

#### ✨ 3. Crear y cambiar a una nueva rama
Crea una nueva rama (por ejemplo nueva-rama) y cambia a ella automáticamente.

```bash
git switch -c nueva-rama

# Cambiado a una nueva rama 'nueva-rama'
```
---

#### 🔀 4. Fusionar una rama con la actual
Combina los cambios de otra rama (por ejemplo nombre-rama) en la rama en la que estás trabajando.

```bash
git merge nombre-rama

# Fusionando rama 'nombre-rama' en la rama actual
# Todo actualizado (o mostrará conflictos si los hay)
```
---

#### 🚀 5. Subir una nueva rama al repositorio remoto
Envía una nueva rama o actualizaciones de esa rama al repositorio en GitHub.

```bash
git push origin nombre-rama

# Subiendo rama a 'origin'
# Enumerando objetos: 5, hecho.
# Conteo de objetos: 100% (5/5), hecho.
# Delta compression usando hasta 4 hilos
# Empujando a https://github.com/tuusuario/tu-repo.git
```

---

## 👀 Visualización y gestión de ramas

En GitHub o con herramientas como `git log --graph` puedes:

- Ver cuántos commits está adelantada o atrasada tu rama respecto a `main`.
- Cambiar el nombre de una rama
     ```bash
    git branch -m nombre-nuevo
    ```

- Eliminar una rama local
    ```bash
    git branch -d nombre-rama
    ```

- Eliminar una rama remota 
    ```bash
    git push origin --delete nombre-rama
    ```

- Filtrar y listar ramas activas/inactivas.

---

## 🔄 Actualizar tu rama de trabajo con cambios de `main`

Cuando trabajas en una rama diferente a `main`, es importante mantenerla actualizada con los últimos cambios de `main`.

1.  Descarga los cambios más recientes de `main`:

    ```bash
    git pull origin main
    ```

2. Cambia a tu rama de trabajo:

    ```bash
    git switch develop
    ```

3. Fusiona los cambios de `main` en tu rama:

    ```bash
    git merge main
    ```

💡 **Alternativa:**
En GitHub puedes hacer esto visualmente usando *Comparing changes* y creando un *Pull Request* para unir los cambios de `main` a tu rama.

---

## 🌟 Buenas prácticas

- ✨ Crea ramas con nombres claros, como `feature/login`, `fix/bug-login`, `docs/update-readme`.
- ✨ Sube tus ramas al remoto para tener un respaldo y facilitar el trabajo en equipo.
- ✨ Antes de hacer merge en `main`, asegúrate de probar tus cambios.

