## Descripción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
## Pistas
## Solución 1
1. Vemos que la mayor parte del trafico es UDP, por lo que filtramos
2. Al seguir el stream nos damos cuenta que en el no. 32 hay una marca de start, que llega hasta el 60, vemos que ambos tienen como destino el puerto 22
3. Filtramos por paquetes que tengan como destino dicho puerto
4. Vemos que los puertos de salida empiezan en 5000, pero que van cambiando y los primeros corresponden con los valores ASCII de `pico`, por lo que asumimos que el resto de la bandera se encuentra en el puerto de salida - 5000 en ASCII
5. Con un script de python...
```python
from scapy.all import *

packets = rdpcap('capture.pcap')

flag = ''

for p in packets:
        if UDP in p and p[UDP].dport == 22:
                if p[UDP].sport > 5000:
                        flag += chr(p[UDP].sport - 5000)
print(flag)

```
6. 
```bash
python3 exp.py    
picoCTF{p1LLf3r3d_data_v1a_st3g0}
```

## Notas adicionales

## Referencias
