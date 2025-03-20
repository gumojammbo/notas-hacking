## Descripción
Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?You can access the Cookie Monster [here](http://verbal-sleep.picoctf.net:60118/) and good luck
## Pistas
Sometimes, the most important information is hidden in plain sight. Have you checked all parts of the webpage?

Cookies aren't just for eating - they're also used in web technologies!

Web browsers often have tools that can help you inspect various aspects of a webpage, including things you can't see directly.
## Solución 1
Usando el inspector web de safari, en la parte de cookies
```shell

Cookies:
	Name: secret_recipe
	value: cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzX0E5NjRBMTM0fQ%3D%3D	
```

Luego usando cyberChef
```
Input: cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzX0E5NjRBMTM0fQ%3D%3D

Recipe: From Base64

Output: picoCTF{c00k1e_m0nster_l0ves_c00kies_A964A134}
```

## Notas adicionales

## Referencias
