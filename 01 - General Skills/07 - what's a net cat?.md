## Descripción
Using netcat (nc) is going to be pretty important. Can you connect to `jupiter.challenges.picoctf.org` at port `41120` to get the flag?
## Pistas
nc [tutorial](https://linux.die.net/man/1/nc)

## Solución 1
Utilizando el programa `cat` con el archivo proporcionado
``` shell
Input: 
nc jupiter.challenges.picoctf.org 41120 > filename.out

cat filename.out

Output: 
You're on your way to becoming the net cat master

picoCTF{nEtCat_Mast3ry_3214be47}

```



## Notas adicionales

## Referencias
