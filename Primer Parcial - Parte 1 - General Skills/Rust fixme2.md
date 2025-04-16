## Descripción
The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).
## Pistas
1. https://doc.rust-lang.org/book/ch04-02-references-and-borrowing.html
## Solución 1
1. Definir que el argumento de la función sera mutable:
```rust 
fn decrypt(encrypted_buffer:Vec<u8>, borrowed_string: &mut String){
```
2. Definir una variable mutable en:
```rust
let mut party_foul = String::from("Using memory unsafe languages is a: "); 
```
3. Definir que se trata de un argumento mutable en
```rust
decrypt(encrypted_buffer, &mut party_foul); 
						^^^^^^^^
```

4. Obtener la bandera `picoCTF{4r3_y0u_h4v1n5_fun_y31?}`

## Notas adicionales

## Referencias
