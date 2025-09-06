```shell
Microsoft Windows [Versión 10.0.26100.4351]
(c) Microsoft Corporation. Todos los derechos reservados.

C:\Windows\System32>DISKPART

Microsoft DiskPart versión 10.0.26100.1150

Copyright (C) Microsoft Corporation.
En el equipo: DESKTOP-VDLU0ET

DISKPART> LIST DISK

  Núm Disco  Estado      Tamaño   Disp     Din  Gpt
  ---------- ----------  -------  -------  ---  ---
  Disco 0    En línea        931 GB  4999 MB        *
  Disco 1    En línea         57 GB    57 GB        *

DISKPART> SELECT DISK 1

El disco 1 es ahora el disco seleccionado.

DISKPART> LIST PARTITION

No hay particiones en este disco para mostrar.

DISKPART> clean

DiskPart ha limpiado el disco satisfactoriamente.

DISKPART> create partition primary

DiskPart ha creado satisfactoriamente la partición especificada.

DISKPART> list partition

  Núm Partición  Tipo              Tamaño   Desplazamiento
  -------------  ----------------  -------  ---------------
* Partición 1    Principal           57 GB  1024 KB

DISKPART> select partition 1

La partición 1 es ahora la partición seleccionada.

DISKPART> active

DiskPart marca la partición actual como activa.

DISKPART> format fs=nfts quick

    0 por ciento completado

Error del Servicio de disco virtual:
El sistema de archivos es incompatible.


DISKPART> format fs=fat32 quick

    0 por ciento completado

Error del Servicio de disco virtual:
El volumen es demasiado grande.


DISKPART> format fs=fat quick

    0 por ciento completado

Error del Servicio de disco virtual:
El volumen es demasiado grande.


DISKPART> format fs=exfat quick

  100 por ciento completado

DiskPart formateó el volumen correctamente.

DISKPART>
```