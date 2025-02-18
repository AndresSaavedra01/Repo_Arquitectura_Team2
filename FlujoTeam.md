#Flujo de trabajo del Team-2

1. El scrum master crea el repositorio: 

    🔹Crea repositorio en GitHub

    🔹Agrega un archivo README.md

    🔹Crea la rama develop para  el desarrollo
    🔹

2. Cada miembro del equipo clona el repositorio en sus máquinas

    git clone <URL_DEL_REPO>
    
    git switch develop  # Cambiar la rama develop

    git pull origin develop  # Asegurar que tienen la última versión

3. Cada miembro crea su propia rama de trabajo: 

    git checkout -b feature/nombre_apellido 

    git push feature/nombre_apellido # Subir la rama al repositorio

4. Desarrollo y confirmación de cambios: cada miembro realiza sus cambios, en este proceso se realizan los comandos (si se desean hacer commits de lo que se agrega al archivo README.md): 

    git add .

    git commit -m "Implementación de nueva funcionalidad"

    git push origin feature-mi-rama

5. Hacer merge a develop

    Cuando el miembro termina su tarea, debe integrar sus cambios en develop, hay que asegurarse de que ya se ha terminado y esté la última versión de la rama al repositorio remoto.

    git switch develop / cambiar a rama develop
    
    git pull origin develop / actualizar contenido en develop

    git merge feature/nombre_apellido / merging

    git push origin develop / subir cambios al repositorio remoto

#En caso de conflictos

    Si git detecta conflictos, se indica con un mensaje similar a:

    CONFLICT (content): Merge conflict in README.md (nombre del archivo que tiene conflicto)

    En el editor, el archivo en conflicto tedrá marcadores de git: 

    <<<<<<< HEAD

    (Contenido de la rama principal)

    =======

    (Contenido de la rama secundaria)

    >>>>>> feature-branch

    Editar el archivo manualmente para mantener la versión deseada y eliminar los marcadores (<<<<<<<, =======, >>>>>>>), prestar atención a la información que contiene el archivo, se puede eliminar o mezclar la información

    Otra forma de resolver el conflicto es abrir el archivo directamente en Git Bash usando nano README.md, editarlo manualmente para combinar los cambios deseados y eliminar los marcadores (<<<<<<<, =======, >>>>>>>)


0. Confirmar cambios

    Después de editar el archivo correctamente, se tienen que confirmar los cambios, agregar el archivo y comitear:

    git add README.md /nombre archivo

    git commit -m "Resolviendo conflicto y combinando cambios de feature/nombre_apellido en develop"

    git push origin develop
