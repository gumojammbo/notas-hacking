## Descripción
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/136/challenge.zip)

## Pistas
Version control can help you recover files if you change or lose them!

Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)

You can 'checkout' commits to see the files inside them


## Solución 1
Utilizando el comando `git log` para ver el historial de commits del repositorio, luego `git checkout <commit>` para regresar el repositorio al punto en el que estaba en ese commit.
```shell
$ git log

$ git checkout 87b85d7dfb839b077678611280fa023d76e017b8

	HEAD is now at 87b85d7 create flag

$ cat message.txt

	picoCTF{s@n1t1z3_ea83ff2a}
```


## Notas adicionales

## Referencias
