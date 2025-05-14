## Descripción
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/d1375e383810d8d957c04eef9e345732/cat.jpg)
## Pistas
Look at the details of the file
Make sure to submit the flag as picoCTF{XXXXX}
## Solución 1
1. Usando la herramienta `exiftool` para ver los metadatos
2. Hay un metadato que parece estar codificado `License: cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
`
3. Usando cyberchef
```
Input: cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Recipe: From Base64
Output: picoCTF{the_m3tadata_1s_modified}
```


## Notas adicionales


## Referencias
