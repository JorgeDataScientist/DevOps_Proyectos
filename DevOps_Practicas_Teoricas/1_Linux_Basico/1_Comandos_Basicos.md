
```markdown
# Comandos Básicos de Linux

## Introducción

Linux es un sistema operativo robusto y versátil ampliamente utilizado en entornos de desarrollo, servidores y sistemas de producción. Dominar sus comandos básicos es esencial para cualquier profesional de tecnología, especialmente en DevOps, donde la gestión eficiente de sistemas y procesos es clave. 

Este documento proporciona una referencia práctica de comandos básicos de Linux, explicados con ejemplos para facilitar su comprensión y uso. Ya sea que estés comenzando o reforzando tus habilidades, aquí encontrarás herramientas fundamentales para interactuar con el sistema operativo, gestionar archivos, administrar procesos y optimizar tareas.

---

## Lista de Comandos

### Gestión de Archivos y Directorios
1. **`pwd`** - Muestra la ruta del directorio actual.
   ```bash
   pwd
   ```

2. **`ls`** - Lista los archivos y directorios.
   ```bash
   ls
   ls -la   # Muestra detalles adicionales como permisos y tamaño
   ```

3. **`cd`** - Cambia de directorio.
   ```bash
   cd /ruta/del/directorio
   cd ..    # Sube un nivel
   ```

4. **`mkdir`** - Crea un nuevo directorio.
   ```bash
   mkdir nuevo_directorio
   ```

5. **`rm`** - Elimina archivos o directorios.
   ```bash
   rm archivo.txt         # Elimina un archivo
   rm -r directorio/      # Elimina un directorio y su contenido
   ```

6. **`cp`** - Copia archivos o directorios.
   ```bash
   cp archivo.txt /ruta/destino/
   cp -r directorio /ruta/destino/   # Copia un directorio y su contenido
   ```

7. **`mv`** - Mueve o renombra archivos o directorios.
   ```bash
   mv archivo.txt /ruta/destino/
   mv viejo_nombre.txt nuevo_nombre.txt
   ```

8. **`find`** - Busca archivos o directorios.
   ```bash
   find /ruta/de/busqueda -name archivo.txt
   ```

---

### Gestión de Usuarios y Permisos
1. **`whoami`** - Muestra el usuario actual.
   ```bash
   whoami
   ```

2. **`chmod`** - Cambia permisos de un archivo.
   ```bash
   chmod 755 script.sh   # Lectura, escritura y ejecución para el propietario; solo lectura y ejecución para otros
   ```

3. **`chown`** - Cambia el propietario de un archivo.
   ```bash
   sudo chown usuario:grupo archivo.txt
   ```

4. **`useradd`** - Añade un nuevo usuario.
   ```bash
   sudo useradd nuevo_usuario
   ```

5. **`passwd`** - Cambia la contraseña de un usuario.
   ```bash
   passwd usuario
   ```

6. **`groupadd`** - Añade un nuevo grupo.
   ```bash
   sudo groupadd nuevo_grupo
   ```

7. **`usermod`** - Modifica la configuración de un usuario.
   ```bash
   sudo usermod -aG grupo usuario   # Añade el usuario a un grupo
   ```

---

### Gestión de Procesos
1. **`top`** - Monitorea los procesos en tiempo real.
   ```bash
   top
   ```

2. **`ps`** - Muestra el estado de los procesos.
   ```bash
   ps aux
   ```

3. **`kill`** - Termina un proceso.
   ```bash
   kill <PID>
   ```

---

### Conexión de Red
1. **`ping`** - Verifica conectividad de red.
   ```bash
   ping ejemplo.com
   ```

2. **`ssh`** - Establece una conexión segura con un servidor.
   ```bash
   ssh usuario@servidor
   ```

3. **`scp`** - Copia archivos entre sistemas de forma segura.
   ```bash
   scp archivo.txt usuario@servidor:/ruta/destino/
   ```

4. **`wget`** - Descarga archivos desde una URL.
   ```bash
   wget http://ejemplo.com/archivo.zip
   ```

5. **`curl`** - Transfiere datos desde o hacia un servidor.
   ```bash
   curl http://ejemplo.com
   ```

---

### Otros Comandos Útiles
1. **`alias`** - Crea un alias para un comando.
   ```bash
   alias ll='ls -la'
   ```

2. **`df`** - Muestra el uso del disco.
   ```bash
   df -h
   ```

3. **`du`** - Muestra el uso del espacio por archivos.
   ```bash
   du -sh carpeta/
   ```

4. **`uptime`** - Muestra el tiempo que el sistema ha estado funcionando.
   ```bash
   uptime
   ```

5. **`clear`** - Limpia la terminal.
   ```bash
   clear
   ```

6. **`man`** - Accede al manual de un comando.
   ```bash
   man ls
   ```

---

### Sugerencias Adicionales
- Agregar una sección sobre redirección y tuberías (`>`, `>>`, `|`).
- Explicar comandos relacionados con el manejo de logs, como `tail` y `head`.
- Introducir conceptos básicos de scripting en Bash, como variables y estructuras condicionales.

---