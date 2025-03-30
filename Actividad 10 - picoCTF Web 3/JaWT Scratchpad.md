## Descripción

> [!DANGER]
>Internal server errors can be intentionally returned by this challenge. If you experience one, try clearing your cookies.

Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210
## Pistas
1. What is that cookie?
2. Have you heard of JWT?
## Solución 1
1. Probamos loguearnos con la palabra admin
2. Probamos con otro nombre y revisamos las cookies
	`eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoibmRhaGFpIn0.xiN4wjjuHokvxsEosoFWBrDhJZRhzveSGJKZmWS5qUc`
 3. Decodificamos la cookie con [jwt.io]() 
 ```
 {
  "user": "ndahai"
}
```
 4. Cambiamos el user por admin y cambiamos la cookie
 5. Vemos que se necesita una firma, por lo que usamos **John** para crackearla, guardando la cookie en un archivo y usando el wordlist ubicado en `/usr/share/wordlists/rockyou.txt.gz`
 ```bash
 john hash -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 128/128 ASIMD 4x])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:02 DONE (2025-03-29 23:55) 0.4901g/s 3626Kp/s 3626Kc/s 3626KC/s iloverob4live345..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably
Session completed. picoCTF{jawt_was_just_what_you_thought_44c752f5}

```
6. Vemos que la contrasena es `ilovepico`
7. La ingresamos en jwt.io, junto con el user "admin".
8. `picoCTF{jawt_was_just_what_you_thought_44c752f5}`
``
## Notas adicionales

## Referencias