# Clase 06

Me sirven para marca por las diferentes versiones de mi aplicación. Y marcan un commit. Apunta a ese commit el tag.

## Crear un tag

Esto crea un tag en el último commit en la rama que este.

```sh
git tag hice-un-tag
```

## Otra forma de crear un tag

```sh
git tag -a v1.0.0 -m "Esta versión número 1.0.0" # Crea un tag en el último commit
git tag -a v1.0.0 -m "Esta versión número 1.0.0" <HASH> # Crea un tag en el commit especificado
git tag -a v0.1.0 -m "Esta versión número 0.1.0" 4d04d44 
```

## Ver información sobre el tag

```sh
git show <HASH> #Me muestra información solamente del commit
git show fa48e4e
git show <TAG> # Me muestra información sobre el tag y el commit
git show v1.0.0 
```

## Borrar un tag local.

```sh
git tag -d <TAG>
git tag -d <hice-un-tag>
```

## Borrar un tag remote.

```sh
git push --delete origin <TAG>
git push --delete origin v0.1.0
```

## Punteros

![punteros](imgs/punteros.png)

### Punteros estaticos

* Branches, tags

### Puntero dinamico

* HEAD


## Subir tags

### Subir un tag en especifico.

```sh
git push origin <TAG>
```

### TODO. No recomendado. Porque me sube todos los tags.

```sh
git push --tags # No es buena practica
```

## Trabajar en proyectos Open Source (Pull Request)

1. Hacer un fork del proyecto. Del proyecto del cual quiero contribuir (Me voy copiar en mi cuenta el repo del proyecto original)
2. Me clono el fork desde mi cuenta github
3. Trabajo normalmente. Subo los cambios (A repo propio)
4. Me voy al proyecto original en el apartado Pull Request. Creo un nuevo Pull Request. Algunas veces aparece en mi repo la posibilidad Pull Request.
---
5. Si el repo original sufrió más modificaciones. (Commits). Voy a tener que actualizar mi fork.
6. Voy a la cuenta del proyecto original y me copio la url del repositorio
7. Y agrego en mi repositorio local, la url (el remoto) del proyecto original.

    git remote upstream <URL-repositorio-original>

8. Me traigo los cambios del repositorio original a mi repo local

    git pull upstream <rama-que-quiero-actualizar>

9. Subo a mi repositorio remoto (Fork) las actualizaciones del repo local

    git push origin <rama-a-actualizar>
