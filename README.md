# Comandos de GIT (2023) 🚀

## Establecemos los valores de configuración

Ahora debemos establecer las variables de configuración global, que son muy importantes, especialmente si estás trabajando con otros desarrolladores. La principal ventaja de esto es que es más fácil averiguar quién ha hecho un commit de determinado bloque de código.

git config puede ser usado para establecer una configuración específica de usuario, como el nombre de usuario ,y el email, etc.
#
```
$ git config --global user.name "nombre"          
$ git config --global user.email "correo@correo.com" 
```

Habilitar la útil colorización del producto de la línea de comando.

```
$ git config --global color.ui auto

```
Ver la configuracion.
```
$ git config --list

```
Puedes establecer fácilmente un alias para cada comando mediante git config.
```
$ git config --global alias.ci 'commit'

```
Con este comando haremos que git detecte automaticamente lo que queremos escribir

```
$ git config --global help.autocorrect 1
```

## CREAR REPOSITORIOS

Iniciar un nuevo repositorio

```
$ git init
```

Clonar un repositorio existente, descarga un proyecto y toda su historia de versión

```
$ git clone <https://link-con-nombre-del-repositorio>
```

Agregar archivos a la área de preparación
```
$ git add <nombre-del-archivo>   // Agregar un archivo especifico.
$ git add .                 // Agregar todos los archivos.
```

Deshacer los git add
```
$ git reset .
```

Hacer commit de los cambios con un mensaje que explique los cambios
```
$ git commit -m "mensaje de confirmación"
$ git commit -a -m "saltar el git add" // Con este comando nos saltamos de hacer el git add 
```

Enumera todos los archivos nuevos o modificados que se deben confirmar
```
$ git status -s
```

Muestra las diferencias de archivos que no se han enviado aún al área de espera
```
$ git diff
```

Modificar los git commit
```
$ git commit --amend
```

Deshacer los commit
```
$ git reset --soft HEAD~1   // Borra el ultimo commit y no borra los cambios
$ git reset --hard HEAD~1   // Borra el ultimo commit y si borra los cambios
```

Subir los archivos a un repositorio remoto
```
$ git push origin <nombre-de-la-rama>
```
## RAMAS

Crear una nueva rama
```
$ git branch <nombre-de-la-rama>
```

Crear una rama rama (Segunda opción)
```
$ git checkout -b <nombre-de-la-rama> // Creará la nueva rama y cambiará a ella al instante
```

Visualiza todas las ramas en el repositorio actual
```
$ git branch
$ git branch --list
```

Cambiar a la rama especificada y actualiza el directorio activo
```
$ git checkout <nombre-de-la-rama>
```

Volver a la rama anterior sin necesidad de escribir el nombre
```
$ git switch -
```

Borrar una Rama
```
$ git branch -D <nombre-de-la-rama>
```

Lista los branches con mas información
```
$ git show-branch
```

Combina el historial de la rama especificada con la rama actual
```
$ git merge <nombre-de-la-rama>
```

## REBASE

Se usa para aplicar ciertos cambios de una rama en otra, Une el branch actual con la main
```
$ git rebase
```

Cuando resolvemos los conflictos --continue continua la secuencia del rebase donde se pauso
```
$ git rebase --continue
```

Omite el conflicto y sigue su camino
```
$ git rebase --skip
```

Devuelve todo al principio del rebase
```
$ git rebase --abort
```

Se usa para aplicar ciertos cambios de una rama en otra
```
$ git rebase <nombre-de-la-rama>
```
