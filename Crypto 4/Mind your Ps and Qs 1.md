## Descripción
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values)
## Pistas
Bits are expensive, I used only a little bit over 100 to save money
## Solución 1
1. Para obtener `d` se necesita saber el valor de `tn` y para el se necesita tener `p` y `q`, se puede probar factorizando `n`. 
```python
c = 964354128913912393938480857590969826308054462950561875638492039363373779803642185
n = 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
e = 65537
```
2. La pagina factorDB nos indica que existe una factorización con dos numeros, por lo que obtenemos los siguientes valores:
```python
p = 2434792384523484381583634042478415057961
q = 650809615742055581459820253356987396346063
```
3. Comprobamos que `p * q = n`
```python
>>> p * q
1584586296183412107468474423529992275940096154074798537916936609523894209759157543
```
4. Calculamos `tn` y `d` para obtener la llave privada
```python
tn = (p-1) * (q-1)
d = pow(e, -1, tn)
```

5. Usando la siguiente formula, podemos descifrar el texto y despues lo decodificamos.
```python
m = pow(c,d,n)
m =
13016382529449106065927291425342535437996222135352905256639684640304028661985917
bytes.fromhex(hex(m)[2:])
b'picoCTF{sma11_N_n0_g0od_73918962}'
```
## Notas adicionales


## Referencias
factordb.com