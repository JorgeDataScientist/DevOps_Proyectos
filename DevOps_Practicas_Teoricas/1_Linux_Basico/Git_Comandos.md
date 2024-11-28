
---

# Comandos Básicos de Git y GitHub: Guía Ampliada para Principiantes

Esta guía está diseñada para introducirte en el uso básico de Git y GitHub, herramientas esenciales para el control de versiones y la colaboración en proyectos de desarrollo de software. Git te permite gestionar el historial de cambios de tu código, mientras que GitHub te ofrece una plataforma en línea para alojar tus repositorios y colaborar con otros desarrolladores. A lo largo de esta guía, aprenderás los comandos fundamentales de Git, cómo trabajar con ramas, sincronizar tu trabajo con GitHub, y gestionar cambios en tus proyectos de manera eficiente. Los ejemplos proporcionados te ayudarán a comprender cómo usar Git en tu flujo de trabajo diario.


## 1. Configuración Inicial

### **`git config`**
Configura la información del usuario que se usará para los commits. Esto asegura que cada cambio realizado sea registrado con tu nombre y correo.

**Ejemplo:**
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu.email@example.com"
```

**Detalles:**
- La opción `--global` aplica esta configuración a todos los repositorios en tu máquina.
- Puedes configurarlo para un proyecto específico omitiendo `--global`.

**Ejercicio:**
1. Configura tu nombre y correo para un proyecto local.
2. Verifica la configuración con:
   ```bash
   git config --list
   ```

---

## 2. Crear y Clonar Repositorios

### **`git init`**
Inicializa un repositorio Git en el directorio actual. Este comando crea una carpeta `.git` para almacenar el historial del proyecto.

**Ejemplo:**
```bash
mkdir mi_proyecto
cd mi_proyecto
git init
```

**Ejercicio:**
1. Crea una carpeta `prueba_git` y dentro de ella inicializa un repositorio Git.
2. Confirma que se creó el repositorio usando:
   ```bash
   ls -la
   ```

---

### **`git clone`**
Clona un repositorio remoto en tu máquina local.

**Ejemplo:**
```bash
git clone https://github.com/usuario/repositorio.git
```

**Detalles:**
- Crea una copia completa, incluyendo el historial de commits.
- Útil para colaborar en proyectos existentes.

**Ejercicio:**
1. Clona cualquier repositorio público de GitHub (por ejemplo, un repositorio de prueba).

---

## 3. Trabajar con Cambios

### **`git add`**
Añade archivos al área de preparación para incluirlos en el próximo commit.

**Ejemplo:**
Añadir un archivo específico:
```bash
git add archivo.txt
```

Añadir todos los cambios:
```bash
git add .
```

**Ejercicio:**
1. Crea un archivo `notas.txt`.
2. Añádelo al área de preparación y verifica con:
   ```bash
   git status
   ```

---

### **`git commit`**
Crea un commit con los archivos añadidos al área de preparación. Los commits son puntos de control en el historial del proyecto.

**Ejemplo:**
```bash
git commit -m "Añadido archivo de notas"
```

**Detalles:**
- El mensaje debe describir claramente el cambio realizado.
- Usa `git commit -a -m "Mensaje"` para añadir y commitear en un solo paso.

---

### **`git status`**
Muestra el estado del repositorio: archivos modificados, en staging o no rastreados.

**Ejemplo:**
```bash
git status
```

**Ejercicio:**
1. Modifica el archivo `notas.txt`.
2. Observa el estado antes y después de usar `git add`.

---

### **`git log`**
Muestra el historial de commits.

**Ejemplo:**
```bash
git log
```

**Detalles:**
- Usa `git log --oneline` para un resumen más compacto.

---

## 4. Trabajar con Ramas

### **`git branch`**
Gestiona las ramas en el repositorio.

**Ejemplo:**
Listar ramas:
```bash
git branch
```

Crear una nueva rama:
```bash
git branch nueva-rama
```

---

### **`git checkout`**
Cambia de rama o crea una nueva.

**Ejemplo:**
Cambiar de rama:
```bash
git checkout nombre-rama
```

Crear y cambiar a una nueva:
```bash
git checkout -b nueva-rama
```

**Ejercicio:**
1. Crea una rama llamada `experimentacion`.
2. Cambia entre ramas usando `git checkout`.

---

## 5. Sincronización con Repositorios Remotos

### **`git push`**
Envía los commits locales a un repositorio remoto.

**Ejemplo:**
```bash
git push origin nombre-rama
```

**Detalles:**
- Asegúrate de estar en la rama correcta antes de usar este comando.
- La primera vez puede ser necesario usar `git push -u origin nombre-rama`.

---

### **`git pull`**
Descarga y fusiona cambios desde el repositorio remoto.

**Ejemplo:**
```bash
git pull origin main
```

**Ejercicio:**
1. Realiza cambios en el repositorio remoto (desde GitHub) y luego sincronízalos con tu local usando `git pull`.

---

## 6. Ejercicios Prácticos Finales

### **Estructuración y Gestión:**
1. Crea un proyecto llamado `blog`.
2. Inicializa un repositorio Git en él.
3. Añade un archivo `index.html` y crea un commit.
4. Crea una rama `estilo`, modifica `index.html` y haz un commit.
5. Fusiona los cambios de la rama `estilo` a `main`.

---

### **Colaboración:**
1. Clona un repositorio público.
2. Crea una rama, realiza cambios y súbelos con `git push`.
3. Crea un *pull request* desde GitHub para que revisen tus cambios.

---

### **Avanzado:**
1. Etiqueta el commit inicial como `v1.0` usando:
   ```bash
   git tag -a v1.0 -m "Versión inicial"
   git push origin v1.0
   ```
2. Usa `git revert` para deshacer el último commit sin eliminarlo del historial.

---
