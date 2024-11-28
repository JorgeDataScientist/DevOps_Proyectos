
```markdown
# Comandos Básicos Ampliados  

## Introducción  

Esta guía ampliada proporciona una descripción detallada de comandos básicos de Linux, incluyendo ejemplos prácticos, contexto de uso, y ejercicios para aplicar en escenarios reales. Está diseñada para principiantes que quieren entender Linux y para profesionales que buscan profundizar en su uso en tareas de administración de sistemas y DevOps.  

## Tabla de Contenidos  
1. Gestión de Archivos y Directorios  
2. Gestión de Procesos  
3. Conexión y Diagnóstico de Red  
4. Manipulación Avanzada con Redirección y Tuberías  
5. Comandos Esenciales para DevOps  
6. Ejercicios Prácticos  
7. Recursos Adicionales  

---

## 1. Gestión de Archivos y Directorios  

Esta sección cubre los comandos esenciales para navegar y administrar archivos y directorios en un sistema Linux.

### Lista de Comandos  

1. **`pwd` - Print Working Directory**  
   Muestra la ruta completa del directorio actual en el que te encuentras.  

2. **`ls` - List Directory Contents**  
   Lista los archivos y directorios contenidos en el directorio actual o en una ubicación especificada.  
   - Opciones comunes:  
     - `-l`: Muestra los archivos en formato detallado.  
     - `-a`: Incluye archivos ocultos en la lista.  

3. **`cd` - Change Directory**  
   Cambia el directorio actual a una ubicación específica.  
   - Ejemplo:  
     ```bash
     cd /ruta/del/directorio
     cd ..  # Sube un nivel en la jerarquía de directorios
     ```  

4. **`mkdir` - Make Directory**  
   Crea un nuevo directorio vacío en la ubicación especificada.  
   - Ejemplo:  
     ```bash
     mkdir nuevo_directorio
     ```  

5. **`rmdir` - Remove Directory**  
   Elimina un directorio vacío.  
   - Ejemplo:  
     ```bash
     rmdir nombre_del_directorio
     ```  

6. **`rm` - Remove Files or Directories**  
   Elimina archivos o directorios.  
   - Opciones comunes:  
     - `-r`: Elimina directorios de forma recursiva.  
     - `-f`: Fuerza la eliminación sin confirmación.  

7. **`cp` - Copy Files or Directories**  
   Copia archivos o directorios de una ubicación a otra.  
   - Opciones comunes:  
     - `-r`: Copia directorios de forma recursiva.  

8. **`mv` - Move or Rename Files or Directories**  
   Mueve archivos o directorios a otra ubicación o los renombra.  
   - Ejemplo:  
     ```bash
     mv archivo.txt /ruta/destino/
     mv viejo_nombre.txt nuevo_nombre.txt
     ```  

9. **`touch` - Create an Empty File**  
   Crea un archivo vacío o actualiza la fecha de modificación de un archivo existente.  
   - Ejemplo:  
     ```bash
     touch archivo.txt
     ```  

### Nota  
Estos comandos son fundamentales para interactuar con el sistema de archivos en Linux. Es recomendable practicar su uso en un entorno seguro para evitar eliminar datos accidentalmente.  


Aquí tienes una versión mejorada y ampliada, pensada para ser clara y útil para principiantes que están aprendiendo Linux:

```markdown
# Guía de Comandos y Ejercicios de Linux para Principiantes  

Este documento te guiará paso a paso en el aprendizaje de los comandos básicos de Linux y su aplicación práctica mediante ejercicios y ejemplos detallados.

---

## 1. Gestión de Archivos y Directorios  

### Lista de Comandos  

1. **`pwd` - Mostrar Directorio Actual**  
   Muestra la ruta completa del directorio en el que te encuentras actualmente.  

2. **`ls` - Listar Contenido del Directorio**  
   Lista los archivos y carpetas del directorio actual o de una ruta específica.  
   - Opciones comunes:  
     - `-l`: Muestra detalles como permisos, propietario y tamaño.  
     - `-a`: Incluye archivos ocultos.  

3. **`cd` - Cambiar de Directorio**  
   Cambia tu ubicación actual a otro directorio.  
   - Ejemplo:  
     ```bash
     cd /home/usuario/documentos
     cd ..  # Subir un nivel
     cd ~   # Ir al directorio personal
     ```  

4. **`mkdir` - Crear un Directorio**  
   Crea una nueva carpeta vacía.  
   - Ejemplo:  
     ```bash
     mkdir proyectos
     ```  

5. **`rmdir` - Eliminar Directorios Vacíos**  
   Elimina una carpeta, siempre que esté vacía.  
   - Ejemplo:  
     ```bash
     rmdir carpeta_vacia
     ```  

6. **`rm` - Eliminar Archivos o Directorios**  
   Elimina archivos o carpetas.  
   - Opciones comunes:  
     - `-r`: Elimina carpetas y su contenido de forma recursiva.  
     - `-f`: Fuerza la eliminación sin confirmación.  
   - Ejemplo:  
     ```bash
     rm archivo.txt
     rm -rf carpeta_no_vacia
     ```  

7. **`cp` - Copiar Archivos o Directorios**  
   Copia archivos o carpetas de un lugar a otro.  
   - Ejemplo:  
     ```bash
     cp archivo.txt copia_archivo.txt
     cp -r carpeta_original carpeta_copia
     ```  

8. **`mv` - Mover o Renombrar Archivos o Directorios**  
   Mueve archivos a otra ubicación o cambia su nombre.  
   - Ejemplo:  
     ```bash
     mv archivo.txt /nueva/ruta/
     mv archivo.txt archivo_renombrado.txt
     ```  

9. **`touch` - Crear un Archivo Vacío**  
   Crea un archivo vacío o actualiza la fecha de modificación de uno existente.  
   - Ejemplo:  
     ```bash
     touch archivo_nuevo.txt
     ```  

### Ejemplo Ampliado:  

```bash
mkdir proyecto
cd proyecto
touch archivo.txt
ls -la
mv archivo.txt archivo_renombrado.txt
rm archivo_renombrado.txt
```  

### Ejercicio Guiado  

1. Crea una estructura de carpetas como esta:  
   ```
   proyectos/
   ├── cliente1/
   └── cliente2/
   ```  

   Comando sugerido:  
   ```bash
   mkdir -p proyectos/cliente1 proyectos/cliente2
   ```  

2. Dentro de cada carpeta, crea un archivo vacío llamado `datos.txt` utilizando `touch`.  

3. Copia el archivo `datos.txt` de la carpeta `cliente1` a la carpeta `cliente2`.  

   Comando sugerido:  
   ```bash
   cp proyectos/cliente1/datos.txt proyectos/cliente2/
   ```  

4. Lista los contenidos de ambas carpetas para verificar los cambios.  

---

## 2. Gestión de Procesos  

### Comandos Clave  

1. **`top` - Monitoreo de Procesos**  
   Muestra los procesos en ejecución en tiempo real, ordenados por uso de recursos.  

2. **`ps` - Mostrar Procesos**  
   Muestra una lista de procesos activos.  
   - Ejemplo:  
     ```bash
     ps aux  # Lista todos los procesos con detalles
     ps aux | grep "nombre_proceso"  # Filtra por un proceso específico
     ```  

3. **`kill` - Terminar Procesos**  
   Detiene un proceso utilizando su PID (Identificador del Proceso).  
   - Ejemplo:  
     ```bash
     kill 1234  # Termina el proceso con PID 1234
     kill -9 1234  # Fuerza la terminación
     ```  

### Ejemplo Ampliado:  

```bash
top
ps aux | grep "nombre_proceso"
kill 1234
```  

### Ejercicio Guiado  

1. Usa `top` para identificar el proceso que más CPU consume.  

2. Encuentra su PID con `ps aux`.  

3. Detén ese proceso utilizando `kill`.  

---

## 3. Conexión y Diagnóstico de Red  

### Comandos Clave  

1. **`ping`**  
   Verifica la conectividad con una dirección o dominio.  
   - Ejemplo:  
     ```bash
     ping google.com
     ```  

2. **`curl` y `wget`**  
   Descarga archivos desde servidores web.  
   - Ejemplo con `wget`:  
     ```bash
     wget http://servidor.com/archivo.zip
     ```  

3. **`ssh`**  
   Conéctate a otro servidor de manera remota.  
   - Ejemplo:  
     ```bash
     ssh usuario@servidor
     ```  

### Ejercicio Guiado  

1. Conéctate a un servidor remoto usando `ssh`.  

2. Verifica la versión del sistema operativo en el servidor remoto:  
   ```bash
   uname -a
   ```  
---

Aquí tienes una versión ampliada con más ejercicios detallados para cada sección. Estos ejercicios están diseñados para ser más prácticos y comprensibles para principiantes, pero también pueden retar a quienes ya tienen algo de experiencia.

---

### **1. Gestión de Archivos y Directorios**  

#### Ejercicios Ampliados  

1. **Crea una Estructura Compleja de Directorios:**  
   Diseña esta estructura de carpetas:  
   ```
   empresa/
   ├── finanzas/
   │   ├── informes/
   │   └── presupuestos/
   ├── marketing/
   └── recursos_humanos/
       └── contratos/
   ```  
   **Instrucciones:**  
   - Usa `mkdir` con la opción `-p` para crear todas las carpetas de una sola vez.  
   - Comando sugerido:  
     ```bash
     mkdir -p empresa/finanzas/informes empresa/finanzas/presupuestos empresa/marketing empresa/recursos_humanos/contratos
     ```  

2. **Gestión de Archivos en la Estructura Creada:**  
   - Crea un archivo vacío llamado `reporte_anual.txt` en `finanzas/informes`.  
   - Copia este archivo a `finanzas/presupuestos` y renómbralo como `reporte_presupuesto.txt`.  
   - Lista el contenido de ambas carpetas para verificar los cambios.  
     ```bash
     touch empresa/finanzas/informes/reporte_anual.txt
     cp empresa/finanzas/informes/reporte_anual.txt empresa/finanzas/presupuestos/reporte_presupuesto.txt
     ls empresa/finanzas/informes
     ls empresa/finanzas/presupuestos
     ```  

3. **Limpieza y Reorganización:**  
   - Elimina la carpeta `marketing` y todo su contenido.  
   - Mueve `empresa/recursos_humanos/contratos` a `empresa/finanzas/`.  
     ```bash
     rm -rf empresa/marketing
     mv empresa/recursos_humanos/contratos empresa/finanzas/
     ```  

---

### **2. Gestión de Procesos**  

#### Ejercicios Ampliados  

1. **Identificación de Procesos Activos:**  
   - Usa `top` para encontrar el proceso que más memoria consume.  
   - Anota el PID del proceso y confirma su detalle con `ps`.  
     ```bash
     ps aux | grep <PID>
     ```  

2. **Crea un Proceso en Segundo Plano:**  
   - Ejecuta este comando en segundo plano:  
     ```bash
     sleep 300 &
     ```  
   - Verifica que el proceso está corriendo con `jobs` o `ps`.  
   - Detén el proceso usando `kill` con su PID.  
     ```bash
     jobs
     kill <PID>
     ```  

3. **Termina un Proceso con Forzado:**  
   - Busca un proceso relacionado con el navegador (`firefox`, por ejemplo):  
     ```bash
     ps aux | grep firefox
     ```  
   - Termina el proceso con `kill -9`.  
     ```bash
     kill -9 <PID>
     ```  

---

### **3. Conexión y Diagnóstico de Red**  

#### Ejercicios Ampliados  

1. **Diagnóstico de Red con `ping`:**  
   - Realiza un `ping` a un sitio web de tu elección (ejemplo: `google.com`) para verificar conectividad.  
   - Cancela el `ping` después de 10 segundos con `Ctrl+C`.  

2. **Descarga un Archivo con `wget`:**  
   - Descarga el archivo de ejemplo:  
     ```bash
     wget https://www.example.com/sample.txt
     ```  
   - Verifica que el archivo fue descargado con `ls`.  

3. **Conexión Remota con `ssh`:**  
   - Conéctate a un servidor remoto (reemplaza `usuario` y `servidor`):  
     ```bash
     ssh usuario@servidor
     ```  
   - Ejecuta el comando `uptime` en el servidor remoto para verificar su estado.  
   - Sal de la sesión con `exit`.  

4. **Simula una Descarga con `curl`:**  
   - Descarga el contenido de una página web:  
     ```bash
     curl https://www.example.com -o pagina.html
     ```  
   - Abre el archivo `pagina.html` en un editor de texto para verificar su contenido.  

---

### **4. Redirección y Tuberías**  

#### Ejercicios Ampliados  

1. **Redirección de Salidas a un Archivo:**  
   - Guarda el listado de archivos de tu directorio personal en un archivo llamado `archivos.txt`:  
     ```bash
     ls -la ~ > archivos.txt
     ```  
   - Añade una línea personalizada al final del archivo:  
     ```bash
     echo "Lista generada el: $(date)" >> archivos.txt
     ```  

2. **Búsqueda con `grep` y Tuberías:**  
   - Busca la palabra "ERROR" en un archivo de registro llamado `registro.log` y guarda los resultados en `errores.log`:  
     ```bash
     cat registro.log | grep "ERROR" > errores.log
     ```  

3. **Filtrado y Ordenación de Datos:**  
   - Filtra las líneas de un archivo que contengan el número "404" y ordénalas alfabéticamente:  
     ```bash
     grep "404" registro.log | sort > errores_ordenados.txt
     ```  

---

### **5. Comandos Esenciales para DevOps**  

#### Ejercicios Ampliados  

1. **Gestión de Contenedores con `docker`:**  
   - Lista los contenedores activos:  
     ```bash
     docker ps
     ```  
   - Crea e inicia un contenedor con la imagen `nginx`:  
     ```bash
     docker run -d -p 8080:80 nginx
     ```  
   - Detén el contenedor con su ID o nombre:  
     ```bash
     docker stop <ID_contenedor>
     ```  

2. **Programación de Tareas con `crontab`:**  
   - Programa un script que registre el uso de disco cada 10 minutos:  
     - Abre el editor de tareas programadas:  
       ```bash
       crontab -e
       ```  
     - Añade la siguiente línea:  
       ```bash
       */10 * * * * df -h > ~/uso_disco.txt
       ```  

3. **Monitoreo de Servicios con `systemctl`:**  
   - Verifica el estado del servicio `nginx`:  
     ```bash
     systemctl status nginx
     ```  
   - Detén el servicio:  
     ```bash
     systemctl stop nginx
     ```  
   - Inicia nuevamente el servicio:  
     ```bash
     systemctl start nginx
     ```  

---

### **6. Proyectos Finales**  

1. **Automatización Completa:**  
   - Escribe un script llamado `backup.sh` que:  
     - Comprima un directorio llamado `proyecto` en un archivo `.tar.gz`.  
     - Use la fecha actual como nombre del archivo.  
     - Guarde el archivo en `/backups`.  
     - **Script sugerido:**  
       ```bash
       #!/bin/bash
       mkdir -p /backups
       tar -czvf /backups/proyecto_$(date +%F).tar.gz proyecto
       echo "Respaldo creado en /backups"
       ```  

2. **Monitoreo en Tiempo Real:**  
   - Usa `htop` o `top` para monitorear los procesos que consumen más del 10% de CPU.  
   - Usa `kill` para terminar manualmente los procesos innecesarios.  

---

Aquí tienes una versión ampliada con más ejercicios detallados para cada sección. Estos ejercicios están diseñados para ser más prácticos y comprensibles para principiantes, pero también pueden retar a quienes ya tienen algo de experiencia.

---
---
---
### **1. Gestión de Archivos y Directorios**  

#### Ejercicios Ampliados  

1. **Crea una Estructura Compleja de Directorios:**  
   Diseña esta estructura de carpetas:  
   ```
   empresa/
   ├── finanzas/
   │   ├── informes/
   │   └── presupuestos/
   ├── marketing/
   └── recursos_humanos/
       └── contratos/
   ```  
   **Instrucciones:**  
   - Usa `mkdir` con la opción `-p` para crear todas las carpetas de una sola vez.  
   - Comando sugerido:  
     ```bash
     mkdir -p empresa/finanzas/informes empresa/finanzas/presupuestos empresa/marketing empresa/recursos_humanos/contratos
     ```  

2. **Gestión de Archivos en la Estructura Creada:**  
   - Crea un archivo vacío llamado `reporte_anual.txt` en `finanzas/informes`.  
   - Copia este archivo a `finanzas/presupuestos` y renómbralo como `reporte_presupuesto.txt`.  
   - Lista el contenido de ambas carpetas para verificar los cambios.  
     ```bash
     touch empresa/finanzas/informes/reporte_anual.txt
     cp empresa/finanzas/informes/reporte_anual.txt empresa/finanzas/presupuestos/reporte_presupuesto.txt
     ls empresa/finanzas/informes
     ls empresa/finanzas/presupuestos
     ```  

3. **Limpieza y Reorganización:**  
   - Elimina la carpeta `marketing` y todo su contenido.  
   - Mueve `empresa/recursos_humanos/contratos` a `empresa/finanzas/`.  
     ```bash
     rm -rf empresa/marketing
     mv empresa/recursos_humanos/contratos empresa/finanzas/
     ```  

---

### **2. Gestión de Procesos**  

#### Ejercicios Ampliados  

1. **Identificación de Procesos Activos:**  
   - Usa `top` para encontrar el proceso que más memoria consume.  
   - Anota el PID del proceso y confirma su detalle con `ps`.  
     ```bash
     ps aux | grep <PID>
     ```  

2. **Crea un Proceso en Segundo Plano:**  
   - Ejecuta este comando en segundo plano:  
     ```bash
     sleep 300 &
     ```  
   - Verifica que el proceso está corriendo con `jobs` o `ps`.  
   - Detén el proceso usando `kill` con su PID.  
     ```bash
     jobs
     kill <PID>
     ```  

3. **Termina un Proceso con Forzado:**  
   - Busca un proceso relacionado con el navegador (`firefox`, por ejemplo):  
     ```bash
     ps aux | grep firefox
     ```  
   - Termina el proceso con `kill -9`.  
     ```bash
     kill -9 <PID>
     ```  

---

### **3. Conexión y Diagnóstico de Red**  

#### Ejercicios Ampliados  

1. **Diagnóstico de Red con `ping`:**  
   - Realiza un `ping` a un sitio web de tu elección (ejemplo: `google.com`) para verificar conectividad.  
   - Cancela el `ping` después de 10 segundos con `Ctrl+C`.  

2. **Descarga un Archivo con `wget`:**  
   - Descarga el archivo de ejemplo:  
     ```bash
     wget https://www.example.com/sample.txt
     ```  
   - Verifica que el archivo fue descargado con `ls`.  

3. **Conexión Remota con `ssh`:**  
   - Conéctate a un servidor remoto (reemplaza `usuario` y `servidor`):  
     ```bash
     ssh usuario@servidor
     ```  
   - Ejecuta el comando `uptime` en el servidor remoto para verificar su estado.  
   - Sal de la sesión con `exit`.  

4. **Simula una Descarga con `curl`:**  
   - Descarga el contenido de una página web:  
     ```bash
     curl https://www.example.com -o pagina.html
     ```  
   - Abre el archivo `pagina.html` en un editor de texto para verificar su contenido.  

---

### **4. Redirección y Tuberías**  

#### Ejercicios Ampliados  

1. **Redirección de Salidas a un Archivo:**  
   - Guarda el listado de archivos de tu directorio personal en un archivo llamado `archivos.txt`:  
     ```bash
     ls -la ~ > archivos.txt
     ```  
   - Añade una línea personalizada al final del archivo:  
     ```bash
     echo "Lista generada el: $(date)" >> archivos.txt
     ```  

2. **Búsqueda con `grep` y Tuberías:**  
   - Busca la palabra "ERROR" en un archivo de registro llamado `registro.log` y guarda los resultados en `errores.log`:  
     ```bash
     cat registro.log | grep "ERROR" > errores.log
     ```  

3. **Filtrado y Ordenación de Datos:**  
   - Filtra las líneas de un archivo que contengan el número "404" y ordénalas alfabéticamente:  
     ```bash
     grep "404" registro.log | sort > errores_ordenados.txt
     ```  

---

### **5. Comandos Esenciales para DevOps**  

#### Ejercicios Ampliados  

1. **Gestión de Contenedores con `docker`:**  
   - Lista los contenedores activos:  
     ```bash
     docker ps
     ```  
   - Crea e inicia un contenedor con la imagen `nginx`:  
     ```bash
     docker run -d -p 8080:80 nginx
     ```  
   - Detén el contenedor con su ID o nombre:  
     ```bash
     docker stop <ID_contenedor>
     ```  

2. **Programación de Tareas con `crontab`:**  
   - Programa un script que registre el uso de disco cada 10 minutos:  
     - Abre el editor de tareas programadas:  
       ```bash
       crontab -e
       ```  
     - Añade la siguiente línea:  
       ```bash
       */10 * * * * df -h > ~/uso_disco.txt
       ```  

3. **Monitoreo de Servicios con `systemctl`:**  
   - Verifica el estado del servicio `nginx`:  
     ```bash
     systemctl status nginx
     ```  
   - Detén el servicio:  
     ```bash
     systemctl stop nginx
     ```  
   - Inicia nuevamente el servicio:  
     ```bash
     systemctl start nginx
     ```  

---

### **6. Proyectos Finales**  

1. **Automatización Completa:**  
   - Escribe un script llamado `backup.sh` que:  
     - Comprima un directorio llamado `proyecto` en un archivo `.tar.gz`.  
     - Use la fecha actual como nombre del archivo.  
     - Guarde el archivo en `/backups`.  
     - **Script sugerido:**  
       ```bash
       #!/bin/bash
       mkdir -p /backups
       tar -czvf /backups/proyecto_$(date +%F).tar.gz proyecto
       echo "Respaldo creado en /backups"
       ```  

2. **Monitoreo en Tiempo Real:**  
   - Usa `htop` o `top` para monitorear los procesos que consumen más del 10% de CPU.  
   - Usa `kill` para terminar manualmente los procesos innecesarios.  

---
