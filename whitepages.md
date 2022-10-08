# WhitePages
#picoCTF2019 #FORENSICS 
## Objetivo
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/74274b96fe966126a1953c80762af80d/whitepages.txt) is all blank!
## Solución
Existen dos tipos de espacio en blanco en el texto, se pueden interpretar como ceros y unos.
Se hará un script en python para automatizar el asunto.

```python
from pwn import *
file = open('whitepages.txt','rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)
print(data)
```
Bandera = ==**picoCTF{not_all_spaces_are_created_equal_c54f27cd05c2189f8147cc6f5deb2e56}**==
## Notas adicionales
Unicode es un intento de estandarizar el lenguaje en computadoras, UTF-8 son sistemas de codificación para texto.
En UTF-8 hay distintos tipos de espacio en blanco

```bash
┌──(kali㉿kali)-[~]
└─$ python3 -m pip install pwntools
```
PWN Tools es utilizado principalmente para programar xploits.

## Referencias
https://es.wikipedia.org/wiki/Unicode