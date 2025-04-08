## Descripción
The flag is somewhere on this web application not necessarily on the website. Find it.
Check [this](http://saturn.picoctf.net:56885/) out.
## Pistas

## Solución 1
1. El nombre del reto nos da una pista `robots.txt`
2. Podemos entrar al directorio `robots.txt`
```
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
```
3. Decodificamos el texto desde base 64
```
flag1.txtjs/myfi
js/myfile.txt
²û,²ðzè°¡¡»/u«%z8
```
4. Probamos con la ruta `/js/myfile.txt`
5. Obtenemos la bandera:
`picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}`

## Notas adicionales

## Referencias
