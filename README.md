Introducción a Git, Github y Gitflow

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



