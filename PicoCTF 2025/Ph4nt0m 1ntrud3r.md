## Descripción
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/a917f567b9cc0f1a730a7801b309955df4d2234a8114326857b9759e9e5d0453/myNetworkTraffic.pcap) and try to get the flag.
## Pistas
Filter your packets to narrow down your search.
Attacks were done in timely manner.
Time is essential
## Solución 1
Usando la herramienta WireShark y cargando el archivo proporcionado ordenando los paquetes por tiempo.

Copiando los caracteres ASCII en los paquetes...
```php
ePRXDio=
dgV9v0s
nfu4Vww
XThGxuE=
CJr4oDk=
TOGSGg4=
ckBkZLK=
YQEFzIU=
3psv5C4
a23/UbI=
BgJLB0c=
Yt8ksMM=
fjIzQwk=
bpzQ0R8=
J4auZMY=
cGljb0NURg==
ezF0X3c0cw==
bnRfdGg0dA==
XzM0c3lfdA==
YmhfNHJfOQ==
NTlmNTBkMw==
fQ==
```

Usando CodeChef para decodificar desde base64...
(Solo los paquetes despues de cGljb0NURg== generaron una secuencia valida)
```
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_959f50d3}
```
## Notas adicionales


## Referencias
https://serverfault.com/questions/38626/how-can-i-read-pcap-files-in-a-friendly-format

0000   45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010   c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020   50 02 20 00 eb 52 00 00 62 6e 52 66 64 47 67 30   P. ..R..bnRfdGg0
0030   64 41 3d 3d                                       dA==
