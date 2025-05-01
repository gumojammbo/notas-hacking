## Descripción
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/9a7436948cc502e9cacf5bc84d2cccb5/Forensics is fun.pptm)
## Pistas

## Solución 1
1. Vemos que se trata de un archivo de powerpoint, por lo que lo desempaquetamos con `unzip`
2. Abrimos el contenido resultante en `code` para buscar la bandera ahi
3. Encontramos un archivo llamado `hidden` usamos `CMD+F` para buscar los espacios en blanco y eliminarlos
4. Obtenemos una cadena codificada `ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ`
5. La decodificamos con `echo ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ | base64 -d`
6. Obtenemos la bandera `flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}`
## Notas adicionales

## Referencias
