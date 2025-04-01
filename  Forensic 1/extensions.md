## Descripción
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? 
Can you find the flag?

## Pistas
1. How do operating systems know what kind of file it is? (It's not just the ending!
2. Make sure to submit the flag as picoCTF{XXXXX}
## Solución 1

1. Comprobar el tipo de archivo con file
```bash
file flag.txt

flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced

```
2. Le cambiamos la extension al archivo y lo abrimos
```bash
mv flag.txt flag.png
```
3. Obtenemos la bandera
`picoCTF{now_you_know_about_extensions}`
## Notas adicionales

## Referencias
