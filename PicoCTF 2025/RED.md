## Descripción
RED, RED, RED, REDDownload the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)
## Pistas
The picture seems pure, but is it though?
Red?Ged?Bed?Aed?
Check whatever Facebook is called now.
## Solución 1
Revisando la imagen con nano se observa el siguiente poema
```php
Crimson heart, vibrant and bold,

Hearts flutter at your sight.

Evenings glow softly red,

Cherries burst with sweet life.

Kisses linger with your warmth.

Love deep as merlot.

Scarlet leaves falling softly,

Bold in every stroke.
```

Al juntar las primeras letras de cada verso se obtiene
```
CHECK LSB
```

Usando la herramienta pyLSB se obtiene 

```
cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==
```

Luego usando CyberChef:

```
Input: cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==

Recipe: From Base64

Output: picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}
```

## Notas adicionales


## Referencias
https://medium.com/@renantkn/lsb-steganography-hiding-a-message-in-the-pixels-of-an-image-4722a8567046                 
