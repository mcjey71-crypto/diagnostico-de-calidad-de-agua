# Sistema Híbrido de Diagnóstico de Calidad del Agua

Proyecto Integrador — Ciencia de Datos Ambientales (UTEC). Combina un pipeline de Machine
Learning (Gradient Boosting + imputación con Random Forest) con validación normativa contra
ECA (DS N° 004-2017-MINAM), MINSA (DS N° 031-2010-SA), OMS (GDWQ 2022) y EPA (NPDWR/SMCL 2024).

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `PROYECTO_CDA_G3.ipynb` | Notebook completo (11 secciones): EDA, imputación, modelado, validación normativa y exportación del dashboard. |
| `dashboard.html` | Dashboard interactivo autocontenible (HTML/CSS/JS, sin dependencias de backend) con los resultados del modelo. |
| `modelo_agua.pkl`, `imputer_agua.pkl`, `features_agua.txt` | Artefactos exportados por el notebook (pipeline entrenado). |

## Publicar el dashboard en GitHub Pages

1. Sube este repositorio a GitHub (o usa uno existente).
2. Copia o renombra `dashboard.html` a `index.html` en la raíz del repo — o déjalo en una
   carpeta `/docs` (en ese caso selecciona esa carpeta en el paso 4).
3. Haz commit y push de los archivos.
4. En GitHub: **Settings → Pages → Build and deployment → Source** → elige la rama `main`
   y la carpeta `/ (root)` (o `/docs`) → **Save**.
5. En 1-2 minutos, GitHub publicará el sitio en:
   `https://<tu-usuario>.github.io/<tu-repositorio>/`

## Regenerar el dashboard

El notebook incluye una sección final ("11. Dashboard Interactivo") que reconstruye
`dashboard.html` a partir de las variables ya calculadas en las secciones anteriores
(accuracy, AUC-ROC, matriz de confusión, importancia de variables, marco normativo). Basta
con ejecutar el notebook de principio a fin en Google Colab; al llegar a esa sección se
generará y descargará el archivo automáticamente.
