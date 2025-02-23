## Descripción
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/69/challenge.zip)
## Pistas
`git branch -a` will let you see available branches

How can file 'diffs' be brought to the main branch? Don't forget to `git config`!

Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.

## Solución 1
Uniendo las 3 ramas de git en las que están distintos cambios al archivo.
```shell
  git branch -a
  
  feature/part-1

  feature/part-2

  feature/part-3
  
  main
    ```

```shell
git merge feature/part-1
```

Despues se tienen que eliminar los conflictos, modificando el archivo de tal forma que se eliminen los marcadores de conflicto (<<<======>>>>)
```shell
git merge feature/part-2

nano flag.py

git add flag.py

git commit -m "Resolver conflicto"

git merge feature/part-2
```
```shell
git merge feature/part-3

nano flag.py

git add flag.py

git commit -m "Resolver conflicto 2"

git merge feature/part-2

python3 flag.py
	
	Printing the flag...
	picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_e4b79efb}
```


## Notas adicionales

## Referencias
