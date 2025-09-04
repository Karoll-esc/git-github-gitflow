Introducción a Git, Github y Gitflow



\# 📖 Git es una herramienta que nos ayuda a guardar y controlar los cambios de un proyecto en nuestro computador y GitHub es como una nube donde podemos subir ese proyecto para tenerlo guardado y compartirlo con otras personas.





\#🖥️ El repositorio local es el que está en nuestra computadora.



\#☁️ El repositorio remoto es el que está en GitHub.



\#La idea es crear ambos y luego conectarlos, para que lo que hagamos en el computador se pueda enviar a GitHub y quede sincronizado.



\#💡 REPOSITORIO LOCAL Y REMOTO 



\#🖥️ Repositorio local en Git:

\#-Nos ubicamos en la carpeta en la cual quieres generar ese repositorio con el comando cd, si esta en documentos por ejemplo debes agregar cd documents y después cd "la carpeta de tu proyecto"

\#-Iniciamos Git en el Bash con el comando git init, este nos creara una carpeta oculta llamada .git 

\#-En la carpeta de tu archivo creamos un archivo llamado README.md, en el cual cada cambio que hagas lo debes confirmar con un git add y un commit.



\#☁️ Repositorio remoto en GitHub:

\#-Creamos una cuenta en GitHub e iniciamos sesión

\#-Creamos un repositorio en el apartado de New repository, le pones el nombre que desees y le haces en Create repository.

\#-Te aparecerá tu repositorio y dos códigos el cual nos brinda GitHub para poder generar conexión con el.



\#🔗 ¿Como generar la conexión con los repositorios local y remoto ya creados?

\#En Git Bash vas a indicar tu nombre de usuario de tu cuenta de GitHub y tu correo por medio del siguiente comando git config --global user.name "Nombre de usuario" y git config --global user.email "Correo electrónico"

\#Realizamos los pasos del repositorio local en Git y el repositorio remoto en GitHub 

\#Al obtener los códigos que GitHub nos ofrece copiamos el segundo código y lo pegamos en nuestro Git Bash

\#Se generara la conexión exitosamente y para enviar los commits que hagas en tu repositorio local al remoto utilizas el siguiente comando git push.

