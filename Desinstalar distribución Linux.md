# En Linux colocar los comandos  
>[!WARNING]  
>El id del orden de prioridad no siempre es el mismo, se debe verificar cual es windows y cual es Linux  
  
## 1. Ver el orden de arranque para ver la prioridad  
```sh  
$ efibootmgr    
BootCurrent: 0002    
Timeout: 1 seconds    
BootOrder: 0002,0000,0003,0004,0005,0006    
Boot0000* Windows Boot Manager  HD(1,GPT,64025f92-2885-411a-bc74-a7e1a22    
6287d,0x800,0x32000)/\EFI\MICROSOFT\BOOT\BOOTMGFW.EFI57494e444f575300010    
0000088000000780000004200430044004f0042004a004500430054003d007b003900640    
06500610038003600320063002d0035006300640064002d0034006500370030002d00610    
06300630031002d006600330032006200330034003400640034003700390035007d00000    
064000100000010000000040000007fff0400    
Boot0002* Fedora        HD(1,GPT,64025f92-2885-411a-bc74-a7e1a226287d,0x    
800,0x32000)/\EFI\FEDORA\SHIMX64.EFI    
Boot0003* Fedora        HD(1,GPT,64025f92-2885-411a-bc74-a7e1a226287d,0x    
800,0x32000)/\EFI\FEDORA\SHIM.EFI0000424f    
Boot0004* UEFI:CD/DVD Drive     BBS(129,,0x0)    
Boot0005* UEFI:Removable Device BBS(130,,0x0)    
Boot0006* UEFI:Network Device   BBS(131,,0x0)  
```  
## 2. Eliminar el arranque de Linux  
```sh  
$ sudo efibootmgr -b 0002    
[sudo] contraseña para qwerty:      
BootCurrent: 0002    
Timeout: 1 seconds    
BootOrder: 0002,0000,0003,0004,0005,0006    
Boot0000* Windows Boot Manager  HD(1,GPT,64025f92-2885-411a-bc74-a7e1a22    
6287d,0x800,0x32000)/\EFI\MICROSOFT\BOOT\BOOTMGFW.EFI57494e444f575300010    
0000088000000780000004200430044004f0042004a004500430054003d007b003900640    
06500610038003600320063002d0035006300640064002d0034006500370030002d00610    
06300630031002d006600330032006200330034003400640034003700390035007d00000    
064000100000010000000040000007fff0400    
Boot0002* Fedora        HD(1,GPT,64025f92-2885-411a-bc74-a7e1a226287d,0x    
800,0x32000)/\EFI\FEDORA\SHIMX64.EFI    
Boot0003* Fedora        HD(1,GPT,64025f92-2885-411a-bc74-a7e1a226287d,0x    
800,0x32000)/\EFI\FEDORA\SHIM.EFI0000424f    
Boot0004* UEFI:CD/DVD Drive     BBS(129,,0x0)    
Boot0005* UEFI:Removable Device BBS(130,,0x0)    
Boot0006* UEFI:Network Device   BBS(131,,0x0)  
```  
## 3. Poner como prioridad a Windows boot manager  
```sh  
$ sudo efibootmgr -o 0000    
BootCurrent: 0002    
Timeout: 1 seconds    
BootOrder: 0000    
Boot0000* Windows Boot Manager  HD(1,GPT,64025f92-2885-411a-bc74-a7e1a22    
6287d,0x800,0x32000)/\EFI\MICROSOFT\BOOT\BOOTMGFW.EFI57494e444f575300010    
0000088000000780000004200430044004f0042004a004500430054003d007b003900640    
06500610038003600320063002d0035006300640064002d0034006500370030002d00610    
06300630031002d006600330032006200330034003400640034003700390035007d00000    
064000100000010000000040000007fff0400    
Boot0002* Fedora        HD(1,GPT,64025f92-2885-411a-bc74-a7e1a226287d,0x    
800,0x32000)/\EFI\FEDORA\SHIMX64.EFI    
Boot0003* Fedora        HD(1,GPT,64025f92-2885-411a-bc74-a7e1a226287d,0x    
800,0x32000)/\EFI\FEDORA\SHIM.EFI0000424f    
Boot0004* UEFI:CD/DVD Drive     BBS(129,,0x0)    
Boot0005* UEFI:Removable Device BBS(130,,0x0)    
Boot0006* UEFI:Network Device   BBS(131,,0x0)  
```  
  
Comprobamos que windows sea el de mayor prioridad  
```sh  
$ efibootmgr      
BootCurrent: 0002    
Timeout: 1 seconds    
BootOrder: 0000    
Boot0000* Windows Boot Manager  HD(1,GPT,64025f92-2885-411a-bc74-a7e1a22    
6287d,0x800,0x32000)/\EFI\MICROSOFT\BOOT\BOOTMGFW.EFI57494e444f575300010    
0000088000000780000004200430044004f0042004a004500430054003d007b003900640    
06500610038003600320063002d0035006300640064002d0034006500370030002d00610    
06300630031002d006600330032006200330034003400640034003700390035007d00000    
064000100000010000000040000007fff0400    
Boot0002* Fedora        HD(1,GPT,64025f92-2885-411a-bc74-a7e1a226287d,0x    
800,0x32000)/\EFI\FEDORA\SHIMX64.EFI    
Boot0003* Fedora        HD(1,GPT,64025f92-2885-411a-bc74-a7e1a226287d,0x    
800,0x32000)/\EFI\FEDORA\SHIM.EFI0000424f    
Boot0004* UEFI:CD/DVD Drive     BBS(129,,0x0)    
Boot0005* UEFI:Removable Device BBS(130,,0x0)    
Boot0006* UEFI:Network Device   BBS(131,,0x0)  
```  
## 4. Eliminar el /boot/ la carpeta de la distribución  
Entramos como super usuario (root)  
```sh  
sudo -i  
```  
Nos vamos al directorio EFI  
```sh  
cd /boot/efi/EFI/  
```  
Vemos con un ls  
```sh  
ls    
Boot  fedora  Microsoft  
```  
Eliminamos la distribución  
```sh  
rm -rf fedora  
```  
Revisamos con ls  
```sh  
ls    
Boot  Microsoft  
```  
# Nos vamos a Windows y borramos la partición
Se le da en eliminar volumen (no borra la partición solo borra los datos)
