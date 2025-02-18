## Descripción
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!
 
## Pistas
none

## Solución 1
Usando `ltdis.sh`, dando permisos de ejecucion, y usando grep para ver la bandera
```
~ % ./ltdis.sh

~ % chmod +x ltdis.sh

~ % ./ltdis.sh static
Attempting disassembly of static ...

Disassembly successful! Available at: static.ltdis.x86_64.txt

Ripping strings from binary with file offsets...

Any strings found in static have been written to static.ltdis.strings.txt with file offset

~ % cat static.ltdis.strings.txt | grep pico

1020 picoCTF{d15a5m_t34s3r_f5aeda17}
```


## Notas adicionales

## Referencias
