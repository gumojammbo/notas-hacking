## Descripción
Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.

Our flag printing service has started glitching!`$ nc saturn.picoctf.net 56438`
## Pistas
1. ASCII is one of the most common encodings used in programming
2. We know that the glitch output is valid Python, somehow!
3. Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

## Solución 1
Utilizando el programa `python` con el output proporcionado por netcat
``` shell
Input: 
nc saturn.picoctf.net 56438

python3

Output: 

**>>>** 'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'

'picoCTF{gl17ch_m3_n07_a4392d2e}'

```



## Notas adicionales

## Referencias
