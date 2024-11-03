```markdown
### Comandos Básicos para Instalar Paquetes en Ubuntu

#### 1. `apt update`
Actualiza la lista de paquetes disponibles y sus versiones. Es un paso necesario antes de instalar cualquier paquete nuevo.

**Ejemplo:**
```bash
sudo apt update
```

#### 2. `apt upgrade`
Actualiza todos los paquetes instalados a las versiones más recientes disponibles en los repositorios.

**Ejemplo:**
```bash
sudo apt upgrade
```

#### 3. `apt install`
Instala un nuevo paquete desde los repositorios oficiales de Ubuntu.

**Ejemplo:**
```bash
sudo apt install nombre_paquete
```
**Ejemplo instalando `curl`:**
```bash
sudo apt install curl
```

#### 4. `apt remove`
Elimina un paquete instalado, pero deja intactos sus archivos de configuración.

**Ejemplo:**
```bash
sudo apt remove nombre_paquete
```
**Ejemplo eliminando `curl`:**
```bash
sudo apt remove curl
```

#### 5. `apt purge`
Elimina un paquete instalado junto con sus archivos de configuración.

**Ejemplo:**
```bash
sudo apt purge nombre_paquete
```

#### 6. `apt autoremove`
Elimina automáticamente los paquetes que ya no son necesarios, como dependencias que ya no son usadas por ningún otro paquete instalado.

**Ejemplo:**
```bash
sudo apt autoremove
```

#### 7. `apt search`
Busca un paquete en los repositorios de Ubuntu.

**Ejemplo:**
```bash
apt search nombre_paquete
```
**Ejemplo buscando `git`:**
```bash
apt search git
```

#### 8. `apt-cache show`
Muestra detalles sobre un paquete disponible, como su versión, tamaño, dependencias, etc.

**Ejemplo:**
```bash
apt-cache show nombre_paquete
```

#### 9. `dpkg -i`
Instala un paquete `.deb` localmente (no desde los repositorios).

**Ejemplo:**
```bash
sudo dpkg -i paquete.deb
```

#### 10. `dpkg -r`
Elimina un paquete instalado usando `dpkg`.

**Ejemplo:**
```bash
sudo dpkg -r nombre_paquete
```

#### 11. `add-apt-repository`
Añade un repositorio PPA (Personal Package Archive) a tu lista de fuentes de software.

**Ejemplo:**
```bash
sudo add-apt-repository ppa:nombre/ppa
```
**Ejemplo añadiendo el PPA de `git`:**
```bash
sudo add-apt-repository ppa:git-core/ppa
```

```

Puedes usar estos comandos en Ubuntu para instalar, eliminar, y gestionar paquetes en tu sistema.