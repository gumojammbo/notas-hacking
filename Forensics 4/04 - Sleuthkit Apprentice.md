## Descripción
Download this disk image and find the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.
## Pistas
[Download compressed disk image](https://artifacts.picoctf.net/c/138/disk.flag.img.gz)
## Solución 1
1. Desempaquetar imagen con `gzip disk.flag.img.gz -d`
2. Usando mmls para ver las particiones `mmls disk.flag.img`
```
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)


```
3. Podemos ver los archivos de bandera de cada particion con (Asumimos un sistema de archivos `ext4` ya que se trata de Linux)
```bash
fls -f ext4 -o 360448 -r disk.flag.img 

+ r/r 2363:     .ash_history
+ d/d 3981:     my_folder
++ r/r * 2082(realloc): flag.txt
++ r/r 2371:    flag.uni.txt

```
3. Usando el comando `icat` podemos leer los archivos, especificando su direccion
```bash
icat disk.flag.img -o 360448 2371  -f ext4
picoCTF{by73_5urf3r_2f22df38}
```

## Notas adicionales

1. Podemos ver como se elimino la bandera `flag.txt` viendo el archivo `.ash_history`
```bash
icat disk.flag.img -o 360448 2363  -f ext4
apk add nano
mkdir my_folder
cd my_folder/
nano flag.txt
ls -al
iconv -f ascii -t utf16 > flag.uni.txt
l
ls -al
iconv -f ascii -t utf16 flag.txt > flag.uni.txt
ls -al
shred
shred -zu flag.txt 
ls -al
halt
```

## Referencias

