## Descripción
We found this [file](https://mercury.picoctf.net/static/21c07c9dd20cd9f2459a0ae75d99af6e/tunn3l_v1s10n). Recover the flag.
## Pistas
1. Weird that it won't display right...

## Solución 1
1. Al abrir la imagen se trata de un archivo BMP
2. Usando un editor hexadecimal vemos que la firma corresponde a un archivo `.BMP`.
3. La firma correspondiente a un BMP creado en windows es `BM` y tiene una longitud de 40 bytes, la cual se especifica en el offset `0E`, vemos que el valor no corresponde, por lo que lo modificamos `00 00 BA D0 -> 00 00 28 00`
4. Al intentar abrirlo, vemos que aun no es posible, el offset que indica donde empiezan los datos `0A` es incorrecto, por lo que especificamos el 28 nuevamente `00 00 BA D0 -> 00 00 28 00`
5. Al abrir el archivo vemos que no tiene la bandera, revisamos los metadatos, el peso es muy alto para el tamano
6. El alto de la imagen esta en el offset `16`, sustituimos el valor por uno mas alto `00 00 30 01 -> 00 00 FF 01` , 
7. Obtenemos la bandera `picoCTF{qu1t3_a_v13w_2020}`

## Notas adicionales

## Referencias
1. https://en.wikipedia.org/wiki/List_of_file_signatures
2. https://en.wikipedia.org/wiki/BMP_file_format/