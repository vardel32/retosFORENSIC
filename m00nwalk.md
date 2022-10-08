# m00nwalk
#picoCTF2019 #FORENSICS 
## Objetivo
Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.
## Solución
Se utiliza sstv después de copiar el repositorio e instalarlo.
```bash
┌──(kali㉿kali)-[~/Downloads/RetosForensic/m00nwalk]
└─$ sstv -d message.wav -o result.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [###############################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!

```
![[Pasted image 20220929101345.png]]
## Notas adicionales

El Apollo11 enviaba imágenes en forma de audios a la tierra, llegando aqui eran decodificados estos audios en imágenes.
## Referencias
