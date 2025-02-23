## Descripción
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/72/challenge.zip)
## Pistas
In collaborative projects, many users can make many changes. How can you see the changes within one file?

Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).

You can use `python3 <file>.py`to try running the code, though you won't need to for this challenge.

## Solución 1
Utilizando el comando `git log` con el nombre del archivo para ver los cambios en ese archivo
```shell
% git log message.py 

commit 9ae3e1bc67ad0143c611c5f65399b79850d20983

Author: picoCTF{@sk_th3_1nt3rn_b64c4705} <ops@picoctf.com>

Date:   Sat Mar 9 21:09:01 2024 +0000

    optimize file size of prod code
    ```


## Notas adicionales

## Referencias
