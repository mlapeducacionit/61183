# Clase 02

## Estado de los archivos

* untracked

* unmodified

* modified

* staged

## GIT LOG
Me muestra las fotos que les fui sacando al proyecto que están dentro del LOCAL REPO

```sh
git log 
```

> GIT LOG versión corta

```sh
git log --oneline
```

## GIT DIFF
Me sirve para visualizar los cambios que hay entre el WD (working directory) y la última foto (Commit) dentro de la caja de commits (Local Repo)

```sh
git diff
```

## GIT AMMEND
Me permite agregar cambios al último commit. Sean líneas de código o archivos completo

Coloco en el area temporal (Stage area) los cambios que quiero sumar en el último commit. Sean líneas que faltaron, archivos que faltaron. Y luego hago el amend

```sh
git add .
git commit --amend
```
El git commit suele abrir un editor de texto (Nano) para colocar el mensaje o editar el actual mensaje

* Ctrl + O: Guardar
* Ctrl + X: Salir




