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
```