Para cambiar el nombre de la compu se usan estos pasos.

1. Ver el nombre de la maquina con:
	`hostname`
	o
	`hostnamectl`
2. Entrar como superusuario
	`sudo su`
3. Colocar el comando
	`hostnamectl set-hostname nombreNuevo`
4. Confirmar los cambios con:
	`nano /etc/hosts`
5. Poner el mismo nombre en el renglón donde dice 127.0.1.1
6. Confirmar los cambios