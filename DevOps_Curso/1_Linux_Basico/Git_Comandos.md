```markdown
# Comandos Básicos de Git

## Configuración Inicial

### 1. `git config`
Configura la información del usuario que se usará para los commits.

**Ejemplo:**
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu.email@example.com"
```

## Crear y Clonar Repositorios

### 2. `git init`
Inicializa un nuevo repositorio Git en el directorio actual.

**Ejemplo:**
```bash
git init
```

### 3. `git clone`
Clona un repositorio existente desde GitHub (o cualquier otro repositorio remoto).

**Ejemplo:**
```bash
git clone https://github.com/usuario/repositorio.git
```

## Trabajar con Cambios

### 4. `git add`
Añade archivos al área de preparación (staging area) para el próximo commit.

**Ejemplo:**
```bash
git add archivo.txt
```
Añadir todos los archivos modificados:
```bash
git add .
```

### 5. `git commit`
Crea un commit con los archivos añadidos al área de preparación.

**Ejemplo:**
```bash
git commit -m "Mensaje del commit"
```

### 6. `git status`
Muestra el estado actual del repositorio, incluyendo archivos modificados y cambios pendientes.

**Ejemplo:**
```bash
git status
```

### 7. `git diff`
Muestra las diferencias entre los archivos en el área de preparación y el último commit.

**Ejemplo:**
```bash
git diff
```

### 8. `git log`
Muestra el historial de commits del repositorio.

**Ejemplo:**
```bash
git log
```

## Trabajar con Ramas

### 9. `git branch`
Lista las ramas existentes en el repositorio o crea una nueva rama.

**Ejemplo:**
Listar ramas:
```bash
git branch
```
Crear una nueva rama:
```bash
git branch nueva-rama
```

### 10. `git checkout`
Cambia de rama o restaura archivos del repositorio.

**Ejemplo:**
Cambiar de rama:
```bash
git checkout nombre-rama
```
Crear y cambiar a una nueva rama:
```bash
git checkout -b nueva-rama
```

### 11. `git merge`
Combina cambios de una rama en la rama actual.

**Ejemplo:**
```bash
git merge nombre-rama
```

## Sincronización con GitHub

### 12. `git remote`
Gestiona las conexiones remotas del repositorio.

**Ejemplo:**
Listar los remotos:
```bash
git remote -v
```

### 13. `git push`
Envía tus commits locales a un repositorio remoto.

**Ejemplo:**
```bash
git push origin nombre-rama
```

### 14. `git pull`
Descarga cambios del repositorio remoto y los fusiona con tu rama actual.

**Ejemplo:**
```bash
git pull origin nombre-rama
```

### 15. `git fetch`
Descarga cambios del repositorio remoto sin fusionarlos con tu rama actual.

**Ejemplo:**
```bash
git fetch origin
```

### 16. `git clone`
Clona un repositorio remoto en tu máquina local.

**Ejemplo:**
```bash
git clone https://github.com/usuario/repositorio.git
```

### 17. `git remote add`
Añade un nuevo repositorio remoto.

**Ejemplo:**
```bash
git remote add origin https://github.com/usuario/repositorio.git
```

### 18. `git rm`
Elimina archivos del repositorio y del área de preparación.

**Ejemplo:**
```bash
git rm archivo.txt
```

### 19. `git tag`
Crea una etiqueta para un commit específico.

**Ejemplo:**
Crear una etiqueta:
```bash
git tag -a v1.0 -m "Versión 1.0"
```

### 20. `git revert`
Revierte un commit específico sin borrar el historial.

**Ejemplo:**
```bash
git revert <commit-id>
```