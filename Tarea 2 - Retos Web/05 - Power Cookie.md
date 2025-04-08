## Descripción
Can you get the flag? Go to this [website](http://saturn.picoctf.net:63425/) and see what you can discover.
## Pistas
1. Do you know how to modify cookies?
## Solución 1
1. Interceptando la solicitud GET con burpsuite para obtener la cookie
```
Cookie: isAdmin=0
Upgrade-Insecure-Requests: 1
Priority: u=0, i
```
2. Obtenemos la bandera
`picoCTF{gr4d3_A_c00k13_0d351e23}`
## Notas adicionales

## Referencias
