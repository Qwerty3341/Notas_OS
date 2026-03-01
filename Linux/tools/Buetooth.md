Vemos si tenemos pipewire
```sh
systemctl --user status pipewire
```

Si no está lo instalamos con 
```sh
sudo apt install pipewire pipewire-audio pipewire-alsa pipewire-pulse wireplumber libspa-0.2-bluetooth
```
https://usuariodebian.blogspot.com/2025/10/bluetooth-audio-en-debian-13.html
# Por gestor de bluetooth
Instalamos gestor de bluetooth
```sh
sudo apt blueman
```

# Por terminal con bluetoothctl 
Activar bluetooth
```sh
sudo systemctl enable bluetooth --now
```

Entramos a `bluetoothctl` 
```sh
bluetoothctl
```

Encender el adaptador
```sh
[bluetoothctl]> power on
```

Encender el agente (maneja las solicitudes de emparejamiento)
```sh
agent on
```

Dejar el agente como default 
```sh
default-agent
```

Para reconocer dispositivos bluetooth
```sh
scan on
```

Cuando ya no queremos buscar dispositivos
```sh
scan off
```

> [!NOTE] scan off y MAC
> El scan off nos enseña dispositivos bluetooth con la red MAC y el nombre del dispositivo 
> Ejemplo: AA:BB:CC:DD:EE:FF

Emparejar el dispositivo
```sh
pair AA:BB:CC:DD:EE:FF
```

Esto por si pide confirmación
```sh
yes
```

Confiar en el dispositivo
```sh
trust AA:BB:CC:DD:EE:FF
```

Conectarse al dispositivo
```sh
connect AA:BB:CC:DD:EE:FF
```

Para ver dispositivos conocidos
```sh
devices
```

Ver información de dispositivo 
```sh
info AA:BB:CC:DD:EE:FF
```

Salir de `bluetoothctl`
```
exit
```

## Para conectarse rápido 
```sh
bluetoothctl connect AA:BB:CC:DD:EE:FF
```
## Quitar un dispositivo
```
remove AA:BB:CC:DD:EE:FF
```
## Desconectar un dispositivo
```
bluetoothctl
```

```
devices
```

```
disconnect AA:BB:CC:DD:EE:FF
```
### Desconectar rápido
```
bluetoothctl disconnect AA:BB:CC:DD:EE:FF
```
