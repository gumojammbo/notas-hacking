## Descripción
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 22902`, but it doesn't speak English...
## Pistas
1. You can practice using netcat with this picoGym problem: [what's a netcat?](https://play.picoctf.org/practice/challenge/34)
2. You can practice reading and writing ASCII with this picoGym problem: [Let's Warm Up](https://play.picoctf.org/practice/challenge/22)

## Solución 1
Utilizando la herramienta [cyberchef](https://cyberchef.io/#recipe=From_Decimal('Line%20feed',false)&input=MTEyIAoxMDUgCjk5IAoxMTEgCjY3IAo4NCAKNzAgCjEyMyAKMTAzIAo0OCAKNDggCjEwMCAKOTUgCjEwNyAKNDkgCjExNiAKMTE2IAoxMjEgCjMzIAo5NSAKMTEwIAo0OSAKOTkgCjUxIAo5NSAKMTA3IAo0OSAKMTE2IAoxMTYgCjEyMSAKMzMgCjk1IAoxMDAgCjUxIAoxMDAgCjEwMiAKMTAwIAo1NCAKMTAwIAoxMDIgCjEyNSAKMTAgCg)
``` shell
Input: 
112 

105 

99 

111 

67 

84 

70 

123 

103 

48 

48 

100 

95 

107 

49 

116 

116 

121 

33 

95 

110 

49 

99 

51 

95 

107 

49 

116 

116 

121 

33 

95 

100 

51 

100 

102 

100 

54 

100 

102 

125 

10

Recipe: From Decimal (Line feed delimiter)

Output: 
picoCTF{g00d_k1tty!_n1c3_k1tty!_d3dfd6df}

```



## Notas adicionales

## Referencias
