## Descripción
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).
## Pistas
1. Cargo is Rust's package manager and will make your life easier. See the getting started page [here](https://doc.rust-lang.org/book/ch01-03-hello-cargo.html)
2. [println!](https://doc.rust-lang.org/std/macro.println.html)
3. Rust has some pretty great compiler error messages. Read them maybe?
## Solución 1

1. Corrigiendo la sintaxis del código
```rust
let key = String::from("CSUCKS")
=================================
let key = String::from("CSUCKS");
```
2. Para salir del main solo hacemos return, como en Java, C, etc.
```rust
if res.is_err() {
	ret;
}
=================================
if res.is_err() {
	return;
}
```

3. Usar corchetes para indicar una variable
```rust
println!(
	":?", // How do we print out a variable in the println function?
	String::from_utf8_lossy(&decrypted_buffer)
);

==================================

println!(
	": {}", // How do we print out a variable in the println function?
	String::from_utf8_lossy(&decrypted_buffer)
);
```

`picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}`
## Notas adicionales

## Referencias
