## Descripción
Can you login to this website?

## Pistas
`admin` is the user you want to login as.
## Solución 1
1. El sitio nos revela la consulta SQL que se usa para el LOGIN
2. Haciendo SQL Injection con los siguientes datos
```
user: 1' OR '1' == '1';--
password:123
```
3. El sitio nos indica que nos logueamos exitosamente, pero no esta la bandera, por lo que vemos el codigo fuente de la pagina
4. Obtenemos la bandera `picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}`
## Notas adicionales

## Referencias
