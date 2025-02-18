## Descripción
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `abcba9f7`

Additional details will be available after launching your challenge instance.
## Pistas
Finding a cheatsheet for bash would be really helpful!
## Solución 1
Utilizando el comando `ls y cat`
```
ctf-player@pico-chall$ ls

	1of3.flag.txt  instructions-to-2of3.txt

ctf-player@pico-chall$ cat 1of3.flag.txt 

	picoCTF{xxsh_

ctf-player@pico-chall$ cat instructions-to-2of3.txt 

	Next, go to the root of all things, more succinctly `/`

ctf-player@pico-chall$ cd /

ctf-player@pico-chall$ ls

	2of3.flag.txt     instructions-to-3of3.txt  

ctf-player@pico-chall$ cat 2of3.flag.txt 

	0ut_0f_\/\/4t3r_
	
ctf-player@pico-chall$ cat instructions-to-3of3.txt 

	Lastly, ctf-player, go home... more succinctly `~`

ctf-player@pico-chall$ cd ~

ctf-player@pico-chall$ ls

	3of3.flag.txt  drop-in

ctf-player@pico-chall$ cat 3of3.flag.txt 

	21cac893}
```

Juntando las partes encontradas
`picoCTF{xxsh_0ut_0f_\/\/4t3r_21cac893}`
## Notas adicionales
Revisar tipo de archivo usando `file`

## Referencias
