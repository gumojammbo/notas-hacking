## Descripción
There's a flag shop selling stuff, can you buy a flag? [Source](https://jupiter.challenges.picoctf.org/static/253c4651d852ac6342752ff222cf2a83/store.c). Connect with `nc jupiter.challenges.picoctf.org 9745`.
## Pistas
1. Two's compliment can do some weird things when numbers get really big!
## Solución 1
1. Podemos comporar la bandera que vale `100000` intentando desbordar el entero que almacena el valor de compra usando 2,147,483,647
2. 
```
Welcome to the flag exchange

We sell flags
1. Check Account Balance
2. Buy Flags
3. Exit

Enter a menu selection
2

Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1

These knockoff Flags cost 900 each, enter desired quantity
2147483647

The final cost is: -900
Your current balance after transaction: 2900
```

3. Intentando con un numero mayor simplemente nos expulsa, sin embargo si bajo un numero, aumenta a -1800, subiendo el balance luego de la transacción
4. Intentando con 2,147,400,000
```
The final cost is: -75283200

Your current balance after transaction: 75288800
```
5. Podemos comprar la bandera cara
```
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2

1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one
1

YOUR FLAG IS: picoCTF{m0n3y_bag5_65d67a74}
```
## Notas adicionales

## Referencias
