Introducción a Git, Github y Gitflow



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

