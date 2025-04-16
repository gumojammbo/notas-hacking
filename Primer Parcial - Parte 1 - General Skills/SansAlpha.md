## Descripción
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.

`ssh -p 52676 ctf-player@mimas.picoctf.net`Use password: `1ad5be0d`
## Pistas
1. Where can you get some letters?
## Solución 1
1. Usando expresiones regulares con wildcards se puede navegar por el sistema
2. `*/*` vemos que hay un archivo flag.txt
3. Para abrirlo podemos usar Base64, podemos acceder a base64 usando, con `![_]` excluimos guiones bajos, para asegurarnos que solo usamos base64 
```bash
/???[!_]64
```
4. Podemos seleccionar nuestro archivo usando
```
*/????.*
```
5. Juntando las expresiones `/???[!_]64 */????.*`
6. Nos da la bandera codificada `cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV83NzVhYzEyZH0`
7. Decodificando con base64
`return 0 picoCTF{7h15_mu171v3r53_15_m4dn355_775ac12d}`

## Notas adicionales

## Referencias
