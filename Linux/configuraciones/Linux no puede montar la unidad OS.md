> [!NOTE] Descripción
> Cuando se da al ícono de la unidad OS en el escritorio o en el gestor de archivos sale un error que no se puede montar la unidad
# Solución
1. Cuando te muestra el error te dice como el id de la partición (se encuentran en el directorio /dev/)
2. Con ese id se va a ejecutar el siguiente comando
	1. ```sh
	   sudo ntfsfix -d /dev/nombre_particion
	   ```
# Referencias
https://bbs.archlinux.org/viewtopic.php?id=271650