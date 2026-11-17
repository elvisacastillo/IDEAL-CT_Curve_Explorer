# IDEAL-CT Curve Explorer

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

**Author / Autor:** Dr. Elvis A. Castillo-Camarena
Universidad Tecnológica de Panamá (UTP) — Facultad de Ingeniería Civil

**Live app / Aplicación en línea:** https://USUARIO.github.io/REPOSITORIO/
<!-- Replace USUARIO and REPOSITORIO with your GitHub user and repository name. -->

[English](#english) · [Español](#español)

---

## English

### What it is

The **IDEAL-CT Curve Explorer** is an interactive web application to explore, fit and
interpret IDEAL-CT load–displacement curves and the cracking tolerance index
(CT<sub>index</sub>) defined in ASTM D8225.

The standard ASTM D8225 procedure is ideal for routine acceptance, but it works on discrete
data points and cannot answer "what-if" questions such as *how would CT<sub>index</sub> change
if the peak load were 10% higher, or if the drop after the peak were gentler?* The Curve
Explorer represents the whole curve with a smooth shape controlled by four parameters with
direct engineering meaning (peak load, displacement at peak, and the steepness of the rise
before the peak and of the decay after it) and recalculates every ASTM D8225 quantity
instantly as they change.

It is useful for **teaching**, **laboratory analysis** and **mix screening**.

> The Curve Explorer complements, and does not replace, the standard ASTM D8225 procedure,
> which remains the reference for acceptance testing.

### Main features

- **Drag-to-shape:** drag the peak (red), the rise marker (green) or the decay marker
  (purple) directly on the curve, or use the sliders. P<sub>75</sub>, l<sub>75</sub>,
  |m<sub>75</sub>|, W<sub>f</sub>, G<sub>f</sub> and CT<sub>index</sub> update in real time.
- **Import and fit:** load a test record from `.xlsx`, `.xls` or `.csv`, choose the sheet and
  the load/displacement columns, and press **Optimize** to fit the curve to the data.
- **Comparison with ASTM D8225:** with data loaded, the standard ASTM D8225 parameters are also
  computed directly from the raw record and shown next to the model values.
- **Parameter-space view:** plot any pair of P, d, P<sub>75</sub>, l<sub>75</sub>,
  |m<sub>75</sub>|, W<sub>f</sub>, G<sub>f</sub> and CT<sub>index</sub> and follow the
  trajectory as the curve changes.
- **Variable springs and live equation:** each variable of the CT<sub>index</sub> equation
  glows green when it increases and red when it decreases.
- **Report:** save a self-contained HTML report (project, specimen, model and ASTM results,
  plot) that can be printed to PDF from the browser.

### How to use

1. Open the app in any modern browser (desktop, tablet or phone).
2. Enter the specimen diameter *D* and thickness *t* (150 mm and 62 mm by default).
3. Shape the curve by dragging the markers, or click **Import .xlsx / .csv** and then
   **Optimize** to fit your data.
4. Review the results on the plot, type the project and specimen names, and click
   **Save report**.

**Data format:** two numeric columns, load in **kN** and displacement in **mm**, on any sheet
(columns are selected when importing). CSV files may use commas, semicolons or tabs as
separators. Header rows and non-numeric cells are skipped automatically.

**Privacy:** files are read and processed entirely inside your browser; no data is uploaded
to any server.

### Running locally

Download `index_interactive.html` and open it with a double-click; no installation or server
is needed. An internet connection is required to load the two libraries the app uses from
public CDNs: [Plotly.js](https://plotly.com/javascript/) 2.35.2 and
[SheetJS](https://sheetjs.com/) 0.18.5.

### Repository contents

| File | Description |
|---|---|
| `index.html` | Home page (bilingual EN/ES) describing the application |
| `index_interactive.html` | The IDEAL-CT Curve Explorer application (single, self-contained file) |
| `README.md` | This file |
| `LICENSE` | License terms (CC BY 4.0) |

### Publishing on GitHub Pages

1. Push these files to the root of the repository's `main` branch.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and
   `/ (root)`, and save.
4. After a minute the site is available at `https://USUARIO.github.io/REPOSITORIO/`.

### License and attribution

© 2026 Elvis A. Castillo-Camarena and Universidad Tecnológica de Panamá (UTP).

This application is released under the
[Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
You are free to **use, share and adapt** it, for any purpose, including commercially,
**provided you give credit to the authors of the application, Dr. Elvis A. Castillo-Camarena
and the Universidad Tecnológica de Panamá (UTP)**, include a link to the license, and indicate
whether changes were made. See [`LICENSE`](LICENSE) for details.

Suggested credit line:

> IDEAL-CT Curve Explorer — Dr. Elvis A. Castillo-Camarena, Universidad Tecnológica de Panamá
> (UTP). Licensed under CC BY 4.0.

### How to cite

If you use the application in a course, thesis, report or publication, please cite it as:

> Castillo-Camarena, E. A. (2026). *IDEAL-CT Curve Explorer* [Web application].
> Universidad Tecnológica de Panamá. https://USUARIO.github.io/REPOSITORIO/

```bibtex
@misc{castillocamarena2026idealct,
  author       = {Castillo-Camarena, Elvis A.},
  title        = {{IDEAL-CT Curve Explorer}},
  year         = {2026},
  howpublished = {Web application, Universidad Tecnol{\'o}gica de Panam{\'a}},
  url          = {https://USUARIO.github.io/REPOSITORIO/}
}
```

---

## Español

### Qué es

El **IDEAL-CT Curve Explorer** es una aplicación web interactiva para explorar, ajustar e
interpretar curvas carga–desplazamiento del ensayo IDEAL-CT y el índice de tolerancia al
agrietamiento (CT<sub>index</sub>) definido en la norma ASTM D8225.

El procedimiento estándar de la ASTM D8225 es ideal para la aceptación rutinaria, pero trabaja
sobre puntos discretos y no responde preguntas como *¿cuánto cambiaría el CT<sub>index</sub> si
la carga pico fuera un 10% mayor, o si la caída después del pico fuera más suave?* El Curve
Explorer representa la curva completa con una forma suave controlada por cuatro parámetros con
significado ingenieril directo (carga pico, desplazamiento en el pico y qué tan pronunciados son
el ascenso antes del pico y el descenso después de él) y recalcula al instante todas las
cantidades de la ASTM D8225 a medida que estos cambian.

Es útil para **docencia**, **análisis de laboratorio** y **evaluación de mezclas**.

> El Curve Explorer complementa, y no reemplaza, el procedimiento estándar de la ASTM D8225,
> que sigue siendo la referencia para los ensayos de aceptación.

### Funciones principales

- **Modelado por arrastre:** arrastra el pico (rojo), el marcador de ascenso (verde) o el de
  descenso (morado) directamente sobre la curva, o usa los deslizadores. P<sub>75</sub>,
  l<sub>75</sub>, |m<sub>75</sub>|, W<sub>f</sub>, G<sub>f</sub> y CT<sub>index</sub> se
  actualizan en tiempo real.
- **Importación y ajuste:** carga el registro de un ensayo desde `.xlsx`, `.xls` o `.csv`,
  elige la hoja y las columnas de carga y desplazamiento, y presiona **Optimize** para ajustar
  la curva a los datos.
- **Comparación con la ASTM D8225:** con datos cargados, también se calculan los parámetros
  estándar de la ASTM D8225 directamente del registro original y se muestran junto a los del
  modelo.
- **Espacio de parámetros:** grafica cualquier par entre P, d, P<sub>75</sub>, l<sub>75</sub>,
  |m<sub>75</sub>|, W<sub>f</sub>, G<sub>f</sub> y CT<sub>index</sub> y sigue la trayectoria al
  modificar la curva.
- **Resortes y ecuación en vivo:** cada variable de la ecuación del CT<sub>index</sub> se
  ilumina en verde cuando aumenta y en rojo cuando disminuye.
- **Reporte:** guarda un reporte HTML autocontenido (proyecto, probeta, resultados del modelo y
  de la ASTM, gráfica) que puede imprimirse a PDF desde el navegador.

### Cómo usarla

1. Abre la aplicación en cualquier navegador moderno (computadora, tableta o teléfono).
2. Ingresa el diámetro *D* y el espesor *t* de la probeta (150 mm y 62 mm por defecto).
3. Modela la curva arrastrando los marcadores, o haz clic en **Import .xlsx / .csv** y luego
   en **Optimize** para ajustar tus datos.
4. Revisa los resultados en la gráfica, escribe el nombre del proyecto y de la probeta, y haz
   clic en **Save report**.

**Formato de datos:** dos columnas numéricas, carga en **kN** y desplazamiento en **mm**, en
cualquier hoja (las columnas se eligen al importar). Los CSV pueden usar comas, punto y coma o
tabuladores como separadores. Las filas de encabezado y las celdas no numéricas se omiten
automáticamente.

**Privacidad:** los archivos se leen y procesan completamente dentro del navegador; ningún dato
se envía a un servidor.

### Uso local

Descarga `index_interactive.html` y ábrelo con doble clic; no requiere instalación ni servidor.
Se necesita conexión a internet para cargar las dos librerías que usa la aplicación desde CDN
públicos: [Plotly.js](https://plotly.com/javascript/) 2.35.2 y [SheetJS](https://sheetjs.com/)
0.18.5.

### Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `index.html` | Página de inicio (bilingüe EN/ES) que describe la aplicación |
| `index_interactive.html` | La aplicación IDEAL-CT Curve Explorer (un solo archivo autocontenido) |
| `README.md` | Este archivo |
| `LICENSE` | Términos de la licencia (CC BY 4.0) |

### Publicación en GitHub Pages

1. Sube estos archivos a la raíz de la rama `main` del repositorio.
2. En el repositorio, ve a **Settings → Pages**.
3. En **Build and deployment**, elige **Deploy from a branch**, selecciona `main` y
   `/ (root)`, y guarda.
4. Al cabo de un minuto el sitio estará disponible en `https://USUARIO.github.io/REPOSITORIO/`.

### Licencia y atribución

© 2026 Elvis A. Castillo-Camarena y Universidad Tecnológica de Panamá (UTP).

Esta aplicación se distribuye bajo la licencia
[Creative Commons Atribución 4.0 Internacional (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.es).
Puedes **usarla, compartirla y adaptarla** con cualquier propósito, incluso comercial,
**siempre que des crédito a los autores de la aplicación, el Dr. Elvis A. Castillo-Camarena y
la Universidad Tecnológica de Panamá (UTP)**, incluyas un enlace a la licencia e indiques si
realizaste cambios. Consulta el archivo [`LICENSE`](LICENSE) para más detalles.

Texto de crédito sugerido:

> IDEAL-CT Curve Explorer — Dr. Elvis A. Castillo-Camarena, Universidad Tecnológica de Panamá
> (UTP). Licencia CC BY 4.0.

### Cómo citarla

Si usas la aplicación en un curso, tesis, informe o publicación, por favor cítala así:

> Castillo-Camarena, E. A. (2026). *IDEAL-CT Curve Explorer* [Aplicación web].
> Universidad Tecnológica de Panamá. https://USUARIO.github.io/REPOSITORIO/
