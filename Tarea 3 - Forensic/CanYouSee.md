## Descripción
How about some hide and seek? Download this file [here](https://artifacts.picoctf.net/c_titan/5/unknown.zip).
## Pistas
How can you view the information about the picture?
If something isn't in the expected form, maybe it deserves attention?
## Solución 1
1. Usando la herramienta `exiftool` para ver los metadatos
2. Hay una url que no parece una url, puede que este codificado `Attribution URL: cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==`
3. Usando cyberchef
```
Input: cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==
Recipe: From Base64
Output: picoCTF{ME74D47A_HIDD3N_4dabddcb}
```

## Notas adicionales


## Referencias
