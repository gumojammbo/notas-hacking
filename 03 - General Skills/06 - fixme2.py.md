## Descripción
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## Pistas
Are equality and assignment the same symbol?

To view the file in the webshell, do: `$ nano fixme2.py`

To exit `nano`, press Ctrl and x and follow the on-screen prompts.

The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución 1
Corrigiendo el simbolo de comparación en el script
```python
if flag == "":
	print('String XOR encountered a problem, quitting.')
else:
	print('That is correct! Here\'s your flag: ' + flag)
```

## Notas adicionales

## Referencias
