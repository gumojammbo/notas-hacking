## Descripción
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/2f998eee12730cf5766624681212a441/dds1-alpine.flag.img.gz)
## Pistas
1. Have you ever used `file` to determine what a file was?
2. Relevant terminal-fu in picoGym: https://play.picoctf.org/practice/challenge/85
3. Mastering this terminal-fu would enable you to find the flag in a single command: https://play.picoctf.org/practice/challenge/48
4. Using your own computer, you could use qemu to boot from this disk!
## Solución 1
1. Desempaquetar imagen con `gzip dds1-alpine.flag.img.gz -d`
2. Usando strings `srch_strings dds1-alpine.flag.img | grep pico`
3. Obtener la bandera `picoCTF{f0r3ns1c4t0r_n30phyt3_267e38f6}`

## Notas adicionales

## Referencias

