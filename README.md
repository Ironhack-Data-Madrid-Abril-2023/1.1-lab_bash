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
echo Hello World
* Crea un directorio nuevo llamado `new_dir`.
mkdir new_dir
* Elimina ese directorio.
rm -r new_dir
* Copia el archivo `sed.txt` dentro de la carpeta lorem a la carpeta lorem-copy. TIP: Puede ser necesario crear la carpeta lorem-copy primero. 
mkdir lorem-copy
cd lorem
cp sed.txt ..\lorem-copy\

* Muestra el contenido de los archivos `at.txt` y `lorem.txt` dentro de la carpeta lorem. 
cd lorem
cat at.txt
cat lorem.txt
* Visualiza las primeras 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy 
cd lorem-copy
gc sed.txt -head 3
* Añade `Homo homini lupus.` al final de archivo `sed.txt` dentro de la carpeta lorem-copy. 
add-Content sed.txt "Homo homini lupus."
* Visualiza las últimas 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy. Deberías ver ahora `Homo homini lupus.`. 
gc sed.txt -head 3
* Encuentra al usuario activo en el sistema.
whoami
* Encuentra dónde estás en tu sistema de ficheros.
pwd
* Lista los archivos que terminan por `.txt` en la carpeta lorem.
Get-ChildItem *.txt
* Cuenta el número de líneas que tiene el archivo `sed.txt` dentro de la carpeta lorem. 
(Get-Content sed.txt).count
* Cuenta el número de **archivos** que empiezan por `lorem` que están en este directorio y en directorios internos.
(Get-ChildItem -Filter lorem*).Count
* Cuenta el número de apariciones del string `et` en `at.txt` dentro de la carpeta lorem. 
(Get-ChildItem at.txt -Recurse -File | Select-String -Pattern "et" -AllMatches).Matches.Count

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
