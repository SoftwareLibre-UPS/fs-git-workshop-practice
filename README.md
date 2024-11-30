
# Práctica de Git - Software Libre

Bienvenidos a la **parte práctica del curso de Git de la UPS**. Esta práctica está diseñada para aplicar los conceptos fundamentales de Git que hemos estudiado, incluyendo ramas, manejo de conflictos, commits, rebase, y mucho más. ¡Sigue las instrucciones paso a paso!

---

## **1. Preparación Inicial**

### 1.1 Fork del Repositorio

1. Realiza un **fork** de este repositorio en tu cuenta de GitHub.
2. En tu fork, configura un valor en el repositorio usando `git config` con las siguientes llaves:
   - `integrantes.uno`: Nombre y apellido del primer integrante.
   - `integrantes.dos`: Nombre y apellido del segundo integrante.
   
   Ejemplo:
   ```bash
   git config --add integrantes.uno "Nombre1 Apellido1"
   git config --add integrantes.dos "Nombre2 Apellido2"
   ```

### 1.2 Clonación del Repositorio

1. Cada integrante debe clonar el repositorio de forma local con:
   ```bash
   git clone <url-del-repositorio>
   ```

2. Agrega a los integrantes como **colaboradores** en tu fork desde GitHub para que ambos puedan trabajar en el repositorio.

---

## **2. Primera Parte: Configuración de Archivos**

### 2.1 Crear Archivos `.bin`

1. Cada integrante debe crear un archivo con su nombre y apellido en formato `.bin` en la rama principal.  
   Ejemplo:  
   - `JuanPerez.bin`
   - `MariaLopez.bin`

2. Realiza un commit y súbelo al repositorio:
   ```bash
   git add <archivo.bin>
   git commit -m "Add: archivo bin con nombre y apellido"
   git push origin main
   ```

---

## **3. Segunda Parte: Ramas y Gitignore**

### 3.1 Configuración en la Rama Uno

1. Crea una rama llamada `uno`:
   ```bash
   git checkout -b uno
   ```

2. En esta rama, crea un archivo `.gitignore` que incluya las siguientes reglas:
   - Ignorar el archivo `claves.txt`.
   - Ignorar todos los archivos `.pdf`.
   - Ignorar el directorio de imágenes.
   - Ignorar todos los archivos `.log` en el directorio `resultados`.
   - Ignorar archivos `.bin` con el nombre y apellido de cada persona.

   Contenido del archivo `.gitignore`:
   ```
   claves.txt
   *.pdf
   imagenes/
   resultados/*.log
   JuanPerez.bin
   MariaLopez.bin
   ```

3. Realiza un commit con este archivo y súbelo al repositorio:
   ```bash
   git add .gitignore
   git commit -m "Add: archivo .gitignore con reglas específicas"
   git push origin uno
   ```

### 3.2 Resolución de Conflictos

1. Este paso generará un **conflicto**. Resuélvelo manualmente editando los archivos en conflicto.
2. Marca los conflictos resueltos:
   ```bash
   git add <archivos-resueltos>
   git commit -m "Resolve: conflictos en archivo .gitignore"
   ```

3. Sube los cambios al repositorio:
   ```bash
   git push origin uno
   ```

---

## **4. Tercera Parte: Trabajando con Otras Ramas**

### 4.1 Rama Dos

1. Crea la rama `dos` desde la rama `uno`:
   ```bash
   git checkout -b dos
   ```

2. **Elimina el archivo `.gitignore`** de esta rama.  
   Realiza un commit:
   ```bash
   git rm .gitignore
   git commit -m "Remove: archivo .gitignore"
   ```

3. Sube los cambios:
   ```bash
   git push origin dos
   ```

---

### 4.2 Rama Tres: Eliminar un Commit

1. En la rama `tres`, identifica el commit que contiene el archivo `claves`.
   ```bash
   git log --oneline
   ```

2. Elimina ese commit del historial:
   ```bash
   git rebase -i <hash-anterior-al-commit>
   ```

3. Sube los cambios:
   ```bash
   git push origin tres --force
   ```

---

### 4.3 Rama Cuatro: Revertir un Cambio

1. Cambia a la rama `cuatro`:
   ```bash
   git checkout cuatro
   ```

2. Identifica el commit que modificó `archivoD.md`:
   ```bash
   git log -- archivoD.md
   ```

3. Regresa a ese commit y crea un nuevo commit sin esos cambios:
   ```bash
   git revert <hash-del-commit>
   git commit -m "Revert: cambios en archivoD.md"
   ```

4. Sube los cambios:
   ```bash
   git push origin cuatro
   ```

---

## **5. Creación de Ramas Personales**

1. Cada integrante debe crear una rama con su nombre desde la rama `cuatro`.  
   Ejemplo:
   ```bash
   git checkout -b JuanPerez
   ```

2. Combina los cambios de la rama `dos` con tu rama:
   ```bash
   git merge dos
   ```

3. Sube tu rama al repositorio:
   ```bash
   git push origin JuanPerez
   ```

---

## **6. Finalización**

1. Confirma que todas las ramas (`uno`, `dos`, `tres`, `cuatro`, y las personales) estén actualizadas en el repositorio.
2. Verifica que los commits sean consistentes y que no queden claves o archivos no deseados en el historial.

¡Felicidades, has completado la práctica de Git! 🎉
``` 

### Características del README:
1. **Estructura clara:** Cada paso está organizado por partes con numeración y subtítulos.
2. **Comandos específicos:** Se incluyen ejemplos de comandos reales.
3. **Mensajes personalizados:** Mensajes de commit claros para mantener un historial limpio.
4. **Práctica colaborativa:** Incluye acciones colaborativas como forks y conflictos.

