## Descripción
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!
## Pistas
## Solución 1
1. Primero vemos el tipo de archivo
```
file whitepages.txt 
whitepages.txt: Unicode text, UTF-8 text, with very long lines (1376), with no line terminators
```
2. Vemos que tiene efectivamente tiene algo, lo abrimos con un editor de texto
3. Reemplazamos el primer espacio en blanco por un 1
4. Vemos que quedan espacios sin remplazar, por lo que remplazamos lo restante por un 0
5. Convertimos el binario restante y obtenemos la bandera

`picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}`
## Notas adicionales

## Referencias
https://es.wikipedia.org/wiki/Unicode
