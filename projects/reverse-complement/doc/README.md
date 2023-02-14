markdown
<p float="left">
  <img img style="float: left;"width ="200" height="100" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEji0v55N5TAUIk5h0XzQKtqmlg3kpEx11_6PZqPs4juvDGyXVfcGYIRWozxTAqYACiKkBEpKABjS9Md7t8mYycBDzNC_fXUvQVE8gMw9E0Fr9DstnrFBectnz2uZWr3r_UzxNjZ771ja7l18zeVib3K7DPiHfeTCNz7MRxsAR3FGCPSLcECZod7Tcnc/s320/Logo%20UNAM%20Morelos%20letras.png"/>             
  <img img style="float: right;" width ="60" height="100" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiqqbbUKBPSySIHU3QZIBXVIE0Hm02hAqzlkq7e3_xU_jRRvvvzYBRXKemheQaMYmv5hgPijN-LPMDQoqRX7dPaFSTZ-fQMe9UCbyK3nKiD7Jb__tIAWgcvrGTbZvcqDB-zo2pTp7qILY8-vr2djypOrYabQTaTXEqOzrTLrUJIUazIzPt7Upw6T0ax/s320/Logo%20LCG.png"/> 
</p>
<br>
<br>
<p align="center">  <font size="3">Universidad Nacional Autónoma de México, Campus Morelos</font> <br>
<font size="2"> Licenciatura en Ciencias Genómicas, Semestre 2023-2</font> <br>
<font size="2"> Python, Tarea 1</font> 
<p/>
<div style="text-align: justify">

### Bernardo Chombo Álvarez
## Introducción
Para esta tarea se hizo uso de los comandos de git: `git add` y `git commit` con la finalidad de hacer un seguimiento de los cambios en el nuevo archivo ingresado "araC_EColi.fna.
<br>

El comando `git add` sirve para añadir archivos para su posterior seguimiento de versiones.
<br>

El comando `git commit` sirve para aceptar los cambios realizados en un archivo para asignarlo como una nueva versión. 
<br>

## Metodología
1. Descargar el archivo FASTA en la computadora y realizar un cp a la carpeta
2. Ejecutar el comando `git add` y el nombre del archivo.
3. Ejecutar el comando `git commit` y el nombre del archivo para aceptar que se llevaron a cabo cambios y que se le haga un segumiento y su versión al archivo.
4. ejecutar el comando `git status` para checar que el archivo efectivamente ya se ha recibido como una nueva versión del mismo.
5. Ejecutar el comando `git log` para comprobar nuevamente que la versión del arhcivo haya quedado guardada.

## Resultados
1.
``` 
cd .\Desktop\Python_1\projects\reverse-complement\data
cp ..\..\..\..\..\..\..\Downloads\Documents\araC_EColi.fna .
```
2.
``` 
git add .\araC_EColi.fna
```
3.
``` 
git commit .\araC_EColi.fna
```
4.
``` 
git status
```
5.
``` 
git log
```
Resultado
```
commit 42e2cab7fc74377c27399c0d4f450732d60793a9 (HEAD -> master)
Author: Bernardo Chombo Alvarez <bchombo@lcg.unam.mx>
Date:   Tue Feb 14 15:56:40 2023 -0600

    Nuevo archivo de araC EColi
```
<br>

### Estructura
```
C:.
├───lessons
│       notas.md
│
└───projects
    ├───at_content
    │   ├───doc
    │   │   └───img
    │   ├───lib
    │   └───src
    └───reverse-complement
        ├───data
        │       araC_EColi.fna
        │       sequence.txt
        │
        ├───doc
        │       README.md
        │
        └───src
                reverse-complement.py
```
<br>

## Conclusiones
Se hizo uso práctico de los comandos básicos para el uso de Git con el archivo de ejemplo del gen araC de E. Coli. Se realizó un uso correcto de los comandos y se verificó con comandos adicionales que la versión de dicho archivo sí se haya realizado de form óptima. Es indispensable el buen manejo de este tipo de comandos para hacer un *tracking* de las modificaciones en los archivos con los que se esté trabajando. 

</div>
