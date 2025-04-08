## Descripción
Try [here](http://titan.picoctf.net:60755/) to find the flag
## Pistas
1. Try using burpsuite to intercept request to capture the flag.
2. Try mangling the request, maybe their server-side code doesn't handle malformed requests very well.

## Solución 1
1. Interceptando las solicitudes en burpsuite, vemos que al enviar el OTP hay una solicitud POST
2. Cambiamos el nombre de la variable `otp` por cualquiera.
```
otp=pablo
----------
pablo = pablo
```
3. Enviamos la solicitud usando el repeater
4. Nos da la bandera
`picoCTF{#0TP_Bypvss_SuCc3$S_3e3ddc76}`
## Notas adicionales

## Referencias
