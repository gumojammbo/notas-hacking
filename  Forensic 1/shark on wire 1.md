## Descripción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.

## Pistas
1. Try using a tool like Wireshark
2. What are streams?
## Solución 1
1. Siguiendo el stream de paquetes UDP en wireshark
```
Steam 6: UDP
picoCTF{StaT31355_636f6e6e}
```

## Notas adicionales
Abrir directamente con
```
wireshark <archivo> &
```

## Referencias
