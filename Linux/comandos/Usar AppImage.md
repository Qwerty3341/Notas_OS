# Darle permisos de ejecución
```sh
chmod + x imagen.AppImage
```
# Hay algunas imágenes que incluyen archivos extra
```sh
./drawio-x86_64-29.6.1.AppImage --appimage-extract
```
# Para agregarla al menú de aplicaciones
Se puede poner en `/usr/share/applications` o en `~/.local/share/applications`

Se hace un archivo `.desktop` por ejemplo:
```txt
[Desktop Entry]
Name=draw.io
Exec=/opt/drawio/AppRun
Icon=/opt/drawio/drawio.png
Type=Application
Categories=Office;Development;
Comment=Diagramming tool
Terminal=false
```
