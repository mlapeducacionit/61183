# Clase 05

## RAMAS

### Para crear una rama y moverme a esa rama.

```sh
git switch -c <nombre-de-la-rama>
git switch -c dev
```
### Cambiarme a la rama anterior

```sh
git switch -
```

### TIPO DE MERGE (FUNSIONES)

* Fast-Forward (No hay ningun conflicto. Lo hace automatico) [No Agrega un commit]
* Recursivo (Una unión automatica, no require de ayuda de nosotros) [Agrega un commit al hacer la funsión]
* Manual (Si hay conflicto, que nosotros tenemos que resolver)

#### Abortar la fusión
Si no tengo a la persona que me puede ayudar por ejemplo. Tendría que detener el proceso de merge (fusión)

```sh
git merge --abort
```

## STASH
Trabaja con una estructura de datos de tipo pila. El primero que entra sale último
Permite registrar temporalmente cambios que están en el Working Directory (Area de trabajo) que todavía no están listos para ser un commit.

## Crea el stash

```sh
git stash 
```

## Listo los stashes

```sh
git stash list
```

## Veo en detalle lo que hay dentro del stash

```sh
git stash show -p # Me muestra la info detalla del contenido del último stash
git stash show -p stash@{5} # Me muestra la info detalla del contenido del stash indicado
```

## Comparar con ramas los stashes

```sh
git diff <número-de-stash> <rama>
git diff stash{0} main
```

## Recupero el último stash que tengo en la pila

```sh
git stash pop
```

## Borrar un stash

```sh
git stash drop # Me va borrar el último stash
git stash drop <numero-stash> # Borro un stash en particular
git stash drop stash@{1}
```

## Aplicar un stash diferente si quisiera del último

```sh
git stash apply # Me va aplicar el último stash
git stash apply <numero-stash> # Aplico un stash en particular
git stash apply stash@{1}
```

## Para borrar todos los stashes

```sh
git stash clear
```

## A partir de un stash crear un rama

```sh
git stash branch <nombre-de-ramas>
```

## Buenas practicas para crear mensajes de commits

<https://medium.com/@jmz12/buenas-pr%C3%A1cticas-para-commits-5eb4c86b9a47>

## Para investigar y profundizar sobre los comandos, tengo el man de los diferentes comando

```sh
git <subcomando> --help
git commit --help
git stash --help
git merge --help
git switch --help
```