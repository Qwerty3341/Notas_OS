```shell
**********************
|COMANDOS PARA DOCKER|
**********************

docker images
	Lista las imagenes que se tienen instaladas actualmente
	
docker pull nombre_de_imagen
	Descarga una imagen de Docker Hub
	
docker pull imagen:versión
	Descarga una imagen con una versión especificada
	
docker pull --platform linux/x86_64 imagen
	Se le indica cual es la plataforma que queremos descargar de la imagen

docker image rm nombre_imagen
	Elimina una imagen

docker create nombre_de_imagen
docker container create nombre_de_imagen
	Hace un contenedor con una imagen (nos devuelve el id de contenedor creado)
	
docker start un_id
	Corre un contenedor
	
docker ps
	Muestra una tabla de los 
	
docker stop un_id
	Detiene un contenedor
	
docker ps -a
	Muestra todos los contenedores incluidos los que no están corriendo

docker rm nombre_de_contenedor
	Elimina un contenedor (pero ahora indicandole el name)
	
docker create --name un_nombre nombre_de_imagen
	Hace un contenedor pero especificandole un nombre

docker start un_nombre
	Inicia un contenedor pero indicandole el nombre
	
docker create -pUnPuerto:PuertoAMapear --name un_nombre_existente
	Hace un port mapping y devuelve un id
	
docker create -pUnPuerto --name un_nombre_existente
	Hace un port mapping pero Docker elige el puerto al que se redirige

docker logs un_nombre
	Muestra los logs de un container
	
docker logs --follow un_nombre
	Muestra los logs que vayan apareciendo

docker run una_imagen
	1. Ve si se encuentra la imagen
		1.1 Si no, la descarga
	2. Crea un contenedor
	3. Inicia el contenedor
	4. Muestra los logs
	
docker run -d una_imagen
	1. Ve si se encuentra la imagen
		1.1 Si no, la descarga
	2. Crea un contenedor
	3. Inicia el contenedor

docker run --name un_nombre -pUnPuerto:PuertoAMapear -d una_imagen
----------------------------------------------------------------------
Port mapping

Host
______________________________
 ______    ______    ______
|nodeJS|  |nodeJS|  |MongoDB|
  3000      3000      27017
______________________________

Los contenedores se pueden comunicar internamente
También se pueden redirigir las peticiones de un puerto hacia un contenedor
----------------------------------------------------------------------


```