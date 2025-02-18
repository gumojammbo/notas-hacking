## Descripción
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm) has extraordinarily helpful information...
 
## Pistas
This program will only work in the webshell or another Linux computer.

To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm`

Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`

-h and --help are the most common arguments to give to programs to get more information from them!

Not every program implements help features like -h and --help.

## Solución 1
Usando el argumento `-h`
```
$ ./warm -h

Oh, help? I actually don't do much, but I do have this flag here: 
picoCTF{b1scu1ts_4nd_gr4vy_d6969390}
```


## Notas adicionales

## Referencias
