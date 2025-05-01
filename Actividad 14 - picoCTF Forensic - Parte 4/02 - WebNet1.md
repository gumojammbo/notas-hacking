## Descripción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Pistas
1. Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?

## Solución 1
1. Cargar la captura de paquetes en wireshark
2. Agregar la llave para desencriptar el trafico yendo a `Preferencias -> Protocols -> TLS -> RSA keys list` y agregar el archivo `picopico.key`.
3. Seguir el stream TLS en los paquetes desencriptados hasta encontrar la bandera
`picoCTF{honey.roasted.peanuts}

## Notas adicionales

## Referencias
