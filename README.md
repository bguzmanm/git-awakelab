# Comandos de Terminal

## Windows

Comencemos con los comandos más utilizados en Windows®
| Comando | Descripción |
| --- | --- |
| help | muestra el listado de los comandos básicos y su uso |
| cd | nos permite movernos entre carpetas |
| dir | muestra las carpetas y archivos que contiene la carpeta donde estamos |
| systemimfo | muestra información sobre nuestra computadora y sobre el sistema operativo |
| mkdir | permite crear directorios |
| md | crea una carpeta o directorio dentro de una ruta |
| del | permite eliminar archivos |
| copy | permite copiar archivos de un directorio a otro |
| move | permite mover archivos de un directorio a otro |
| type | permite ver el contenido de un archivo |
| cls | limpia la terminal |
| ni | permite crear un archivo |

## Comandos de Terminal MacOS y Linux

Y los comandos más utilizados en MacOS® y Linux
| Comando | Descripción |
| --- | --- |
| pwd | muestra la ruta absoluta del directorio actual |
| ls | Lista los archivos de un directorio |
| cd | nos permite movernos entre carpetas |
| mkdir | permite crear directorios |
| touch | permite crear un archivo en blanco |
| rm | permite eliminar archivos o directorios vacíos |
| cp | permite copiar archivos de un directorio a otro |
| code | permite abrir un archivo o carpeta con VSCode |
| cat | permite ver el contenido de un archivo y para conectar contenidos de archivos |
| more | lista el contenido de un archivo |
| clear | limpia la terminal |

# Git

## Inicialización

Para usar Git son suficientes unos cuantos comandos, por ejemplo, para inicializar git y que el proyecto en el que estemos trabajando empiece a ser rastreado, basta con escribir en la terminal dentro de la carpeta del proyecto que se quiera empezar a rastrear:

```shell
git init
```

Normalmente, este comando se usa una sola vez por proyecto.

Cuando se requiere descargar un proyecto ya existente en algún servidor externo, es posible hacer eso con el comando:

```shell
git clone <ruta_proyecto_en_servidor_git>
```

Finalmente, si se ocupa realizar una sincronización del código local con el código del servidor remoto, se necesita ejecutar el comando:

```shell
git pull origin <rama_remota>
```

El término **origin** normalmente hace referencia a la URL del servidor git remoto; este comando obtiene los últimos cambios de la rama remota (normalmente master o develop) y los mezcla automáticamente con la rama de trabajo actual.

## Agregar cambios

Cuando estamos trabajando cambios en `git`, una vez inicializada la carpeta con `git init`, es importante prepararlos para que se guarden en el historial de cambios.

Para realizar un proceso de preparación se utiliza, dentro de la terminal:

```shell
git add .
```

Esto permite guardar los cambios en un estado de preparación. Es decir, aún nos falta confirmarlos. Sin embargo, si realizas este comando podrás ver los cambios que están por ejecutarse:

```shell
git status
```

## Confirmar cambios

Una vez que tenemos un conjunto de cambios preparados para confirmarse dentro del historial de cambios, lo que haremos es aplicar el siguiente comando:

```shell
git commit -m "MENSAJE"`
```

Es importante establecer el argumento `-m` para poder generar el mensaje involucrado describiendo los cambios que hiciste en doble comillado.

Resumiendo, cada vez que necesites guardar cambios en el historial de cambios del proyecto, deberás utilizar:

- `git add .`
- `git commit -m "mensaje del commit"`

## Ramas (Branches)

En ocasiones, cuando se realizan mezclas entre ramas (`git pull origin <rama_remota> `), es posible encontrarse con diferencias que el sistema de control de versiones no puede resolver automáticamente, por lo que se hace necesario resolverlas manualmente, cuando esto sucede git informa aquellos archivos afectados por un conflicto y se procede a resolver esos conflictos manualmente, validando los cambios locales con los remotos en cada uno de los archivos modificados y mezclando, también manualmente, estos cambios, de tal manera que los archivos afectados queden en una versión estable y validada sin que ningún cambio se pierda, por lo que se requiere a su vez de un `git commit` de la mezcla haciendo uso de `git merge` o `git rebase` para confirmar la resolución de los conflictos.

Para generar una nueva rama en base a alguna rama base, se puede usar:

```shell
git checkout <rama_base>
```

Para moverse y crear una rama en la cual se quiera empezar a trabajar se usa el comando:

```shell
git checkout -b <nombre_nueva_rama>
```

Para fusionar 2 ramas, debes posicionarte en la rama destino de la fusión, y ejecutar el comando merge

```shell
git merge <rama_origen> -m 'MENSAJE'
```

Disfrutalo!
