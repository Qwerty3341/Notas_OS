https://linuxmint-installation-guide.readthedocs.io/en/latest/verify.html

- Se descarga iso
- Se descarga el checksum file
- Se usan los sig comandos

# Windows
```shell
certutil -hashfile .\linuxmint-22.1-cinnamon-64bit.iso sha256
```
Nos devuelve el hash y verificamos si es igual al del checksum
# Linux
```shell
sha256sum imagen.iso
```