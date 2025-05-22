## Descripción
Can you get the real meaning from this file. Download the file [here](https://artifacts.picoctf.net/c_titan/111/enc_flag).
## Pistas
Engaging in various decoding processes is of utmost importance
## Solución 1
## Solucion 2
1. Usando la herramienta cyberchef
```
Input: YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6ZzVNR3N5TXpjNWZRPT0nCg==
Recipe: From Base64
Output: b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fQ=='
```
2. Usando de nuevo la herramienta cyberchef con el texto que esta entre comillas
```
Input: d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fQ==
Recipe: From Base64
Output: wpjvJAM{jhlzhy_k3jy9wa3k_890k2379}
```
3. Ahora recorriendo el abecedario 19 posiciones
```
Input: wpjvJAM{jhlzhy_k3jy9wa3k_890k2379}
Recipe: ROT
Output: wpjvJAM{jhlzhy_k3jy9wa3k_890k2379}
```
## Notas adicionales


## Referencias
