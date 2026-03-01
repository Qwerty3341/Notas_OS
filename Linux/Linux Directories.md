# / 
The root directory, contains all the system 
# /boot
Contains the files needled to run the system like the kernel 
# /dev
- Device files
	- Hardware interfaces
	- Drivers
	- Disk partitions
# /etc
Text config files
- EDITABLE
- TEXT
- CONFIGURATION
# /home
Here is where users dwell
# /lib
- Shared code between binaries (bin and sbin)
- Dependencies
# /lib64
- The same of lib but for 64 bits OS
# /lost+found

# /media

# /mnt
Used to mount drives
# /opt
- Contains additional software
- Here we can install programs 
	- For instance obsidian and brave are installed in this directory
# /proc
Is created on memory to keep track of running processes 
# /root
The home directory of the root user
# /run 
A "tmpfs" file system for system packages to place runtime data, socket files, and similar.
# /srv
The place to store general server payload, managed by the administrator
# /sys
A virtual kernel file system exposing discovered devices and other functionality.
# /tmp
- Contains temporal files
- When the system reboots all the files in this directory will be delate
# /usr
## /bin 
- lib: symbolic link to usr/lib
- Contains binaries and executables non essential 
- Installed binaries
## /sbin 
- executables for the root user
# /var
Contains variable files that will change as the OS is been used
- logs
- cashfiles

# /efi
If the boot partition /boot/ is maintained separately from the EFI System Partition (ESP), the latter is mounted here.

---
# Sources
https://www.youtube.com/watch?v=42iQKuQodW4
https://forums.linuxmint.com/viewtopic.php?t=369512

You can use this command to see the description of the directories
```bash
man file-hierarchy
```