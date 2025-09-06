```bash
Comandos de git

git clone "dirección del repositorio" 
	Clona un repositorio

git init 
	Hace la carpeta .git en una ruta

git branch -M main 
	hace la rama main

git remote add origin "link del repositorio" 
	vincula el repositorio local con el de la nube

git status
	Muestra el estatus de los archivos del repositorio

git add "Nombre del archivo" 
	Agrega los archivos del proyecto que se le indiquen 

git add . 
	Añade todos los archivos 

git commit -m "Descripcion" 
	Hace un commit

git push 
	Se le envian los archivos para el último commit que realizó 

git pull 
	Añade los cambios que se han hecho en el proyecto (de las otras personas)

git branch 
	Muestra las ramas que se tienen en en repositorio

git branch "Nombre de la nueva rama" 
	Agrega una nueva rama al repositorio

git checkout "Nombre de la rama"
	Cambia la rama en la que se está trabajando

git merge "Nombre de la rama" 
	Fusiona la rama indicada con la rama actual

git push origin "Nombre de la rama" 
	Origin se refiere a la versión del proyecto que tu tienes a raíz de hacer un fork

git diff 
	Ve los cambios que se le hicieron a el trabajo
	
git log un_archivo
	Ve el historial de confirmaciones que afectan un archivo específico	
```