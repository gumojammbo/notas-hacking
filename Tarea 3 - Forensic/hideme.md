## Descripción
Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/259/flag.png).
## Pistas
1. In the country that doesn't exist, the flag persists
## Solución 1
1. Usando el comando `strings` en la imagen nos percatamos de que hay una ruta dentro
```bash
strings flag.png

secret/UT
pVgE#
secret/flag.pngUT
```
2. Usando `unzip` descomprimimos lo que hay dentro 
```bash
unzip flag.png      
Archive:  flag.png
warning [flag.png]:  39739 extra bytes at beginning or within zipfile
  (attempting to process anyway)
   creating: secret/
  inflating: secret/flag.png
```
3. Abrimos la imagen resultante y obtenemos la bandera `picoCTF{Hiddinng_An_imag3_within_@n_ima9e_cda72af0}}`
## Notas adicionales


## Referencias
