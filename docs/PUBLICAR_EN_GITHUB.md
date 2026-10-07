# Publicar FINOVA en GitHub

## Nombre recomendado del repositorio

```text
finova-van-financiamiento
```

También puede utilizar simplemente:

```text
FINOVA
```

## 1. Crear el repositorio

En GitHub:

1. Seleccione **New repository**.
2. Escriba el nombre del repositorio.
3. Descripción recomendada:

> Aplicación web interactiva para evaluar proyectos de inversión con financiamiento bancario mediante VAN, TIR, amortización y análisis de sensibilidad.

4. Seleccione **Public**.
5. No marque “Add a README”, porque este paquete ya incluye uno.
6. Cree el repositorio.

## 2. Subir los archivos desde la web

Descomprima `FINOVA-GitHub-Ready.zip`.

En el repositorio nuevo:

1. **Add file → Upload files**.
2. Arrastre **todo el contenido dentro de la carpeta `FINOVA-GitHub`**.
3. Verifique que `README.md` e `index.html` queden en la raíz.
4. Commit recomendado:

```text
Initial release: FINOVA v1.0.0
```

## 3. Opción con Git

```bash
git init
git add .
git commit -m "Initial release: FINOVA v1.0.0"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/finova-van-financiamiento.git
git push -u origin main
```

## 4. Activar GitHub Pages

Como FINOVA es una aplicación estática, GitHub Pages puede publicarla directamente.

1. Abra **Settings**.
2. Entre a **Pages**.
3. En **Build and deployment** seleccione:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
4. Guarde.

La dirección tendrá esta forma:

```text
https://TU-USUARIO.github.io/finova-van-financiamiento/
```

## 5. Configurar la ficha del repositorio

En la portada del repositorio, junto a **About**, seleccione el ícono de configuración y añada:

### Website

La dirección de GitHub Pages.

### Topics recomendados

```text
finance
npv
van
irr
tir
financial-modeling
project-evaluation
economics
jupyter-notebook
javascript
education
```

## 6. Release v1.0.0

Cuando el repositorio esté listo:

1. Abra **Releases**.
2. Seleccione **Draft a new release**.
3. Tag:

```text
v1.0.0
```

4. Título:

```text
FINOVA v1.0.0 — Primera versión pública
```

5. Texto sugerido:

> Primera versión pública de FINOVA, una aplicación académica e interactiva para evaluar proyectos de inversión con financiamiento bancario. Incluye VAN, TIR, amortización, payback descontado, puntos de equilibrio, análisis de sensibilidad y un modo de exposición.

## 7. Qué NO subir

No incluya:

- transcripciones de clases;
- presentaciones del profesor;
- documentos internos del curso;
- archivos `.ipynb_checkpoints`;
- carpetas `__MACOSX`;
- archivos temporales del sistema.

Este paquete ya fue limpiado para evitar esos elementos.
