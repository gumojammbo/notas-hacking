## Descripción
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## Pistas
Indentation is very meaningful in Python

To view the file in the webshell, do: `$ nano fixme1.py`

To exit `nano`, press Ctrl and x and follow the on-screen prompts.

The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución 1
Corrigiendo la identación en la ultima linea.
```python
flag = str_xor(flag_enc, 'enkidu')

print('That is correct! Here\'s your flag: ' + flag)
```

## Notas adicionales

## Referencias
