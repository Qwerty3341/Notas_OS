Lista de comandos para formatear memoria desde diskpart

```shell
C:\Windows\System32>diskpart

disk list

DISKPART> list disk

DISKPART> select disk X

DISKPART> create partition primary

DiskPart ha creado satisfactoriamente la partición especificada.

DISKPART> format fs=exfat quick

  100 por ciento completado

DiskPart formateó el volumen correctamente.

DISKPART> assign

DiskPart asignó correctamente una letra de unidad o punto de montaje.

DISKPART>
```