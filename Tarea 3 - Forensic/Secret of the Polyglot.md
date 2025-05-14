## Descripción
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?

Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/7/flag2of2-final.pdf).

## Pistas
1. This problem can be solved by just opening the file in different ways
## Solución 1
1. En el PDF vemos que hay un pedazo de bandera cortada
2. Usando strings vemos si podemos ver el resto, pero observamos una cadena que sugiere que hay una imagen dentro
```
IHDR
iCCPICC profile
byY%>'
\W<~
C`$G
        pHYs
tIME
tEXtComment
Created with GIMPW

```
3. Usando convert, convertimos el pdf a una imagen `convert flag2of2-final.pdf png`
4. Abrimos la imagen y vemos el resto de la bandera
`picoCTF{f1u3n7_1n_pn9_&_pdf_53b741d6}`


## Notas adicionales


## Referencias
