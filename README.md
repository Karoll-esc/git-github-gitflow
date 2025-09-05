Adriana Gonzalez

Generalidades de Git y GitHub

Git es un sistema de control de versiones que nos permite llevar un historial de los cambios realizados en los archivos de un proyecto.
Con Git podemos trabajar en equipo sin sobrescribir el trabajo de los demás, y también regresar a versiones anteriores si es necesario.

GitHub es una plataforma en línea que utiliza Git y nos permite compartir proyectos, colaborar con otras personas y guardar el código en la nube.

Instalación de Git

1. Ir a la página oficial: [https://git-scm.com/](https://git-scm.com/)
2. Descargar la versión correspondiente a tu sistema operativo (Windows, Mac o Linux).
3. Instalar dejando las opciones por defecto recomendadas.

Para verificar que la instalación se realizó correctamente, abrimos **Git Bash** y escribimos: git --versión
Si aparece un número de versión, significa que Git está instalado correctamente.

A continuación, los pasos básicos para crear un repositorio en tu computador y conectarlo con GitHub:

git init                             # Inicializa un repositorio local en la carpeta actual
git add .                            # Agrega todos los archivos al área de preparación
git commit -m "primer commit"        # Guarda los cambios en el repositorio local
git branch -M main                   # Cambia el nombre de la rama principal a 'main'
git remote add origin <url-del-repo> # Conecta tu repo local con el repo en GitHub
git push -u origin main              # Envía los cambios al repositorio remoto en GitHub

Nota: En la (url-del-repo) debes poner la dirección HTTPS de tu repositorio en GitHub.


Introducción a Git, Github y Gitflow
