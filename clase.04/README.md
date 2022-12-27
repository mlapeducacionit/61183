# Clase 04

## Ramas (Branches)

![ramas](https://miro.medium.com/max/801/1*DhagidpZutkaCmAZobmzDQ.png)

### Crear una rama

```sh
git branch <nombre-rama>
git branch data-ramas
```

### Listar una rama

```sh
git branch
git branch
```

### Cambiar entre ramas

```sh
git switch <nombre-rama>
git switch data-ramas
```

### Borrar rama

```sh
git branch -d <nombre-de-rama-que-quiero-eliminar>
git branch data-ramas
``` 

### Subir rama local al remoto

```sh
git push -u <alias-del-remoto> <nombre-rama-que-quiero-subir>
git push -u origin dev
```

### Clonar un proyecto

```sh
git clone <url-del-repositorio>
git clone https://github.com/mlapeducacionit/proyecto-cafe.git # Crear una carpeta, que va a tener el nombre del repo
git clone https://github.com/mlapeducacionit/proyecto-cafe.git . # El punto. Le indica al clone que no cree un directorio sino que baje el proyecto en el directorio actual.
```

### Para recuperar la metada del repositorio remoto

```sh
git fetch --all
```