## Descripción
Can you read files in the root file?

Additional details will be available after launching your challenge instance.
## Pistas
What permissions do you have?

The system admin has provisioned an account for you on the main server:`ssh -p 61932 picoplayer@saturn.picoctf.net`
termi
Password: `yX-YQgX-vS`
Can you login and read the root file?
## Solución 1
Usando el comando `vi` como superusuario para poder leer los archivos.
```shell

$ ls -l

	drwx------   1 root   root     34 Feb 23 01:57 root

$ sudo vi root/ 
                             
	.vim
	
	.bashrc
	
	.flag.txt
	
	.profile
	
	.viminfo

$ sudo vi root/.flag.txt

	picoCTF{uS1ng_v1m_3dit0r_55878b51}
```


## Notas adicionales

## Referencias
