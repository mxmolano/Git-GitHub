# 05. Conflictos de Git

## ⚔️ ¿Qué es un conflicto en Git?

Un **conflicto** ocurre cuando Git no puede decidir automáticamente cómo combinar los cambios de dos ramas porque las mismas partes del código fueron modificadas. Tú, como desarrollador, debes indicarle cómo resolverlo.

---

## 🔥 Tipos de conflictos y cómo resolverlos

### 1️⃣ Git falla al iniciar el merge

📌 **Mensaje típico:**  
`entry <fileName> not updated. Cannot merge. (changes in working directory)`

**¿Por qué pasa?**  Porque tienes cambios sin guardar y el merge podría sobrescribirlos.

➡ **¿Cómo solucionarlo?**

- `git commit` → Guarda los cambios en un commit antes de hacer merge.
- `git stash` → Guarda los cambios temporalmente y deja el área de trabajo limpia.
- `git reset` → Quita archivos del área de staging.
- `git checkout -- <file>` → Descarta los cambios de un archivo específico en el área de trabajo.

---

### 2️⃣ Git falla durante el merge

**¿Por qué pasa?**  Porque hay cambios incompatibles entre las ramas que intentas unir (modificaciones en las mismas líneas).
 
➡ **¿Cómo solucionarlo?**
- Abre los archivos con conflicto (Git los marcará).
- Edita el archivo y elige qué partes de los cambios conservar.
- Marca el conflicto como resuelto con:
  ```bash
  git add archivo_resuelto
  ``` 
  Luego finaliza con:
  
  ```bash
  git commit
  ```

💡 GitHub Web:
GitHub te notificará los conflictos y puedes resolverlos directamente desde la interfaz web usando el editor de conflictos.

---

### ✅ Consejos finales

- Antes de hacer merge, asegúrate de que tu área de trabajo esté limpia (git status).

- Resuelve los conflictos uno a uno y prueba tu código antes de confirmar los cambios.

- Documenta qué decisiones tomaste al resolver un conflicto en el mensaje de commit.

---

⚡ **Siguiente paso:** Guarda este contenido en un archivo llamado `Conflictos.md` y agrégalo a tu repositorio con:

```bash
git add Conflictos.md
git commit -m "Agrega guía de resolución de conflictos"
git push origin main
```