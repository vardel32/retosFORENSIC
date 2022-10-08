# shark on wire 1
#picoCTF2019 #FORENSICS 
## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
## Solución
Se abre el paquete de captura de datos mediante wireshark, se selecciona un paquete con protocolo UDP y se sigue la corriente del paquete hasta encontrar la bandera, se encuentra en el stream 6.
Bandera ==**picoCTF{StaT31355_636f6e6e}**==
## Notas adicionales
Para capturar paquete se utiliza un snifer o analizador de paquetes.
wireshark en el caso de Linux.

## Referencias
- Modelo OSI: https://es.wikipedia.org/wiki/Modelo_OSI