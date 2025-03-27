## Descripción
There is some interesting information hidden around this site [http://mercury.picoctf.net:5080/](http://mercury.picoctf.net:5080/). Can you find it?

## Pistas
You should have enough hints to find the files, don't run a brute forcer.
## Solución
Inspeccionando los elementos, yendo a los archivos de la pagina
1. En la raíz: `<!-- Here's the first part of the flag: picoCTF{t -->`
2. En el css: `/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */`
3. El archivos `myjs.js` nos da una pista `/* How can I keep Google from indexing my website? */`, por lo que revisamos robots.txt
4. El archivo `robots.txt` contiene
```
User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?
```
5. Usando la pista dada por `robots.txt`, vemos el archivo `.htaccess` de Apache Server
```
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
```
6. Usando la pista dada por `.htaccess`, vemos el archivo `.DS_Store`, que es común que sea creado por Mac. `Congrats! You completed the scavenger hunt. Part 5: _7a46d25d}`
7. Y armamos la bandera
`picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_7a46d25d}`
## Notas adicionales

## Referencias