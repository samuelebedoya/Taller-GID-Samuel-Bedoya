gir# GIT: Ciclo de Vida y Comandos Básicos
### Actividad en Clase
Universidad el Bosque		
<br/>
Facultad de Comunicación y Creación 
<br/>
Programa de Creación Digital 
<br/>
<br/>
<br/>
En desarrollo necesitará usar Git como sistema de gestión de cambios de su repositorio, este ejercicio guiado le ayudará a familiarizarse con los comandos básicos y un recordatorio de HTML y CSS. **Para esta actividad será calificado su manejo de GIT**, _recuerde que según las pautas de clase, puede usar la inteligencia artificial como herramienta para sugerir mejoras o solución de código._

_Nota: Para este taller, toda creación, edición o eliminación de archivos y carpetas debe hacerse desde el editor de código (VS Code) o el explorador de archivos, no desde la terminal. Las únicas líneas de comando que escribirás son de Git._
<br/>
<br/>
<br/>
### EJERCICIO 0: Clonar un repositorio y primer commit
1. Ingrese a GitHub desde tu navegador y busque el repositorio.
2. Abra el repositorio, haga clic en el botón verde "Code" y copie la URL en formato HTTPS. 
3. Abra VS Code, y desde su terminal ubíquese en la carpeta donde quiera guardar sus proyectos.
4. Clone el repositorio usando la URL copiada.
5. Verifique que la carpeta se descargó correctamente abriéndola en VS Code
6. Revise el historial de commits que trae desde el remoto y confirme que la conexión con el repositorio remoto ya quedó configurada automáticamente.

### EJERCICIO 1: Crear el primer commit
1. Desde el explorador de archivos, cree una carpeta llamada tienda-online en Escritorio y ábrala en VS Code.
2. Cree dentro los archivos index.html, styles.css y app.js usando el editor.
3. Abra la terminal integrada de VS Code (ya estará ubicado en la carpeta del proyecto) e inicializa el repositorio de Git.
4. Verifique el estado para confirmar que Git detecta los tres archivos como no rastreados. Agréguelos al staging area, realiza el primer commit y verifica que quedó registrado.

### EJERCICIO 2: Ignorar archivos sensibles
1. Desde VS Code, cree un archivo llamado config.env y escriba dentro una clave ficticia (número hexadecimal cualquiera) y una carpeta llamada node_modules.
2. Cree también un archivo .gitignore y escriba dentro las reglas para ignorar ambos elementos.
3. Verifique desde la terminal que Git ya no los detecta como cambios pendientes.
4. Agregue al staging únicamente el .gitignore y haga el commit.

### EJERCICIO 3: Ver diferencias antes de confirmar
1. Abre index.html en VS Code y escriba la estructura básica de un documento HTML5 (doctype, html, head con título, body).
2. Guarde el archivo.
3. Antes de agregarlo al staging, revise desde la terminal qué líneas exactamente cambiaron.
4. Agréguelo al staging y vuelve a revisar las diferencias, esta vez las que ya están preparadas. 
5. Haga el commit.

### EJERCICIO 4: Corregir el último commit
Se da cuenta de que el commit anterior debía incluir también los estilos base.
1. Abra styles.css en VS Code y escriba un reset básico (margin, padding, box-sizing y font-family en el body).
2. Guarde y agregue el archivo al staging e incorpórelo al commit anterior sin crear uno nuevo, conservando el mismo mensaje.
3. Verifique el historial para confirmar que la cantidad de commits no aumentó.

### EJERCICIO 5: Descartar cambios no deseados
1. Abra app.js y escriba unas líneas cualesquiera.
2. Guarde el archivo.
3. Verifique el estado del repositorio y confirme que Git detecta el archivo como modificado.
4. Sin hacer commit, revierta el archivo exactamente al estado del último commit 
5. Verifique en VS Code que el contenido experimental desapareció.

### EJERCICIO 6: Trabajar con ramas
1. Cree una rama llamada feature-carrito y cambie a ella en un solo comando.
2. Desde VS Code, agregue alguna línea al archivo app.js.
3. Guarde y haga commit en esa rama.
4. Regrese a la rama principal y observe en VS Code que el archivo app.js volvió a su versión anterior.
5. Liste todas las ramas existentes para confirmar en cuál se encuentra.

### EJERCICIO 7: Fusionar una rama (merge sin conflictos)
1. Estando en la rama principal, fusione la rama feature-carrito para incorporar los cambios.
2. Verifique en VS Code que app.js ahora sí contenga los cambios.
3. Revise el historial con el gráfico de ramas para visualizar la fusión.
4. Una vez confirmado, elimine la rama feature-carrito y verifique que ya no aparece en el listado.

### EJERCICIO 8: Guardar trabajo temporalmente (stash)
1. Comience a trabajar en los estilos del footer: abra styles.css en VS Code y agrega una clase .footer con varias propiedades.
2. Guarda pero no hagas commit.
3. Imagine que un tercero me pide una corrección urgente en el título de la página, guarde temporalmente su trabajo con stash y verifique en VS Code que los cambios desaparecieron del archivo.
4. Cree y cambie a una rama hotfix-titulo, corrija el h1 en index.html desde el editor y haga commit. 
5. Regrese a la rama principal, consulte la lista de stashes y recupere tu trabajo guardado.

### EJERCICIO 9: Deshacer un commit ya publicado (revert)
1. Desde VS Code, agrega cualquier cambio.
2. Guarde y haga commit.
3. Revisa el historial.
4. Ahora, en lugar de borrar ese commit del historial, cree un nuevo commit que deshaga automáticamente esos cambios.
5. Verifique en VS Code que la función desapareció del archivo y revise el historial para confirmar que ahora existen dos commits: el original y el de reversión.

### EJERCICIO 10: Retroceder commits manteniendo los cambios (reset)
1. Desde VS Code, realice tres modificaciones separadas en index.html, haciendo un commit después de cada una.
2. Revise el historial y confirme que tenga tres commits. 
3. Decide que los tres debieron ser uno solo: retroceda los tres commits manteniendo todos los cambios preparados en el staging area, y cree un único commit que los agrupe. 
4. Verifique el historial nuevamente.

### EJERCICIO 11: Explorar un commit antiguo
1. Consulte el historial resumido y copie el hash de uno de sus primeros commits. 
2. Cambie a ese commit para explorar cómo estaba el proyecto en ese momento.
3. Observe en VS Code que los archivos volvieron a su versión antigua. 
4. Revisa el estado y notará que está en modo "detached HEAD". Sin hacer ningún cambio, regrese a la rama principal y confirme que los archivos volvieron a su versión actual.

### EJERCICIO 12: Sincronizar cambios del remoto
1. Desde la interfaz web de GitHub, entre a su repositorio, cree un archivo README.md usando el botón "Add file" y escriba una descripción del proyecto. 
2. Confirme el cambio directamente en GitHub.
3. Desde su terminal local, cambie a la rama principal y descargue los cambios sin fusionarlos todavía. 
4. Revise qué commits trae el remoto y qué diferencias existen respecto a su rama local. 
Una vez revisado, fusione los cambios y confirme en VS Code que el README.md apareció en tu proyecto.

### EJERCICIO 13: Ciclo completo de trabajo
1. Simule un día completo de trabajo profesional:
2. Empiece sincronizando su rama principal con el remoto.
3. Cree una rama llamada feature-checkout y cambie a ella.
4. Desde VS Code, cree un archivo checkout.html.
5. Revise el estado del repositorio, agregue el archivo al staging y revise las diferencias preparadas antes de confirmar. 
6. Haga commit y suba la rama al remoto. 
7. Regrese a la rama principal, fusione la funcionalidad, suba los cambios actualizados al remoto y finalmente elimine la rama tanto en local como en GitHub.
8. Verifique el listado completo de ramas para confirmar la limpieza.

<br/>
<br/>
<br/>

### Tabla de Resumen de Comandos de Git más utilizados

| Comando | Función |
| --- | --- |
| git init | Inicializar repositorio |
| git status | Ver estado de archivos |
| git add . / git add archivo | Agregar al staging area |
| git commit -m "mensaje" | Confirmar cambios |
| git commit --amend --no-edit | Modificar último commit |
| git log --oneline | Ver historial resumido |
| git log --oneline --graph --all | Ver historial con gráfico de ramas |
| git log rama1..rama2 --oneline | Ver commits exclusivos de una rama |
| git diff | Ver cambios sin staging |
| git diff --staged | Ver cambios en staging |
| git diff rama1 rama2 | Comparar dos ramas |
| git diff --stat rama1 rama2 | Resumen estadístico de diferencias |
| git restore archivo | Descartar cambios |
| git restore --staged archivo | Sacar del staging |
| git branch | Listar ramas locales |
| git branch -a | Listar todas las ramas (locales y remotas) |
| git branch -d nombre | Eliminar rama local |
| git checkout rama | Cambiar de rama |
| git checkout -b rama | Crear y cambiar de rama |
| git checkout hash | Explorar un commit antiguo |
| git merge rama | Fusionar rama |
| git stash | Guardar cambios temporalmente |
| git stash list | Ver lista de stashes |
| git stash pop | Recuperar cambios guardados |
| git revert HEAD --no-edit | Deshacer commit creando uno nuevo |
| git reset --soft HEAD~n | Retroceder commits manteniendo cambios |
| git remote add origin URL | Conectar repositorio remoto |
| git remote -v | Ver remotos configurados |
| git push -u origin rama | Subir rama con seguimiento |
| git push origin rama | Subir cambios al remoto |
| git push origin --delete rama | Eliminar rama remota |
| git fetch origin | Descargar sin fusionar |
| git pull origin rama | Descargar y fusionar |
