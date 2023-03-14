markdown
<p float="left">
  <img img style="float: left;"width ="200" height="100" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEji0v55N5TAUIk5h0XzQKtqmlg3kpEx11_6PZqPs4juvDGyXVfcGYIRWozxTAqYACiKkBEpKABjS9Md7t8mYycBDzNC_fXUvQVE8gMw9E0Fr9DstnrFBectnz2uZWr3r_UzxNjZ771ja7l18zeVib3K7DPiHfeTCNz7MRxsAR3FGCPSLcECZod7Tcnc/s320/Logo%20UNAM%20Morelos%20letras.png"/>             
  <img img style="float: right;" width ="60" height="100" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiqqbbUKBPSySIHU3QZIBXVIE0Hm02hAqzlkq7e3_xU_jRRvvvzYBRXKemheQaMYmv5hgPijN-LPMDQoqRX7dPaFSTZ-fQMe9UCbyK3nKiD7Jb__tIAWgcvrGTbZvcqDB-zo2pTp7qILY8-vr2djypOrYabQTaTXEqOzrTLrUJIUazIzPt7Upw6T0ax/s320/Logo%20LCG.png"/> 
</p>
<br>
<br>
<p align="center">  <font size="3">Universidad Nacional Autónoma de México, Campus Morelos</font> <br>
<font size="2"> Licenciatura en Ciencias Genómicas, Semestre 2023-2</font> <br>
<font size="2"> Python, Tarea 2</font> 
<p/>
<div style="text-align: justify">

### Bernardo Chombo Álvarez
  
## Introducción
Para esta tarea se hizo uso de los comandos de git: `git add`, `git log`, `git status`, `git diff`, `git add`, `git cheackout [id]` y `git commit` con la finalidad de añadir el archivo "araB_EColi.fna" y modificar el archivo de "araC_EColi.fna. Asimismo, se restaurará la versión anterior del archivo FASTA de araC y posterior a la comparación de sus versiones.
<br>

El comando `git add` sirve para añadir archivos para su posterior seguimiento de versiones.
<br>

El comando `git log` sirve para visualizar los commits realizados con sus respectivos mensajes.
<br>

El comando `git status` sirve para visualizar si se existen archivos por ser añadidos o por realizarles algún commit.
<br>

El comando `git diff` sirve para comprar dos versiones de un mismo archivo.
<br>

El comando `git cheackout [id]` sirve para restaurar versiones de un archivo proporcionando el id del commit de dicha versión.
<br>

El comando `git commit` sirve para aceptar los cambios realizados en un archivo para asignarlo como una nueva versión. 
<br>

## Metodología o Workflow
1. En el archivo de DNA que ya tienes creado, agrega la secuencia del gene araB en formato Fasta.
2. Sube los cambios a git y confirmalos.
3. Simula que el gene araC ha sufrido 3 mutaciones en su secuencia, cambia 3 nucleótidos.
4. Agrega los cambios a git y confirmalos.
5. Haz las siguientes comparaciones del archivo: última vs penútima y última vs antepenúltima.
6. Restaura la versión del archivo que no tiene las mutaciones.
7. En un reporte en markdown indica lo que hiciste y los comandos que ejecutaste.

## Resultados
1.
``` 
cd .\Desktop\Python_1\projects\reverse-complement\data
cp ..\..\..\..\..\Downloads\araB_EColi.fna .
```
2.
``` 
git add .\araB_EColi.fna
git commit .\araB_EColi.fna
```
3.
``` 
nano araC_EColi.fna
// Se cambiaron los últimos 3 nt de taa a ccg
```
4.
``` 
git add .\araC_EColi.fna
git commit .\araC_EColi.fna
```
5.
``` 
git diff HEAD~1 .\araC_EColi.fna //última vs. penúltima
git diff HEAD~2 .\araC_EColi.fna //última vs. antepenúltima
```
6.
``` 
git log --oneline
git checkout 42e2cab .\araC_EColi.fna
```
Resultado
```
5a.
diff --git a/projects/reverse-complement/data/araC_EColi.fna b/projects/reverse-complement/data/araC_EColi.fna
index acd223e..e3519be 100644
--- a/projects/reverse-complement/data/araC_EColi.fna
+++ b/projects/reverse-complement/data/araC_EColi.fna
@@ -13,4 +13,4 @@ gcacagcatgtttgcttgtcgccgtcgcgtctgtcacatcttttccgccagcagttaggg
 attagcgtcttaagctggcgcgaggaccaacgcattagtcaggcgaagctgcttttgagc
 actacccggatgcctatcgccaccgtcggtcgcaatgttggttttgacgatcaactctat
 ttctcgcgagtatttaaaaaatgcaccggggccagcccgagcgagtttcgtgccggttgt
-gaagaaaaagtgaatgatgtagccgtcaagttgtcataa
+gaagaaaaagtgaatgatgtagccgtcaagttgtcaccg

5b. //última vs. antepenúltima salió exactamente igual porque no había una antepenúltima versión
diff --git a/projects/reverse-complement/data/araC_EColi.fna b/projects/reverse-complement/data/araC_EColi.fna
index acd223e..e3519be 100644
--- a/projects/reverse-complement/data/araC_EColi.fna
+++ b/projects/reverse-complement/data/araC_EColi.fna
@@ -13,4 +13,4 @@ gcacagcatgtttgcttgtcgccgtcgcgtctgtcacatcttttccgccagcagttaggg
 attagcgtcttaagctggcgcgaggaccaacgcattagtcaggcgaagctgcttttgagc
 actacccggatgcctatcgccaccgtcggtcgcaatgttggttttgacgatcaactctat
 ttctcgcgagtatttaaaaaatgcaccggggccagcccgagcgagtttcgtgccggttgt
-gaagaaaaagtgaatgatgtagccgtcaagttgtcataa
+gaagaaaaagtgaatgatgtagccgtcaagttgtcaccg

commit c601008b5a5a1912f1acee4f967433cc6985b28b (HEAD -> master)
Author: Bernardo Chombo Alvarez <bchombo@lcg.unam.mx>
Date:   Wed Mar 1 12:13:21 2023 -0600

    README Tarea2
    
commit 2e35d3802d378aab42d0f979f45e35ba53cd0862 (HEAD -> master)
Author: Bernardo Chombo Alvarez <bchombo@lcg.unam.mx>
Date:   Wed Mar 1 11:50:43 2023 -0600

    araC modificado

commit 92c47876b236bb128679f78a873f576cb45d64b4
Author: Bernardo Chombo Alvarez <bchombo@lcg.unam.mx>
Date:   Wed Mar 1 11:47:15 2023 -0600

    Nuevo archivo de araB EColi
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
        │       araB_EColi.fna
        │       araC_EColi.fna
        │
        ├───doc
        │       README.md
        │       README2.md
        │
        └───src
                reverse-complement.py
```
<br>

## Conclusiones
Se hizo uso práctico de los comandos básicos para el uso de Git con el archivo de ejemplo del gen araC de E. Coli. Se realizó una modificación puntual a la secuencia y además de agregó el archivo FASTA para el gen araB. Posteriormente se practicó con los comandos para la restauración de archivos y se refozó el uso de los comandos indispensables para el buen manejo de git. Finalmente, se volvió a añadir el archivo README.md en el repositorio y se trabajó con el manejo de archivos en Github.  

</div>
