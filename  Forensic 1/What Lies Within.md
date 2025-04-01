## Descripción
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?

## Pistas
1. There is data encoded somewhere... there might be an online decoder.
## Solución 1

1. Usamos `zsteg` para buscar LSB escondidos en archivos
```bash
zsteg -a buildings.png
```
2. Obtenemos la bandera
`picoCTF{h1d1ng_1n_th3_b1t5}`
## Notas adicionales
Steganography - Esconder informacion en los bits menos significativos

## Referencias
