Configuraciones adicionales y permanentes de nano (para home de un usuario)
```shell
nano ~/.nanorc
```
Configuración que puse el sáb 29 mar 2025 03:27:48 CST
```shell
set tabsize 4
```

# nano con sudo
Cuando se ejecuta `sudo nano` el editor no carga el nanorc ya que está en el home y no en root.

Para eso se puede modificar el `nanorc` del root que está en `/etc/nanorc`
Puse esta configuración hasta el final del archivo

```sh
set autoindent
set brackets "characters"
set linenumbers
set mouse
set tabsize 4
set indicator
```

Manual de nano:
https://www.nano-editor.org/dist/latest/nano.pdf