## Descripción
Help us test the form by submiting the username as `test` and password as `test!`

The website running [here](http://saturn.picoctf.net:59755/).
## Pistas
1. any redirections?
## Solución 1
1. Entrando a la pagina con el usuario y contraseña dados
2. Abriendo las herramientas de desarrollador y retrocediendo, podemos ver las redirecciones
3. Vemos que en la URL de cada una hay algo codificado
4. Decoficiando con cyberchef
```
Input:  cGljb0NURntwcm94aWVzX2Fs
		bF90aGVfd2F5XzAxZTc0OGRifQ==
Recipe: Base64
Ouput: picoCTF{proxies_all_the_way_01e748db}
```

## Referencias
