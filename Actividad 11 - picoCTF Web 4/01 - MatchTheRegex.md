## Descripción
How about trying to match a regular expression

The website is running [here](http://saturn.picoctf.net:49746/).
## Pistas
Access the webpage and try to match the regular expression associated with the text field
## Solución 1
1. Poner la expresión regular que se encontró en el código fuente en la pagina `regexr.com`
```
^p.....F!?
```
2. Basado en la explicación que proporciona, construir una cadena que cumpla con la expresión
`p12345F`
3. Ingresar la cadena en el campo correspondiente y obtener la bandera `picoCTF{succ3ssfully_matchtheregex_8ad436ed}`
## Notas adicionales

## Referencias
https://regexr.com/
