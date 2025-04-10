## Descripción
Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.
## Pistas
1. How did pictures from the moon landing get sent back to Earth?
2. What is the CMU mascot?, that might help select a RX option

## Solución 1
1. Usando la pista 1, vemos que esas fotos fueron enviadas usando SSTV
2. SSTV usa audio para codificar imagenes
3. Nuestro archivo es un audio por lo que usamos SSTV Decoder
4. Usando el comando para decodificar, que detecta automaticamente la codificacion usada
```bash
sstv -d message.wav -o result.png
```
5. Vemos que la imagen resultado tiene la bandera
`picoCTF{beep_boop_im_in_space}`
## Notas adicionales


## Referencias
https://en.wikipedia.org/wiki/Apollo_11_missing_tapes
https://github.com/colaclanth/sstv