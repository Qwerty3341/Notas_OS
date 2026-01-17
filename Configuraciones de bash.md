
| File            | Content                                                                                                                                                          |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| /etc/profile    | A global configuration script that applies to all users.                                                                                                         |
| ~/.bash_profile | A user's personal startup file. Can be used to extend or<br>override settings in the global configuration script.                                                |
| ~/.bash_login   | If ~/.bash_profile is not found, bash attempts to<br><br>read this script.                                                                                       |
| ~/.profile      | If neither ~/.bash_profile nor ~/.bash_login<br>is found, bash attempts to read this file. This is the<br>default in Debian-based distributions, such as Ubuntu. |
**Non-login shell sessions read the following startup files:**

| /etc/bash.bashrc | A global configuration script that applies to all users.                                                          |
| ---------------- | ----------------------------------------------------------------------------------------------------------------- |
| ~/.bashrc        | A user's personal startup file. Can be used to extend or<br>override settings in the global configuration script. |

---

| Archivo             | Contenido                                                                                                                                                            |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **/etc/profile**    | Un script de configuración global que se aplica a todos los usuarios.                                                                                                |
| **~/.bash_profile** | Archivo de inicio personal del usuario. Puede utilizarse para ampliar osobrescribir configuraciones definidas en el script global.                                   |
| **~/.bash_login**   | Si no se encuentra `~/.bash_profile`, bash intentaleer este script.                                                                                                  |
| **~/.profile**      | Si no se encuentran `~/.bash_profile` ni `~/.bash_login`, bash intenta leer este archivo. Es el comportamiento predeterminado en distribuciones Debian, como Ubuntu. |
**Sesiones de _non-login shell_** leen los siguientes archivos:

|Archivo|Contenido|
|---|---|
|**/etc/bash.bashrc**|Un script de configuración global que se aplica a todos los usuarios.|
|**~/.bashrc**|Archivo de inicio personal del usuario. Puede utilizarse para ampliar o  <br>sobrescribir configuraciones definidas en el script global.|