## Descripción
A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their message Try it [here](http://standard-pizzas.picoctf.net:55602/)!
## Pistas
1. In the country that doesn't exist, the flag persists
## Solución 1
1. Vemos las banderas, vemos una que no parece de un pais
2. Aplicando `file` a la imagen, se observa que es demasiado grande
3. Usando la herramienta `stepic` podemos decodificar la imagen con el comando `stepic -d -i upz.png`
4. Obtenemos la bandera `picoCTF{fl4g_h45_fl4g3e22f365}`
## Notas adicionales


## Referencias
