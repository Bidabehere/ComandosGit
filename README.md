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
