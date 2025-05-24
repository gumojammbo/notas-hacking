## Descripción
In RSA d is a lot bigger than e, why don't we use d to encrypt instead of e? Connect with `nc jupiter.challenges.picoctf.org 18243`.
## Pistas
What is e generally?
## Solución 
1. Cambiamos el valor de e, del dado al valor por defecto de RSA `e = 65537`
2. Ya que el algoritmo fue usado al reves, usamos la formula de encriptacion para desencriptar `m = pow(c, e, n)`
3. Decodificamos el resultado
```
m = 180638594769037903267909311328535969949661653466129492033745533

bytes.fromhex(hex(m)[2:]).decode()
'picoCTF{bad_1d3a5_4783252}'
```

## Notas adicionales

## Referencias