## Arrancamos con la ayuda 👋
### 1- Primero creamos una carpeta en la consola
##### mkdir "mi proyecto"

### 2- Configuramos los usuarios que van acceder
##### PS C:\mi proyecto> git config --global user.name "adrianco79"

### 3- Configuramos el mail
##### git config --global user.email "adrianco79@gmail.com"

### 4- Para decir que en un directorio vamos a trabajar con git realmente
##### PS C:\mi proyecto> git init


Initialized empty Git repository in C:/mi proyecto/.git/

### 5- Cambiamos el nombre de la rama master por main
##### git branch -m main

### 6- Para ver en que estado esta nuestro git
##### git status

### 7 - Prepatar un archivo para sacar una foto 
##### git add .\hellogit.py

### 8- ahora hay que sacar la foto
##### git add commit -m "este es mi primer commit"

### 9- Verificar si sacamos la foto
##### git log
commit e9313bfcfcf42e9b897a6aef45e67debd3741f3f (HEAD -> main)
Author: root <root@DESKTOP-PP9412S>
Date:   Mon Jul 24 15:28:49 2023 -0300

    Este es mi primer commit
### 10 - Para mejorar la vista de log
git log --graph --decorate --all --oneline

### 11 - Puedo hacer un alis de la ultima linea
 git config --global alias.tree "log --graph --decorate --all --oneline"
 y ahora puedo ejecutar mi alias
 git tree

### 12 .gitignore creamos ese archivo y ahi indicamos que no queremos tener en cuenta en el git
 touch .gitignore

### 13- Para ver que cosas voy cambiando respecto de la ultima version sin necesidad de hacer commit
##### git diff

### 14 - Para movernos a un momento cualquiera
ejemplo :  git checkout eaa8e3f

### 15 - Para borrar desde un determinado punto para adelante(ejemplo hice dos commit y no quiero que este mas eso)
##### git reset --heard eaa8e3f
Una vez que ejecutamos esto va a cambiar nuestro HEAD

### 16 - Si me equivoque y borre todo sin querer podria a llegar a recuperar
##### git reflog

### 17- Puedo crear tag generalmente cuando se arman versiones
##### git tag mitag

### 18 - Me puedo mover a un determinado tag
##### git checkout tag/mitag

## AHORA VIENE LA PAPA AGREGAR RAMA

### 19- para agregar una rama ocupamo branch y el nombre de la rama ejemplo:
##### git branch login

### 20 - para cambiarnos de rama
##### git switch login

### 21- Para actualizar los cambios que se fueron haciendo en la rama main ocupo merge
##### git merge main

### 22- Para guardar modificaciones si tenemos que cambiarnos de rama pero no queremos hacer commit
##### git stash

### 23 - Para borrar stash 
##### git stash drop

### 24 - Para eliminar una rama ocupamos
##### git branch -d nombre_rama

### 25 - SUbir el codigo de git a github
Primero creo el repo y de ahi saco esto
##### git remote add origin https://github.com/adrianco24/git.git
##### git branch -M main
##### git push -u origin main

### 26 - si hice modificaciones a mi servidor local y quiero que suban los cambios solo hago ahora
##### git push

Segunramente me va a dar error ocupo el comando
### git fetch (se descarga el historia sin los cambios)
ahi podemos mirar el log y ver que se modifico

### git pull (se descarga el historial con los cambios)


### 27 - Si hice modificaciones en mi servidor github y quiero descargar
PS J:\Mi unidad\GIT\SQL\ACTAS> git config pull.rebase false
PS J:\Mi unidad\GIT\SQL\ACTAS> git merge origin main
merge: origin - not something we can merge
PS J:\Mi unidad\GIT\SQL\ACTAS> git pull origin main

### 28 si hay algun error

git pull origin main --allow-unrelated-histories
