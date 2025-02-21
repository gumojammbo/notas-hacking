## Descripción
Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/35/serpentine.py)

## Pistas
Try running the script and see what happens

In the webshell, try examining the script with a text editor like `nano`

To exit `nano`, press Ctrl and x and follow the on-screen prompts.

The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución 1
Llamar a la función para imprimir la bandera en el lugar correcto
```python
elif choice == 'b':
	print('\nOops! I must have misplaced the print_flag function! Check my source code!\n\n')
	print_flag()
```

## Notas adicionales

## Referencias
