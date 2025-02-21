## Descripción
Using a Secure Shell (SSH) is going to be pretty important.

Additional details will be available after launching your challenge instance.
## Pistas
[https://linux.die.net/man/1/ssh](https://linux.die.net/man/1/ssh)

You can try logging in 'as' someone with `<user>`@titan.picoctf.net

How could you specify the port?

Remember, passwords are hidden when typed into the shell
## Solución 1
Usando el comando `ssh` y el argumento `-p` para especificar el puerto
```shell
ssh ctf-player@titan.picoctf.net -p 61637

ctf-player@titan.picoctf.net's password: 1db87a14

Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_45a48857}
```


## Notas adicionales

## Referencias
