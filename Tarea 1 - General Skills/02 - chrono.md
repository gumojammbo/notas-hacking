## Descripción
How to automate tasks to run at intervals on linux servers?

Additional details will be available after launching your challenge instance.

Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 56077
Username: picoplayer 
Password: 5wf1w1hVxt

ssh picoplayer@saturn.picoctf.net -p 56077
```

## Pistas
--


## Solución 1
Leyendo el archivo `crontab` para ver la lista de acciones programadas en el servidor.
```shell

$ cat /etc/crontab

# picoCTF{Sch3DUL7NG_T45K3_L1NUX_9d5cb744}
```


## Notas adicionales
En el archivo `/etc/crontab` se puede ver una lista de acciones programadas utilizando `cron` de Linux

## Referencias
