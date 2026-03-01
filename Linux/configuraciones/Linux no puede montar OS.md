Usamos el comando 
```sh
lsblk -f
```
Para ver las particiones del disco
# ntfsfix
Se puede usar el `ntfsfix /dev/nombre_de_la_particion_que_dio_lsblk`

A veces dice que Windows está invernando (vamos a Windows y damos el comando)
```powershell
powercfg /h off
```