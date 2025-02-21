## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.
There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Pistas
To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`

To exit `bvi` type `:q` and press enter.

The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución 1
Probando todas las posibles contraseñas modificando el script
```python
def level_3_pw_check():

	pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]
	for user_pw in pos_pw_list:
		user_pw_hash = hash_pw(user_pw)
		if( user_pw_hash == correct_pw_hash ):
			print("Welcome back... your flag, user:")
			decryption = str_xor(flag_enc.decode(), user_pw)
			print(decryption)
			return
		print("That password is incorrect")
```

## Notas adicionales

## Referencias
