## Descripción
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/205adad23bf9d8303081a0e71c9beab8/dolls.jpg)

## Pistas
1. Wait, you can hide files inside files? But how do you find them?
2. Make sure to submit the flag as picoCTF{XXXXX}

## Solución 1
1. Usando la utilidad `binwalk` para extraer archivos que estén dentro de otros. `binwalk -e dolls.jpg`, nos da una carpeta con los archivos encontrados.
2. En la imagen encontrada, volvemos a utilizar el mismo comando `binwalk -e 2_c.jpg`, nos da otra carpeta
3. Volvemos a usar el comando `binwalk -e 3_c.jpg`, nos vuelve a dar otra carpeta
4. Una vez mas usamos el comando `binwalk -e 4_c.jpg`, y nos da otra carpeta con un archivo `flag.txt` dentro
5. Obtenemos la bandera: `picoCTF{96fac089316e094d41ea046900197662} `
## Notas adicionales

## Referencias
