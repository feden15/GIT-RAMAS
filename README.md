# GIT RAMAS (Branches)

## Crear un repositorio

```sh
git init
```

## Ver el status de los archivos

```sh
git status
```

## GIT Alias (formas cortas de ejecutar comandos)

```sh
git git config --global alias.st "status --short"
# Acorta "git status" a solo "git st", pero te reduce la información que te tira la terminal
```

```sh
git config --global alias.a "add"
# Acorta "git add" a solo "git a"
```

```sh
git config --global alias.c "commit -m"
# Acorta "git commit" a solo "git c"
```

```sh
git config --global alias.l "log --oneline"
# Acorta "git log --oneline" a solo "git l"
```

## Ver las diferencias entre el Working Directory (WD) y el Local Repo (LR)

```sh
git diff
```

## Ver el contenido de cada commit

```sh
git show <número-hash>
```

## Crear y cambiar una rama

```sh
git branch <nombre-rama> # Crear una rama y nos deja donde estamos (rama original)
git branch feature/ramas # Un ejemmplo de lo anterior
git switch -c <nombre-rama> # Crea una rama y nos mueve a la rama que creamos
```

## Moverse entre ramas

```sh
git switch <nombre-rama> # Me muevo a la rama que nombro
git switch feature/ramas # Un ejemmplo de lo anterior
git switch - # Me muevo entre las últimas dos ramas que estuve
```

## Comparar entre los últimos commits de las ramas

```sh
git diff <nombre-rama> # Comparo la rama actual contra la que le indiqué
```

## Ver las ramas locales y remotas

```sh
git branch -a # Me muestra las ramas locales y remotas
```

## Fusionar una rama al main

```sh
git merge <nombre-rama-que-quiero-fusionar-a-main>
# Estando parado en main, indico el nombre de la rama que quiero traer

# Un ejemplo de lo anterior
git switch main
git merge feature/ramas
```

* Fusion -> Fast-foward -> git hace la fusión automáticamente (no genera commit extra)
* Fusión -> con estrategia -> git hace la fusión automáticamente (genera un commit extra, para solucionar la situación que podría ser un conflicto)
* Fusión -> con conflicto -> git no puede fusionar automáticamente, entonces nos va a pedir ayuda a nosotros

## Abortar la fusión

```sh
git merge --abort
```


## Borrar una rama

```sh
git branch -d <nombre-rama> # Se borra automáticamente, si la rama ya estaba fusionada
git branch -D <nombre-rama> #Confirmo el borrado de la rama, si la rama no estaba fusionada
```