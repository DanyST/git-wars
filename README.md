# Practica módulo GIT

### ¿Qué comando utilizaste en el paso 11? ¿Por qué?
`git reset --hard HEAD~1` porque nos permite mover la rama que apunta HEAD al commit padre (deshaciendo el último commit), y cambiar el working copy con todos los cambios que tiene el commit anterior.

### ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
`git reflog` para buscar el id del commit que "Deshacimos" y el cual quedó inaccesible.

`git reset --hard 6eb8c15` porque git reset nos permite mover ramas al commit que queramos, y añadiendo el modificador `--hard` a la vez modificamos el working copy con los cambios que tenga ese commit.

### El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No, porque desde que se creó la rama `styled` en base a los cambios de `main`, esta ultima no ha guardado nuevos cambios(`commits`) que modifiquen el archivo git-nuestro.md.

A nivel de grafo, este forma una lista entre `styled` y `main`, y al ejecutar el comando `git merge main` desde `styled`, este no tiene efecto, ya que `styled` tienes todos los commits de `main`, y a la vez los propios de `styled`.

### El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí, porque la rama `htmly` y `styled` tienen cambios en el archivo `git-nuestro.md` en las mismas lineas, por lo que al hacer `git merge htmly` desde `styled`, git no sabe que cambios(los que tienen conflictos) guardar en el commit del merge no fast fordward, y nos deja la decisión a nosotros al resolver los conflictos.

### El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No, porque la rama `styled` tiene acceso a todos los commits de `main`, por lo que esta ultima no añadió nuevos commits desde que se creó `styled`, dando como resultado un merge fast forward, ya que el grafo de git es un listado entre las dos ramas.

### ¿Qué comando o comandos utilizaste en el paso 25?
`git log --graph --oneline --branches`

### El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Si, porque en el grafo de git, los nodos de commits son lineales entre el puntero de rama `main` y `title`, es decir, no hay commits que puedan quedar inaccesibles si movemos el puntero de rama `main` hacia `title`, por lo que no es obligación que el merge sea *no fast fordward*.

### ¿Qué comando o comandos utilizaste en el paso 27?
`git reset HEAD~1`

### ¿Qué comando o comandos utilizaste en el paso 28?
`git restore git-nuestro.md`

### ¿Qué comando o comandos utilizaste en el paso 29?
`git branch -D title`

### ¿Qué comando o comandos utilizaste en el paso 30?
`git reflog`

`git reset --hard 3ba6af8`

### ¿Qué comando o comandos usaste en el paso 32?
`git log --oneline --graph`

`git reset --hard da0559c`

### ¿Qué comando o comandos usaste en el punto 33?
`git reflog`

`git reset --hard 3ba6af8`
