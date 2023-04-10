# Bash Lab

## Intro

Vamos a practicar con `bash`, un lenguaje de programación que se ejecuta en la línea de comandos!


## Entregable

Abre el  jupyter notebook en esta carpeta llamado solutions.ipynb y ve escribiendo en él los títulos de los ejercicios en una celda, y en otra el comando que has utilizado para solucionar los ejercicios. 

## Setup

1. Ubícate en la carpeta en la que ejecutando en el terminal. Al ejecutar `ls` 
```console
$ ls
```

2. Deberías ver: 
```console
README.md lorem solutions.ipynb
```
3. Intenta hacer todos los ejercicios sin cambiar de directorio. 

## Ejercicios

* Imprime en consola `Hello World`.

* Crea un directorio nuevo llamado `new_dir`.

* Elimina ese directorio.

* Copia el archivo `sed.txt` dentro de la carpeta lorem a la carpeta lorem-copy. TIP: Puede ser necesario crear la carpeta lorem-copy primero. 

* Muestra el contenido del archivo `sed.txt` dentro de la carpeta lorem. 

* Muestra el contenido de los archivos `at.txt` y `lorem.txt` dentro de la carpeta lorem. 

* Visualiza las primeras 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy 

* Añade `Homo homini lupus.` al final de archivo `sed.txt` dentro de la carpeta lorem-copy. 

* Visualiza las últimas 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy. Deberías ver ahora `Homo homini lupus.`. 

* Encuentra al usuario activo en el sistema.

* Encuentra dónde estás en tu sistema de ficheros.

* Lista los archivos que terminan por `.txt` en la carpeta lorem.

* Cuenta el número de líneas que tiene el archivo `sed.txt` dentro de la carpeta lorem. 

* Cuenta el número de **archivos** que empiezan por `lorem` que están en este directorio y en directorios internos.

* Cuenta el número de apariciones del string `et` en `at.txt` dentro de la carpeta lorem. 

## Ficheros bash

Cualquier comando o comandos de bash se pueden almacenar en un fichero y ejecutar cuando queramos. 
Obviamente puedes utilizar tu editor preferido. Creamos el fichero: 
```
$ touch list_files.sh
```

E incluimos el contenido que queramos. En este caso listar ficheros:
```bash
#!/bin/bash
ls
```

Ejecutamos el script:
```
$ bash list_files.sh
```

Y veremos por consola el siguiente output. 
```console
README.md lorem solutions.ipynb
```
Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit,
sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.
Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit,
sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.
Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam,
nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur,
vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?(base) MacBook-Pro-de-Jose:lorem joseluisreguera$
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ cd ..
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ cat at.txt
cat: at.txt: No such file or directory
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ cd lorem
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ cat at.txt
At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum
deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non
provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga.
Et harum quidem rerum facilis est et expedita distinctio.
Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod
maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus.
Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet
ut et voluptates repudiandae sint et molestiae non recusandae.
Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores
alias consequatur aut perferendis doloribus asperiores repellat(base) MacBook-Pro-de-Jose:lorem joseluisreguera$
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ cat lorem.txt
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ pwd
/Users/joseluisreguera/desktop/ironhack/lorem
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ head -n 3 lorem-copy/sed.txt
head: lorem-copy/sed.txt: No such file or directory
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ pwd
/Users/joseluisreguera/desktop/ironhack/lorem
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ cd ironhack
-bash: cd: ironhack: No such file or directory
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ pwd
/Users/joseluisreguera/desktop/ironhack/lorem
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ cd desktop
-bash: cd: desktop: No such file or directory
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ ld
ld: warning: platform not specified
ld: warning: -arch not specified
ld: warning: No platform min-version specified on command line
ld: no object files specified
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ cd ..
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ cd lorem copy
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ head -n 3 lorem-copy/sed.txt
head: lorem-copy/sed.txt: No such file or directory
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ cd ..
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ cd lorem copy
(base) MacBook-Pro-de-Jose:lorem joseluisreguera$ cd ..
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ head -n 3 lorem-copy/sed.txt
Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium,
totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit,
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ whoami
joseluisreguera
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ pwd
/Users/joseluisreguera/desktop/ironhack
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ ls lorem/*.txt
lorem/at.txt    lorem/lorem.txt    lorem/sed.txt
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ wc -l lorem/sed.txt
       9 lorem/sed.txt
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ find . -name "lorem*" | wc -l
       4
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ grep -o 'et' lorem/at.txt | wc -l
      10
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ cd ..
(base) MacBook-Pro-de-Jose:desktop joseluisreguera$ cd ironhack
(base) MacBook-Pro-de-Jose:ironhack joseluisreguera$ cd 1.1-lab_bash
(base) MacBook-Pro-de-Jose:1.1-lab_bash joseluisreguera$ git add me.
fatal: pathspec 'me.' did not match any files
(base) MacBook-Pro-de-Jose:1.1-lab_bash joseluisreguera$ git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
    add
(base) MacBook-Pro-de-Jose:1.1-lab_bash joseluisreguera$ git add .
(base) MacBook-Pro-de-Jose:1.1-lab_bash joseluisreguera$ git commit -m "read me con soluciones"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
(base) MacBook-Pro-de-Jose:1.1-lab_bash joseluisreguera$ git push
Everything up-to-date
(base) MacBook-Pro-de-Jose:1.1-lab_bash joseluisreguera$
