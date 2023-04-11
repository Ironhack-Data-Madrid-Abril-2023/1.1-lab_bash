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

echo hello World
Hello
World


* Crea un directorio nuevo llamado `new_dir`.
 Directorio: C:\Users\cleme


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/04/2023     16:14                new_dir


* Elimina ese directorio.
d-r---        31/03/2023     12:31                Searches
d-r---        07/04/2023      9:44                Videos
-a----        01/04/2023     15:22             14 .bash_history
-a----        31/03/2023     20:31             25 .condarc
-a----        07/04/2023     16:49           8792 exemple 1.ipynb
-a----        07/04/2023     16:52           3861 exercises Ironhack.ipynb
-a----        07/04/2023     11:23              0 untitled
-a----        02/04/2023     19:32            589 Untitled.ipynb
-a----        07/04/2023     11:23              0 untitled.txt
-a----        07/04/2023     12:04           3642 Untitled1.ipynb


* Copia el archivo `sed.txt` dentro de la carpeta lorem a la carpeta lorem-copy. TIP: Puede ser necesario crear la carpeta lorem-copy primero. 
mkdir lorem-copy
Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/04/2023     16:23                lorem-copy
cp sed.txt


* Muestra el contenido del archivo `sed.txt` dentro de la carpeta lorem. 
PS C:\users\cleme\lorem> ls


    Directorio: C:\users\cleme\lorem


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/04/2023     15:18            852 at.txt
-a----        10/04/2023     15:18            448 lorem.txt
-a----        10/04/2023     15:18            873 sed.txt

* Muestra el contenido de los archivos `at.txt` y `lorem.txt` dentro de la carpeta lorem. 
At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum 
deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non
provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga.
Et harum quidem rerum facilis est et expedita distinctio.
Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod
maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus.
Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet
ut et voluptates repudiandae sint et molestiae non recusandae.
Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores
alias consequatur aut perferendis doloribus asperiores repellat
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
PS C:\users\cleme\lorem>


* Visualiza las primeras 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy 
Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, 
totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit,

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
