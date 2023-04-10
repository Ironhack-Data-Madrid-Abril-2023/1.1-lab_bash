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

(base) guille@guille-PT1-140C:~/1.1-lab_bash$ echo Hello World
Hello World

* Crea un directorio nuevo llamado `new_dir`.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ mkdir new_dir
(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ ls
at.txt  lorem.txt  new_dir  sed.txt


* Elimina ese directorio.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ rm -r new_dir
(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ ls
at.txt  lorem.txt  sed.txt

* Copia el archivo `sed.txt` dentro de la carpeta lorem a la carpeta lorem-copy. TIP: Puede ser necesario crear la carpeta lorem-copy primero.

(base) guille@guille-PT1-140C:~/1.1-lab_bash$ ls
lorem  lorem-copy  __MACOSX  README.md
(base) guille@guille-PT1-140C:~/1.1-lab_bash$ cd lorem-copy
(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ pwd
/home/guille/1.1-lab_bash/lorem-copy
(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ cd ..
(base) guille@guille-PT1-140C:~/1.1-lab_bash$ cd lorem
(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ cp sed.txt /home/guille/1.1-lab_bash/lorem-copy
(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ cd ..
(base) guille@guille-PT1-140C:~/1.1-lab_bash$ cd lorem-copy
(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ ls
sed.txt

* Muestra el contenido del archivo `sed.txt` dentro de la carpeta lorem.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ cat sed.txt
Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium,
totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit,
sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.
Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit,
sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.
Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam,
nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur,
vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?

* Muestra el contenido de los archivos `at.txt` y `lorem.txt` dentro de la carpeta lorem.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ cd ..
(base) guille@guille-PT1-140C:~/1.1-lab_bash$ ls
lorem  lorem-copy  __MACOSX  README.md
(base) guille@guille-PT1-140C:~/1.1-lab_bash$ cd lorem
(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ cat at.txt lorem.txt
At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum
deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non
provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga.
Et harum quidem rerum facilis est et expedita distinctio.
Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod
maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus.
Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet
ut et voluptates repudiandae sint et molestiae non recusandae.
Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores
alias consequatur aut perferendis doloribus asperiores repellatLorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

* Visualiza las primeras 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ head -3 sed.txt
Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium,
totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit,

* Añade `Homo homini lupus.` al final de archivo `sed.txt` dentro de la carpeta lorem-copy.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ echo 'Homo homini lupus.' >> sed.txt
(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ cat sed.txt
Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium,
totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit,
sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.
Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit,
sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.
Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam,
nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur,
vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?Homo homini lupus.

* Visualiza las últimas 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy. Deberías ver ahora `Homo homini lupus.`.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ tail -3 sed.txt
Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam,
nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur,
vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?Homo homini lupus.

* Encuentra al usuario activo en el sistema.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ whoami
guille

* Encuentra dónde estás en tu sistema de ficheros.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem-copy$ pwd
/home/guille/1.1-lab_bash/lorem-copy

* Lista los archivos que terminan por `.txt` en la carpeta lorem.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ ls *.txt
at.txt  lorem.txt  sed.txt

* Cuenta el número de líneas que tiene el archivo `sed.txt` dentro de la carpeta lorem.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ wc -l sed.txt
8 sed.txt

* Cuenta el número de **archivos** que empiezan por `lorem` que están en este directorio y en directorios internos.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ ls -d *lorem* | wc -l
1

* Cuenta el número de apariciones del string `et` en `at.txt` dentro de la carpeta lorem.

(base) guille@guille-PT1-140C:~/1.1-lab_bash/lorem$ grep -ow 'et' at.txt | wc -l
8

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
