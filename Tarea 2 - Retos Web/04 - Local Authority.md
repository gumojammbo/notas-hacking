## Descripción
Can you get the flag? Go to this [website](http://saturn.picoctf.net:58874/) and see what you can discover.

## Pistas
1. How is the password checked on this website?

## Solución 1
1. Accediendo con cualquier contrasena
2. Inspeccionamos la pagina
3. Vemos que en el HTML hay una funcion para checar la contrasena
4. Vemos que el archivo secure.js contiene la contrasena
```
admin
strongPassword098765
```
5. Probando la contrasena, nos da la bandera
`picoCTF{j5_15_7r4n5p4r3n7_a8788e61}`

## Notas adicionales

## Referencias
