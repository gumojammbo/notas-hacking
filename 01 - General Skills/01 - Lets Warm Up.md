## Descripción
 If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?
 
## Pistas
Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

## Solución 1

Ir a la tabla ASCII

## Solución 2
Con python
``` python
Python 3.13.1 (main, Dec  3 2024, 17:59:52) [Clang 16.0.0 (clang-1600.0.26.4)] on darwin

Type "help", "copyright", "credits" or "license" for more information.

**>>>** chr(0x70)

'p'


picoCTF(p)

```

## Solución 3
Usando una herramienta llamada cyberchef https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg3MA
```
Input: 0x70

Recipe: From Hex

Output: p

```



## Notas adicionales

## Referencias
https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg3MA