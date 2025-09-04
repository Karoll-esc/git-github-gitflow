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





