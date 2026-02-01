Instalamos gestor de bluetooth
```sh
sudo apt blueman
```

Vemos si tenemos pipewire
```sh
systemctl --user status pipewire
```

Si no está lo instalamos con 
```sh
sudo apt install pipewire pipewire-audio pipewire-alsa pipewire-pulse wireplumber libspa-0.2-bluetooth
```


https://usuariodebian.blogspot.com/2025/10/bluetooth-audio-en-debian-13.html