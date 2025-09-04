
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

----

3\. Gerardo Leyton Rodríguez

(git add .) (git commit) (git push)



### **Conceptos clave antes de los comandos (repaso)**



Espacio de trabajo (Working Directory / Working Tree)

Es la carpeta en la computadora donde están los archivos del proyecto. Aquí es donde se editan los archivos normalmente, por ejemplo en el Bloc de notas, que es el que estamos usando.



**Área de preparación (Staging Area / Index)**

Es un espacio intermedio donde Git guarda los cambios que se quieren incluir en un próximo commit (punto de control o fotografía del proyecto en un momento específico), es decir como una “lista de espera”: los cambios están preparados pero todavía no forman parte de la historia del proyecto.



**Repositorio local**

Es donde Git guarda la historia completa del proyecto en la computadora. Cada commit se almacena aquí.



**Repositorio remoto**

Es un repositorio en línea, como GitHub, donde se pueden subir los commits para compartirlos o respaldarlos.



### **1. git add**



*Explicación*



git add le dice a Git qué cambios del espacio de trabajo se quiere mover al staging area para incluirlos en el próximo commit.



git add nombre\_del\_archivo ---> agrega un archivo específico al área de preparación.



git add . ----> agrega todos los archivos modificados dentro de la carpeta actual y sus subcarpetas.



*Importante:* git add no guarda los cambios de manera permanente en el historial de Git; solo los prepara para el commit, o sea como diciéndole a git que esos son los que se van a establecer pero no lo hace, solo lo indica.



*Ejemplo*



Supongamos que editó un archivo practica.md en el Bloc de notas.



Para preparar solo ese archivo:



git add practica.md





Para preparar todos los archivos modificados en la carpeta:



git add .



### **2. git commit -m "mensaje"**



*Explicación*



git commit toma todo lo que está en el staging area y lo guarda en el repositorio local, creando un punto de control en la historia del proyecto.



El -m "mensaje" permite describir claramente qué cambios se están guardando.



Buenas prácticas: el mensaje debe ser claro y explicar el cambio, por ejemplo: "agrega sección de práctica".



*Ejemplo*



Después de hacer git add practica.md, confirmar los cambios:



git commit -m "agrega nueva sección de practica.md"





Git mostrará algo como:



\[main 123abc] agrega nueva sección de practica.md

&nbsp;1 file changed, 3 insertions(+)





Esto indica que los cambios ya están guardados en el repositorio local.



### 3\. git push



*Explicación*



git push envía los commits (fotos) del repositorio local al repositorio remoto, en GitHub.



Antes de usar git push, debe existir un repositorio remoto creado y vinculado , puede ver el procedimiento en el punto 2 de este manual.





Luego se pueden enviar los commits con:



git push origin main





origin ----> nombre del repositorio remoto.



main ----> nombre de la rama a la que se envían los cambios.



También se puede utilizar git push solamente pero si la rama local ya está vinculada a una rama remota (punto 7 del manual) de lo contrario genera error, por lo cual es mejor hacerlo de la primera forma inicialmente.





*Ejemplo*



Si ya se confirmaron los cambios en la rama principal main:



git push origin main





*Ahora los cambios estarán reflejados en GitHub.*



#### Ejemplo práctico



Crear un archivo nuevo

se debe crear una carpeta primero para tener orden, por ejemplo en descargas o documentos, hay que recordar que están en inglés. El archivo se puede crear con un block de notas teniendo en cuenta el nombre y la extensión, para este caso .md



Carpeta: Documents/ejemplo\_git\_manual

Archivo: manual.md

dentro de ese archivo se escribe:



Este es mi primer archivo de práctica con Git





Editar el archivo manualmente en el Bloc de notas, se añade otra línea, por ejemplo:



Aprendiendo a usar git add, commit y push



Siempre hay que guardar y cerrar.



Preparar los cambios para commit



git add manual.md ---> Recordar que también se puede con git add .





Guarda los cambios en un commit



git commit -m "agregar linea sobre aprendizaje de git"





Enviar los cambios a GitHub



hay que asegurarse de haber creado un repositorio en GitHub y vinculado como se ve en otro punto del presente manual (2):



git remote add origin <URL-del-repositorio>

git branch -M main

git push -u origin main



Recordar el comando *git status*, que muestra el estado en ese momento de la rama y en cuál se encuentra situado.



Verificar en GitHub (Revisar punto del manual 2).



Ingresar al repositorio y confirmar que el archivo manual.md contiene todas las líneas editadas.



**Resumen del flujo básico de Git:**



*Acción:	Comando --->	Qué hace*



Preparar cambios: git add --->	Mueve cambios del espacio de trabajo al staging area

Guardar cambios: git commit -m "mensaje" --->  Guarda los cambios del staging area en el repositorio local

Enviar cambios:	git push --->  Sube los commits del repositorio local al remoto



**Es importante hacer varios ejercicios para comprender bien el tema y leer todo el manual para tener una mejor comprensión.**

----
  
# **Ramificaciones de Git o Git Branch**

##### 



###### **¿Qué es?**



La ramificación de git es muy importante al momento de crear nuestros repositorios de los proyectos, generalmente tendremos el Branch **Main**, es recomendable crear ramificaciones para poder trabajar de forma segura y ordenada.



Estas ramificaciones tienen un nombre y un trabajo especifico:



**Main:** Es el Branch principal de nuestro proyecto, donde será publicado todos los cambios de forma correcta y seguras para la disposición de los usuarios

**Develop**: Es el Branch donde programamos todo antes de ser publicado en la Main, aquí podemos agregar cosas nuevas, corregir errores, etc.

**Feature**: Es el Branch donde vamos a añadir cosas nuevas a nuestro código y añadirlo en el Branch de Develop para asegurarnos que todo funcione correctamente antes de ser publicado en la Main

**Hotfix**: Es el Branch donde vamos a corregir los errores o bugs que tenemos en el Branch de Develop, simplemente resolvemos el error y lo integramos en el Branch de Develop



###### **¿Cómo crear un Branch y fusionar?**



Antes de empezar es importante que en nuestro Git bash estemos ubicados en nuestro repositorio local.



Para crear un Branch podemos ejecutar alguno de estos comandos `git checkout -b (Nombre del Branch)` o `git switch -c (Nombre del Branch)`. 



Con esto ya deberíamos de crear nuestro Branch pero es muy importante aprender movernos entre ramas y eliminarlas.



Para movernos entre ramas vamos a aplicar el siguiente comando `git switch (Nombre del Branch)`

Para eliminar una rama vamos a aplicar el siguiente comando `git Branch -d (Nombre del Branch)`

Para la lista de las ramas que tenemos vamos a aplicar el siguiente comando `git branch`.



Para fusionar un Branch con otro debemos guardar cada procedimiento mediante commits o stash y ahi si podemos fusionarlos por ejemplo agregar el contenido de Feature a Develop haremos lo siguiente:



Nos dirigimos al Branch de Develop y aplicamos el siguiente comando `git merge Feature` de esta forma lo que agregue a feature estará en Develop, muy importante recordar que estos nos podría generar conflictos que debamos resolver para que todo funcione correctamente 



