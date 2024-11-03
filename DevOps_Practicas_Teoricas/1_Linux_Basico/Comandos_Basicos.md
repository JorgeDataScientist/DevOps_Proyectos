```markdown
# Comandos Básicos de Linux

## Introducción

Este documento proporciona una lista de comandos básicos de Linux junto con ejemplos de uso. Estos comandos son esenciales para navegar y gestionar archivos y procesos en un entorno Linux. Tanto si eres un principiante como si buscas repasar los conceptos fundamentales, esta guía te será de gran utilidad.

## Lista de Comandos

### 1. `pwd` - Print Working Directory
Muestra la ruta del directorio actual.

**Ejemplo:**
```bash
pwd
```

### 2. `ls` - List Directory Contents
Lista los archivos y directorios dentro del directorio actual.

**Ejemplo:**
```bash
ls
```

### 3. `cd` - Change Directory
Cambia de directorio.

**Ejemplo:**
```bash
cd /ruta/del/directorio
```

### 4. `mkdir` - Make Directory
Crea un nuevo directorio.

**Ejemplo:**
```bash
mkdir nuevo_directorio
```

### 5. `rmdir` - Remove Directory
Elimina un directorio vacío.

**Ejemplo:**
```bash
rmdir nombre_del_directorio
```

### 6. `rm` - Remove Files or Directories
Elimina archivos o directorios.

**Ejemplo:**
```bash
rm archivo.txt       # Elimina un archivo
rm -r directorio/    # Elimina un directorio y su contenido
```

### 7. `cp` - Copy Files or Directories
Copia archivos o directorios.

**Ejemplo:**
```bash
cp archivo.txt /ruta/destino/
```

### 8. `mv` - Move or Rename Files or Directories
Mueve o renombra archivos o directorios.

**Ejemplo:**
```bash
mv archivo.txt /ruta/destino/   # Mueve el archivo
mv viejo_nombre.txt nuevo_nombre.txt   # Renombra un archivo
```

### 9. `touch` - Create an Empty File
Crea un archivo vacío.

**Ejemplo:**
```bash
touch archivo.txt
```

### 10. `cat` - Concatenate and Display Files
Muestra el contenido de un archivo.

**Ejemplo:**
```bash
cat archivo.txt
```

### 11. `echo` - Display a Line of Text
Imprime texto en la terminal o en un archivo.

**Ejemplo:**
```bash
echo "Hola, Mundo"
echo "Texto de ejemplo" > archivo.txt   # Escribe en un archivo
```

### 12. `nano` - Simple Text Editor
Abre un editor de texto simple.

**Ejemplo:**
```bash
nano archivo.txt
```

### 13. `sudo` - Superuser Do
Ejecuta un comando con privilegios de superusuario.

**Ejemplo:**
```bash
sudo apt update
```

### 14. `apt` - Advanced Package Tool
Gestiona paquetes en distribuciones basadas en Debian.

**Ejemplo:**
```bash
sudo apt update          # Actualiza la lista de paquetes
sudo apt install nombre_paquete   # Instala un paquete
```

### 15. `df` - Disk Free
Muestra el uso del espacio en disco.

**Ejemplo:**
```bash
df -h
```

### 16. `du` - Disk Usage
Muestra el uso del espacio por archivos y directorios.

**Ejemplo:**
```bash
du -h nombre_del_directorio/
```

### 17. `top` - Task Manager
Muestra los procesos en ejecución y el uso de recursos.

**Ejemplo:**
```bash
top
```

### 18. `ps` - Process Status
Muestra una lista de los procesos actuales.

**Ejemplo:**
```bash
ps aux
```

### 19. `kill` - Terminate Processes
Termina un proceso por su PID.

**Ejemplo:**
```bash
kill 1234   # Termina el proceso con PID 1234
```

### 20. `chmod` - Change File Permissions
Cambia los permisos de un archivo o directorio.

**Ejemplo:**
```bash
chmod 755 archivo.sh
```

### 21. `chown` - Change File Owner
Cambia el propietario de un archivo o directorio.

**Ejemplo:**
```bash
sudo chown usuario:grupo archivo.txt
```

### 22. `find` - Search for Files
Busca archivos y directorios.

**Ejemplo:**
```bash
find /ruta/de/busqueda -name archivo.txt
```

### 23. `grep` - Search Text
Busca texto dentro de archivos.

**Ejemplo:**
```bash
grep "cadena_de_texto" archivo.txt
```

### 24. `man` - Manual Pages
Muestra el manual de usuario de un comando.

**Ejemplo:**
```bash
man ls
```

### 25. `history` - Command History
Muestra el historial de comandos ejecutados.

**Ejemplo:**
```bash
history
```

### 26. `clear` - Clear Terminal
Limpia la terminal.

**Ejemplo:**
```bash
clear
```

### 27. `exit` - Exit Terminal
Cierra la terminal.

**Ejemplo:**
```bash
exit
```

```markdown
### 28. `wget` - Download Files from the Web
Descarga archivos desde la web.

**Ejemplo:**
```bash
wget http://ejemplo.com/archivo.zip
```

### 29. `curl` - Transfer Data from or to a Server
Envía o recibe datos desde un servidor.

**Ejemplo:**
```bash
curl http://ejemplo.com
```
Descargar un archivo:
```bash
curl -O http://ejemplo.com/archivo.zip
```

### 30. `tar` - Archive Files
Crea y extrae archivos tar.

**Ejemplo:**
```bash
tar -cvf archivo.tar directorio/   # Crea un archivo tar
tar -xvf archivo.tar               # Extrae un archivo tar
```

### 31. `gzip` - Compress Files
Comprime archivos en formato .gz.

**Ejemplo:**
```bash
gzip archivo.txt
```

### 32. `gunzip` - Decompress Files
Descomprime archivos .gz.

**Ejemplo:**
```bash
gunzip archivo.txt.gz
```

### 33. `zip` - Compress Files into a Zip Archive
Crea archivos comprimidos en formato .zip.

**Ejemplo:**
```bash
zip archivo.zip archivo1.txt archivo2.txt
```

### 34. `unzip` - Extract Zip Files
Extrae archivos comprimidos en formato .zip.

**Ejemplo:**
```bash
unzip archivo.zip
```

### 35. `scp` - Secure Copy
Copia archivos entre hosts de forma segura.

**Ejemplo:**
```bash
scp archivo.txt usuario@servidor:/ruta/destino/
```

### 36. `ssh` - Secure Shell
Accede a un servidor de forma segura mediante una conexión SSH.

**Ejemplo:**
```bash
ssh usuario@servidor
```

### 37. `ping` - Check Network Connectivity
Verifica la conectividad de red hacia un host.

**Ejemplo:**
```bash
ping ejemplo.com
```

### 38. `ifconfig` - Configure a Network Interface
Muestra o configura interfaces de red.

**Ejemplo:**
```bash
ifconfig
```

### 39. `hostname` - Show or Set the System's Hostname
Muestra o establece el nombre del host del sistema.

**Ejemplo:**
```bash
hostname
```

### 40. `uptime` - Show How Long the System Has Been Running
Muestra el tiempo que el sistema ha estado funcionando.

**Ejemplo:**
```bash
uptime
```

### 41. `whoami` - Show Current User
Muestra el nombre del usuario actual.

**Ejemplo:**
```bash
whoami
```

### 42. `uname` - Show System Information
Muestra información del sistema.

**Ejemplo:**
```bash
uname -a   # Muestra toda la información disponible
```

### 43. `df` - Display Disk Space Usage
Muestra el uso del espacio en disco de las particiones.

**Ejemplo:**
```bash
df -h
```

### 44. `du` - Display Directory Space Usage
Muestra el uso del espacio en disco por archivos y directorios.

**Ejemplo:**
```bash
du -sh directorio/
```

### 45. `free` - Display Memory Usage
Muestra la cantidad de memoria libre y usada en el sistema.

**Ejemplo:**
```bash
free -h
```

### 46. `mount` - Mount a Filesystem
Monta un sistema de archivos.

**Ejemplo:**
```bash
mount /dev/sdX /mnt
```

### 47. `umount` - Unmount a Filesystem
Desmonta un sistema de archivos.

**Ejemplo:**
```bash
umount /mnt
```

### 48. `alias` - Create a Shortcut for a Command
Crea un alias para un comando.

**Ejemplo:**
```bash
alias ll='ls -la'
```

### 49. `unalias` - Remove an Alias
Elimina un alias creado.

**Ejemplo:**
```bash
unalias ll
```

### 50. `df` - Report File System Disk Space Usage
Muestra el uso de espacio en disco de los sistemas de archivos.

**Ejemplo:**
```bash
df -h
```

### 51. `uptime` - Show How Long the System Has Been Running
Muestra el tiempo que el sistema ha estado en funcionamiento y la carga del sistema.

**Ejemplo:**
```bash
uptime
```

### 52. `last` - Show Last Logins
Muestra la lista de los últimos usuarios que iniciaron sesión.

**Ejemplo:**
```bash
last
```

### 53. `useradd` - Add a User
Añade un nuevo usuario al sistema.

**Ejemplo:**
```bash
sudo useradd nuevo_usuario
```

### 54. `passwd` - Change User Password
Cambia la contraseña de un usuario.

**Ejemplo:**
```bash
passwd usuario
```

### 55. `userdel` - Delete a User
Elimina un usuario del sistema.

**Ejemplo:**
```bash
sudo userdel usuario
```

### 56. `groupadd` - Add a Group
Crea un nuevo grupo en el sistema.

**Ejemplo:**
```bash
sudo groupadd nuevo_grupo
```

### 57. `groupdel` - Delete a Group
Elimina un grupo del sistema.

**Ejemplo:**
```bash
sudo groupdel grupo
```

### 58. `usermod` - Modify a User Account
Modifica los detalles de una cuenta de usuario.

**Ejemplo:**
```bash
sudo usermod -aG grupo usuario   # Añadir usuario a un grupo
```

### 59. `crontab` - Schedule Tasks
Programa tareas para que se ejecuten en intervalos específicos.

**Ejemplo:**
```bash
crontab -e
```

### 60. `service` - Manage System Services
Administra servicios del sistema.

**Ejemplo:**
```bash
sudo service nombre_del_servicio start   # Inicia un servicio
sudo service nombre_del_servicio stop    # Detiene un servicio
```