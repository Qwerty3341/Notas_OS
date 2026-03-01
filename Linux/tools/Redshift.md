Sirve para activar una luz noctura (la amarilla)

# Instalación
```sh
sudo apt install redshift
```
(existe también el paquete `redshift-gtk` que es como una interfaz gráfica pero esa no sirve en wayland)
# Comandos
## Para activar la luz
```sh
redshift -O temperatura
```
La temperatura debe estar entre 1000 K y 25000 K.
## Para quitar la luz
```sh
redshift -x 
```
# Configuración
En el directorio `.config` hacemos un archivo que se llame `redshift.conf`
```
[redshift]
# Forzar X11 (RANDR). No Wayland.
adjustment-method=randr

# Ubicación manual (no GeoClue)
location-provider=manual

# Temperaturas
temp-day=6500
temp-night=3500

# Transición suave (segundos)
transition=1

# Brillo opcional
brightness-day=1.0
brightness-night=0.9

[manual]
lat=19.43
lon=-99.13
```

(Se pueden omitir algunas cosas)