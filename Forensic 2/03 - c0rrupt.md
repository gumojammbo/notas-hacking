## Descripción
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Pistas
Try fixing the file header
## Solución 1
1. La cabecera del archivo nos sugiere que se trata de un png
```
00000000: 8965 4e34 0d0a b0aa 0000 000d 4322 4452  .eN4........C"DR
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...
00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I
00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?
00000060: 8e64 cd71 bd2d 8b20 2080 9041 8302 08d0  .d.q.-.  ..A....
00000070: f9ed 40a0 f36e 407b 9023 8f1e d720 8b3e  ..@..n@{.#... .>
00000080: b7c1 0d70 0374 b503 ae41 6bf8 bea8 fbdc  ...p.t...Ak.....
00000090: 3e7d 2a22 336f de5b 55dd 3d3d f920 9188  >}*"3o.[U.==. ..
```

2. Vemos que la cabecera no corresponde, por lo que corregimos
`89 50 4E 47  0D 0A 1A 0A`
3. Verificando el archivo aun no puede ser leido, por lo que seguimos corrigiendo, ahora el segmento IHDR
`49 48 44 52`
4. Ahora ya lo reconoce, pero sigue sin ser visible
5. Usando PNGCheck
```
pngcheck mystery 
mystery  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERROR: mystery

```
6. Corregimos el valor alto `59 73 00 00`
7. Volvemos a comprobar
```
mystery  invalid chunk length (too large)
ERROR: mystery
```
7. Corregimos el nombre del chunk `AA FF A5 49   44 41 54 78` IDAT
8. Comprobamos
```
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery
```
9. Corregimos la longitud `52 24 F0 00  00 FF A5 49   44 41 54 78  5E EC BD 3F` IDAT
10. Comprobamos
```
No errors detected in mystery (9 chunks, 96.3% compression).
```
11. El archivo abre correctamente y nos arroja la bandera
`picoCTF{c0rrupt10n_1847995}`
## Notas adicionales

## Referencias
https://es.wikipedia.org/wiki/Portable_Network_Graphics