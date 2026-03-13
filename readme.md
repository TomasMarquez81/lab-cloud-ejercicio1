## Despliegue manual en GitHub Pages ejercicio 1

### 1. Creo la build del proyecto

Genero la carpeta `dist` con los archivos estáticos listos para producción:

```bash
npm run build
```

### 2. Subo el proyecto a GitHub

Inicializo el repositorio y subo el código a la rama `main`:

```bash
git init
git add .
git commit -m "first commit"
git remote add origin https://github.com/TomasMarquez81/lab-cloud-ejercicio1.git
git push -u origin main
```

### 3. Preparo la rama `gh-pages`

Creo la rama `gh-pages` y me pongo en ella.

Elimino todos los archivos **excepto** la carpeta `dist`, muevo su contenido a la raíz del repositorio y realizo el push:

```bash
git add .
git commit -m "upload dist files"
git push -u origin gh-pages
```

### 4. Se activa GitHub Actions

Una vez subida la rama `gh-pages`, GitHub Actions detectará los cambios y ejecutará automáticamente el workflow encargado de publicar el proyecto en GitHub Pages.

Y listo tengo mi proyecto listo para que se pueda ver

https://tomasmarquez81.github.io/lab-cloud-ejercicio1/
