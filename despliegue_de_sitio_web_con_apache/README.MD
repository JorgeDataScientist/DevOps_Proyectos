
# Guía para Instalar y Desplegar un Sitio Web en Apache

## Introducción

En esta guía, aprenderás a instalar Apache en un sistema basado en Linux (Ubuntu), configurar el servidor y desplegar un sitio web personal. Este sitio incluye archivos HTML, CSS, JavaScript, e imágenes organizados en carpetas específicas. Al final, tendrás un servidor funcional sirviendo tu portafolio personal.

Además, incluimos cómo desinstalar Apache completamente si lo necesitas.

---

## Requisitos Previos

Antes de empezar, asegúrate de contar con lo siguiente:
- Una máquina o servidor con Ubuntu.
- Privilegios de administrador (`sudo`).
- Los archivos de tu sitio web listos para ser desplegados.

---

## Paso 1: Instalación de Apache

### 1.1 Actualizar el sistema

Actualiza la lista de paquetes disponibles para asegurarte de instalar las versiones más recientes:

```bash
sudo apt update
```


### 1.2 Instalar Apache

Instala Apache y sus dependencias con el siguiente comando:

```bash
sudo apt install apache2
```

### 1.3 Activar y Verificar Apache

#### Activar Apache

Inicia el servicio de Apache con:

```bash
sudo systemctl start apache2
```

Habilita Apache para que se inicie automáticamente al encender el sistema:

```bash
sudo systemctl enable apache2
```

#### Verificar que Apache está funcionando

Comprueba que el servicio está activo:

```bash
sudo systemctl status apache2
```

Deberías ver una salida que indique `active (running)`.

#### Probar Apache en el navegador

Abre un navegador e ingresa `http://localhost` si estás en la máquina local, o `http://<tu-direccion-ip>` si es un servidor remoto. Si Apache está funcionando correctamente, verás la página predeterminada: **"Apache2 Ubuntu Default Page"**.

#### Detener y Deshabilitar Apache

Si necesitas detener Apache:

```bash
sudo systemctl stop apache2
```

Para evitar que se inicie automáticamente:

```bash
sudo systemctl disable apache2
```

---

## Paso 2: Preparación de los Archivos del Sitio Web

Organiza los archivos de tu sitio web en la siguiente estructura:

```
/var/www/portafolio
│
├── certificados
│   ├── certificados_ok
│   │   ├── imagen1.png
│   │   ├── imagen2.png
│   └── Portafolio_ok
│       ├── imagen1.png
│       ├── imagen2.png
├── img
│   ├── imagen1.png
│   ├── imagen2.png
├── estilos.css
├── index.html
└── script.js
```

### 2.1 Crear el directorio del sitio web

Crea un directorio en `/var/www/` para almacenar los archivos:

```bash
sudo mkdir -p /var/www/portafolio
```

### 2.2 Subir los archivos al servidor

Si trabajas localmente, copia los archivos directamente al directorio creado:

```bash
sudo cp -r /ruta/a/tu/sitio/* /var/www/portafolio
```

Si los archivos están en tu máquina local y el servidor es remoto, usa `scp`:

```bash
scp -r /ruta/a/tu/sitio/* usuario@servidor:/var/www/portafolio
```

---

## Paso 3: Configuración del Virtual Host en Apache

### 3.1 Crear un archivo de configuración

Crea un archivo de configuración para tu sitio web en `/etc/apache2/sites-available/`:

```bash
sudo nano /etc/apache2/sites-available/portafolio.conf
```

Agrega la siguiente configuración:

```apache
<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/portafolio
    ServerName portafolio.local

    <Directory /var/www/portafolio>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

### 3.2 Habilitar el sitio

Habilita tu sitio web con:

```bash
sudo a2ensite portafolio.conf
```

### 3.3 Deshabilitar el sitio por defecto

Desactiva el sitio predeterminado de Apache para evitar conflictos:

```bash
sudo a2dissite 000-default.conf
```

### 3.4 Recargar Apache

Recarga Apache para aplicar los cambios:

```bash
sudo systemctl reload apache2
```

---

## Paso 4: Configuración de Permisos

Configura los permisos adecuados para los archivos del sitio web:

```bash
sudo chown -R www-data:www-data /var/www/portafolio
sudo chmod -R 755 /var/www/portafolio
```

---

## Paso 5: Acceso al Sitio Web

Abre un navegador y accede a tu sitio ingresando:

- `http://<tu-direccion-ip>/index.html`
- O `http://portafolio.local` si configuraste el archivo `/etc/hosts` para resolver `portafolio.local`.

---

## Paso 6: Desinstalar Apache (Opcional)

Si necesitas eliminar Apache y todos sus contenidos:

### 6.1 Desinstalar Apache

Elimina Apache pero deja los archivos de configuración:

```bash
sudo apt remove apache2
```

Para eliminar Apache y sus archivos de configuración completamente:

```bash
sudo apt purge apache2
```

### 6.2 Eliminar directorios y contenido del sitio web

Si deseas eliminar también los archivos de tu sitio web:

```bash
sudo rm -rf /var/www/portafolio
```

### 6.3 Limpiar dependencias no utilizadas

Finalmente, elimina las dependencias instaladas automáticamente:

```bash
sudo apt autoremove
```

---

## Conclusión

Con esta guía, has aprendido a instalar Apache, configurarlo para servir tu sitio web personal y, en caso necesario, desinstalarlo. Este es un punto de partida básico que puedes extender con configuraciones avanzadas, como seguridad HTTPS o reglas personalizadas.

¡Felicidades por completar tu configuración!
```


## Video de Demostración

A continuación, se incluye una demostración del proyecto:

![Video de Demostración](video_demostracionn.gif)

