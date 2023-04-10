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
echo "hello world"

* Crea un directorio nuevo llamado `new_dir`.
mkdir new_dir
* Elimina ese directorio.
rmdir new_dir
* Copia el archivo `sed.txt` dentro de la carpeta lorem a la carpeta lorem-copy. TIP: Puede ser necesario crear la carpeta lorem-copy primero. 
mkdir lorem-copy
cd lorem
ls
cp sed.txt ../lorem-copy
* Muestra el contenido del archivo `sed.txt` dentro de la carpeta lorem. 
cd..(salgo de la carperta lorem)
ls
cd lorem-copy (entro a la carpeta de lorem copy)
ls(compruebo que esta dentro)
* Muestra el contenido de los archivos `at.txt` y `lorem.txt` dentro de la carpeta lorem. 
cd ..(salir de la carpeta lorem-copy)
ls
cd lorem
cat at.txt lorem.txt
* Visualiza las primeras 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy 
head -3 sed.txt
* Añade `Homo homini lupus.` al final de archivo `sed.txt` dentro de la carpeta lorem-copy. 
echo "Homo homini lupus." >> sed.txt
* Visualiza las últimas 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy. Deberías ver ahora `Homo homini lupus.`. 
tail -3 sed.txt
* Encuentra al usuario activo en el sistema.
whoami
* Encuentra dónde estás en tu sistema de ficheros.
pwd
* Lista los archivos que terminan por `.txt` en la carpeta lorem.
cd .. (salir de lorem-copy)
pwd ver mi posicion
find lorem *.txt*
* Cuenta el número de líneas que tiene el archivo `sed.txt` dentro de la carpeta lorem. 
wc -l sed.txt
* Cuenta el número de **archivos** que empiezan por `lorem` que están en este directorio y en directorios internos.
ls -a *lorem* | wc -l
* Cuenta el número de apariciones del string `et` en `at.txt` dentro de la carpeta lorem. 
grep -ow "et" *at.txt* | wc -l
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
