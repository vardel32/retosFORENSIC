# extensions
#picoCTF2019 #FORENSICS 
## Objetivo
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Solución
Nos damos cuenta de que es un archivo te dipo PNG con extension TXT.

```bash
┌──(kali㉿kali)-[~/Downloads/RetosForensic/extensions]
└─$ file flag.txt             
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced

```

Esto tambien se puede saber si se exploran los metadatos del archivo. Al usar el comando xxd se puede mostrar el magic byte del archivo que demuestra que es un PNG.

``` bash
┌──(kali㉿kali)-[~/Downloads/RetosForensic/extensions]
└─$ xxd flag.txt | head
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG........IHDR

```

Se cambia la extensión del archivo a .png y después se puede abrir el archivo.

```bash
┌──(kali㉿kali)-[~/Downloads/RetosForensic/extensions]
└─$ mv flag.txt flag.png

```
## Notas adicionales

## Referencias
- Hex signature: https://en.wikipedia.org/wiki/List_of_file_signatures