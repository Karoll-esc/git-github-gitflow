# Introducción a Git, Github y Gitflow

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

---
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

----
  
# **5: ¿Qué es un conflicto en Git?**

Un conflicto ocurre cuando dos ramas modifican la misma parte de un archivo y Git no puede decidir automáticamente qué versión conservar.

Ejemplo:
Tú trabajas en la rama feature.
Otro compañero trabaja en la rama develop.
Ambos cambian la misma línea en README.md.

Cuando intentas hacer ´git merge´, Git detecta que las modificaciones son incompatibles y genera un ¡conflicto! 

## **¿Cuándo se generan conflictos?**

Durante un merge: Cuando unes dos ramas con cambios en la misma línea de un archivo.
Ejemplo: git merge feature dentro de develop.

Durante un rebase: Cuando Git intenta “recolocar” commits encima de otros commits que tienen cambios en las mismas líneas.

Durante un stash pop: Si guardaste cambios con git stash y luego los aplicas en un archivo que ya fue modificado.

## **Cómo detectar un conflicto?**

Cuando ocurre, Git te avisa:
//CONFLICT (content): Merge conflict in README.md//
//Automatic merge failed; fix conflicts and then commit the result.//


## **¿Cómo se resuelven los conflictos?**

Abrir el archivo en conflicto
Verás el error delimitado por <<<<<======>>>>>

Editar manualmente y elige una de las dos versiones o combina lo mejor de ambas. 

por ultimo: Borra las marcas <<<<<<<, =======, >>>>>>>.

y realiza un git commit -c "Especificando que hiciste un cambio"

En el trabajo colaborativo con Git, los conflictos son inevitables cuando varios desarrolladores modifican las mismas partes de un archivo; en esos casos se deben resolver manualmente para decidir qué cambios conservar. Por otro lado, comandos como git stash ayudan a evitar complicaciones al permitir guardar temporalmente los cambios sin necesidad de hacer un commit, lo que resulta muy útil si surge un conflicto o se necesita cambiar de rama rápidamente.

# **¿Qué es git stash?**

Es un comando que te permite guardar temporalmente los cambios de tu área de trabajo (working directory y staging) sin necesidad de hacer un commit.
Se guarda en una "pila" (stash stack).
Luego puedes aplicar esos cambios cuando quieras.
En pocas palabras: sirve para pausar lo que estás haciendo y dejar tu carpeta limpia, sin perder el trabajo.

## **¿Cuándo usar git stash?**

Cuando tienes cambios a medio hacer y necesitas cambiar de rama rápido
Ejemplo: estás programando en feature/users-crud, pero te dicen que arregles un bug urgente en hotfix/resolve-bugs.

Haces:
git stash
git checkout hotfix/resolve-bugs

Solucionas el bug, haces commit y push.

Regresas a tu rama y recuperas tu trabajo:
git checkout feature/users-crud
git stash pop

Cuando quieres probar algo sin arruinar tu área de trabajo
Puedes guardar tu avance, hacer pruebas, y luego recuperar tu trabajo original.


Manual de Buenas Prácticas en Git y GitHub

Este manual tiene como objetivo unificar el trabajo en equipo, mantener la organización del código y facilitar la colaboración en proyectos.

1. Configuración inicial
Configura tu usuario y correo:
git config --global user.name "Tu Nombre"
git config --global user.email "tu_correo@example.com"
Usa una clave SSH o un token personal para conectarte a GitHub de forma segura.

 2. Flujo de trabajo recomendado
Crear una rama (branch) para cada tarea/funcionalidad:
git checkout -b feature/nueva-funcionalidad
Realizar commits pequeños y frecuentes.
      Usa mensajes claros:
git commit -m "fix: corrige error en login"
git commit -m "feat: agrega validación de correo"
Actualizar tu rama antes de hacer merge:
git pull origin develop
Hacer Pull Request (PR) para revisión antes de integrar cambios.

 3. Nombres y ramas
main/master → Rama principal, siempre estable.
develop → Rama de desarrollo.
feature/ → Funcionalidades nuevas.
hotfix/ → Corrección rápida en producción.
Ejemplo:
feature/agregar-login
hotfix/correccion-bug-404

 4. Buenas prácticas de commits
Usa verbos en infinitivo: add, update, fix, remove.
Un commit debe reflejar un cambio lógico completo, no varios temas mezclados.
Evita mensajes genéricos como "arreglos" o "cambios".

5. Pull Requests
Antes de abrir un PR:
Verifica que el código compile y pase pruebas.
Revisa que no existan archivos innecesarios (ejemplo: temporales, env).
Asigna revisores y explica brevemente el cambio en la descripción.

 6. Archivos a ignorar
Usa .gitignore para evitar subir:
Archivos temporales del editor (ej: .vscode/, .idea/).
Dependencias (node_modules/, vendor/).
Credenciales o configuraciones locales (.env).

 7. Comunicación y colaboración
Sincroniza cambios con frecuencia:
git pull origin develop
Documenta lo necesario en el README del proyecto.
Pregunta antes de hacer cambios grandes que afecten a todo el equipo.

Siguiendo estas prácticas lograremos un proyecto organizado, seguro y fácil de mantener.


