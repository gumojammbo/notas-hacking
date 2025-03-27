## Descripción
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:47967/](http://mercury.picoctf.net:47967/)
## Pistas
1. Maybe you have more than 2 choices
2. Check out tools like Burpsuite to modify your requests and look at the responses
## Solución

Enviando una solicitud POST en la terminal
```bash
curl -I http://mercury.picoctf.net:47967
	HTTP/1.1 200 OK
	**flag**: picoCTF{r3j3ct_th3_du4l1ty_cca66bd3}
	**Content-type**: text/html; charset=UTF-8
```

## Notas adicionales
```bash
curl -x GET
curl -X POST
curl -I HEAD
```

## Referencias