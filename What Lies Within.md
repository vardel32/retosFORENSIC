# What Lies Within
#picoCTF2019 #FORENSICS 
## Objetivo
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?
## Solución
Se va a Steganography Online y se proporciona la imagen.
Bandera ==**picoCTF{h1d1ng_1n_th3_b1t5}**==
Para hacer la decodificación a mano se utiliza zsteg.
```bash
┌──(kali㉿kali)-[~/Downloads/RetosForensic/whatLiesWithin]
└─$ zsteg -a buildings.png | grep picoCTF

b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"

```
_ztseg -a_ implica probar todos lo métodos posibles.

## Notas adicionales
Estenografía trata del estudio y la aplicación de técnicas que permiten ocultar mensajes u objetos dentro de otros, llamados _portadores_ para que no se perciba su existencia. Puede ser aplicado sobre imágenes, audios, etc.
## Referencias
- Estenografía: https://es.wikipedia.org/wiki/Esteganograf%C3%ADa
- zsteg: https://github.com/zed-0xff/zsteg