## Descripción
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.

`ssh -p 51186 ctf-player@saturn.picoctf.net`. The password is `af86add3`
## Pistas
1. What programs do you have access to?
## Solución 1
1. Vemos los programas disponibles con `help`
2. Vemos que ls, cat, etc. No están disponibles
3. Podemos usar `echo *` para ver los archivos y directorios, igualmente usando `echo * */*` podemos ver que hay dentro de los directorios.
4. Podemos abrir archivos con `echo "$(<archivo.txt)"`
5. Probamos con los directorios
```
Specialer$ echo * */*

abra ala sim abra/cadabra.txt abra/cadaniel.txt ala/kazam.txt ala/mode.txt sim/city.txt sim/salabim.txt

Specialer$ echo "$(<abra/cadabra.txt)"

Nothing up my sleeve!

Specialer$ echo "$(<abra/cadaniel.txt)"

Yes, I did it! I really did it! I'm a true wizard!

Specialer$ echo "$(<ala/kazam.txt)"
```
6. Encontramos la bandera `return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_a8567b6f}`

## Referencias
