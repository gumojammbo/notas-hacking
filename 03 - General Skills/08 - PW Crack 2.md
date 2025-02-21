## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.
## Pistas
Does that encoding look familiar?

The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución 1
Convirtiendo desde hexadecimal utilizando python
```python
~ % python3
>>> chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)
'39ce'
```

## Notas adicionales

## Referencias
