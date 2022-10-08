# Glory of the Garden
#picoCTF2019 #FORENSICS
## Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.
## Solución
Se descarga el archivo.

```bash
┌──(kali㉿kali)-[~/Downloads/RetosForensic]
└─$ wget https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg
```
El editor hexadecimal de Linux es el comando _xxd_.
Hay un offset que es increíblemente, hay ocho columnas de 2 bytes cada uno.
hexeditor es un programa que trae kali linux.
Se puede hacer busqueda en hexeditor mediante ctrl+W.

```bash
┌──(kali㉿kali)-[~/Downloads/RetosForensic]
└─$ strings -n 15 garden.jpg | grep pico
Here is a flag "picoCTF{more_than_m33ts_the_3y3657BaB2C}"

```
## Notas adicionales
Un editor hexadecimal es un tipo de programa que permite modificar archivos binarios.
## Referencias
- Editor hexadecimal: https://es.wikipedia.org/wiki/Editor_hexadecimal