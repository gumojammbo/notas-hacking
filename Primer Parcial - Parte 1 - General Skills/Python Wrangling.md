## Descripción
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/ende.py) using [this password](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/pw.txt) to get [the flag](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/flag.txt.en)?
## Pistas
1. Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/ende.py`
2. `$ man python`
## Solución 1
1. Ejecutando el programa con el comando, indicando la bandera encriptada con el argumento -d
```bash
python3 ende.py -d flag.txt.en
```
2. Usando la contraseña proporcionada
```bash
Please enter the password:6008014f6008014f6008014f6008014f
```
3. Obtener la bandera
`picoCTF{4p0110_1n_7h3_h0us3_6008014f}`
## Notas adicionales

## Referencias
