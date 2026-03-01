Activar wi fi desde terminal 
```
# Escanear redes disponibles
nmcli dev wifi list

# Conectar a una red
nmcli dev wifi connect "NOMBRE_DE_LA_RED" password "TU_CONTRASEÑA"

# O editar conexiones guardadas
nmcli connection edit "NOMBRE_DE_LA_CONEXION"
```

