## Descripción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Pistas
1. Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?

## Solución 1
1. Cargar la captura de paquetes en wireshark
2. Agregar la llave para desencriptar el trafico yendo a `Preferencias -> Protocols -> TLS -> RSA keys list` y agregar el archivo `picopico.key`.
3. Seguir el stream TLS en los paquetes desencriptados hasta encontrar la bandera
`picoCTF{nongshim.shrimp.crackers}`

sudo mkdir -p /Library/Preferences/FeatureFlags/Domain && sudo /usr/libexec/PlistBuddy -c "Add 'redesigned_text_cursor:Enabled' bool false" /Library/Preferences/FeatureFlags/Domain/UIKit.plist && sudo shutdown -r now
## Notas adicionales

## Referencias
