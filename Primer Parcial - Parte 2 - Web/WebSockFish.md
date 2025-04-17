## Descripción
Can you win in a convincing manner against this chess bot? He won't go easy on you!

You can find the challenge [here](http://verbal-sleep.picoctf.net:54668/).
## Pistas
1. Try understanding the code and how the websocket client is interacting with the server
## Solución 1
1. Vemos que en el codigo fuente de la pagina hay un metodo sendMessage, donde hay dos tipos, mate y eval.
2. Probando con mate y un numero el pez cambia de mensaje
3. Usando eval y un numero muy grande nos da la bandera `eval 100000000`
4. `picoCTF{c1i3nt_s1d3_w3b_s0ck3t5_50441bef}`
## Referencias
