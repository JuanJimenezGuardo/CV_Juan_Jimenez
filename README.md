# 📄 Juan José Jiménez Guardo — Curriculum Vitae

<p align="center">
  <img alt="LaTeX" src="https://img.shields.io/badge/LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white">
  <img alt="XeLaTeX" src="https://img.shields.io/badge/Compilador-XeLaTeX-blue?style=for-the-badge">
  <img alt="ATS Friendly" src="https://img.shields.io/badge/Formato-Harvard%20%2F%20ATS--Friendly-success?style=for-the-badge">
  <img alt="moderncv" src="https://img.shields.io/badge/Clase-moderncv%20%7C%20banking-9cf?style=for-the-badge">
  <img alt="Estructura" src="https://img.shields.io/badge/Estructura-Modular-orange?style=for-the-badge">
  <img alt="Idioma" src="https://img.shields.io/badge/Idioma-Español-informational?style=for-the-badge">
</p>

Bienvenido al repositorio de mi Curriculum Vitae. Este CV está estructurado bajo el estándar
**Harvard / ATS-friendly** y diseñado íntegramente en código **LaTeX**, para garantizar una
presentación limpia, profesional y legible por los sistemas de selección automáticos (ATS)
que usa la industria tecnológica.

> **¿Por qué sin fotografía?** El formato Harvard y el estilo `banking` de `moderncv` omiten
> intencionalmente la foto: reduce el sesgo en la selección y evita que el parser del ATS
> falle al procesar el documento.

---

## 🗂️ Estructura modular del proyecto

El repositorio **ya no es un único archivo monolítico**. El CV está dividido en módulos: el
preámbulo y los datos de contacto viven en `main.tex`, y cada sección es un archivo
independiente dentro de `src/`. Editar la experiencia no obliga a abrir el resto del documento,
y los diffs de Git quedan acotados a la sección que realmente cambió.

```
.
├── main.tex              # ⬅️ ESTE ES EL ARCHIVO A COMPILAR
│                         #    Preámbulo, datos de contacto y orden de las secciones
├── src/
│   ├── perfil.tex        # Perfil profesional
│   ├── experiencia.tex   # Experiencia profesional (COTECMAR)
│   ├── educacion.tex     # Formación académica y certificaciones
│   ├── habilidades.tex   # Competencias técnicas
│   ├── proyectos.tex     # Proyectos destacados
│   └── idiomas.tex       # Idiomas
├── .gitignore            # Excluye los artefactos de compilación de LaTeX
└── README.md
```

> ⚠️ **Compila siempre `main.tex`.** Los archivos de `src/` son fragmentos: no contienen
> preámbulo ni `\begin{document}`, así que por separado no compilan. `main.tex` los ensambla
> mediante `\input{}`.

**Para reordenar o silenciar una sección**, mueve o comenta su línea `\input{}` en `main.tex`.
**Para añadir una sección nueva**, crea el archivo en `src/` y agrega su `\input{}` en el orden
deseado.

---

## 🧩 Un perfil híbrido: Ingeniería + Negocio

Mi diferencial no está en un solo lado de la mesa, sino en la bisagra entre los dos:

| Dimensión de Ingeniería | Dimensión de Negocio |
|---|---|
| Diseño del modelo relacional (ERD), normalización e integridad transaccional | Levantamiento de reglas de negocio innegociables con las áreas operativas |
| Arquitectura de integración entre sistemas (orquestador ↔ ERP maestro) | Entendimiento del flujo real de un astillero: construcción, reparación, ETO |
| Desarrollo backend y frontend (Laravel, Vue 3, Inertia) | Definición de indicadores de gestión que la operación sí puede sostener |
| Documentación técnica y versionada del esquema | Gestión ágil con stakeholders (Scrum, victorias tempranas, MVP acotado) |

La consecuencia práctica: no traduzco requerimientos, los **cuestiono** antes de convertirlos
en esquema. Varias de las decisiones que documenté en producción nacieron de detectar que lo
que se pedía contradecía la realidad operativa del negocio.

---

## 🚀 Tecnologías y herramientas destacadas en mi CV

| Área | Detalle |
|---|---|
| **Arquitectura** | Modelado de datos (ERD), diccionarios de datos, Mermaid.js, diseño transaccional |
| **Backend** | PHP 8, Laravel 10, Eloquent ORM, APIs REST |
| **Frontend** | Vue 3, Inertia.js, Vite, Tailwind CSS |
| **Bases de datos** | MySQL, SQL Server, SQL avanzado, normalización |
| **Ecosistema corporativo** | SAP ERP (MM / PS), lógica de industria naval (ETO, grafos, SWBS) |
| **Metodologías** | Scrum, levantamiento de requerimientos, gestión de proyectos TI |

---

## 🛠️ Cómo compilar este CV

### Opción 1 — Overleaf (recomendada)

1. Crea un nuevo proyecto vacío en [Overleaf](https://www.overleaf.com/) (`New Project → Blank Project`).
2. Sube **todo el repositorio**, conservando la carpeta `src/`. La vía más simple es
   `New Project → Upload Project` con un ZIP del repo, o importarlo directamente desde GitHub.
3. En `Menu → Compiler`, selecciona **XeLaTeX** (o LuaLaTeX). Es obligatorio para renderizar
   la fuente *Noto Sans* mediante `fontspec`; con `pdfLaTeX` falla.
4. En `Menu → Main document`, confirma que esté seleccionado **`main.tex`**.
5. Pulsa `Recompile` y descarga el PDF.

### Opción 2 — Entorno local

> ✅ **Compilación verificada.** La versión actual compila sin errores ni advertencias con
> XeLaTeX (TeX Live 2023) y produce un PDF de **una sola página**.

Necesitas una distribución de TeX con `moderncv` y la fuente *Noto Sans*. En Debian/Ubuntu:

```bash
sudo apt install texlive-xetex texlive-latex-extra texlive-fonts-extra \
                 texlive-fonts-recommended texlive-lang-spanish fonts-noto-core
```

Luego, desde la raíz del repositorio:

```bash
xelatex main.tex
```

Si prefieres LuaLaTeX:

```bash
lualatex main.tex
```

### Solución de problemas

| Error | Causa y solución |
|---|---|
| `File 'fontawesome5.sty' not found` | El estilo `banking` de `moderncv` usa iconos de FontAwesome. Instala `texlive-fonts-extra` |
| `File 'moderncv.cls' not found` | Falta `texlive-latex-extra` |
| `I can't find file 'pzdr'` / `Font \XeTeXLink@font=pzdr ... not loadable` | Falta la métrica ZapfDingbats que usa `hyperref`. Instala `texlive-fonts-recommended` |
| `Option clash for package hyperref` | `moderncv` ya carga `hyperref`; no lo declares con `\usepackage`. Configúralo con `\hypersetup` dentro de `\AtBeginDocument{}`, como hace `main.tex` |
| `Font "Noto Sans" not found` | Instala `fonts-noto-core`, o cambia `\setmainfont{Noto Sans}` en `main.tex` por `Lato`, `Open Sans` o `Carlito` |
| `Unknown option "spanish" for package polyglossia` | Reemplaza la línea de `polyglossia` por `\usepackage[spanish,es-nodecimaldot]{babel}` |
| `The fontspec package requires XeTeX or LuaTeX` | Estás compilando con `pdflatex`; cambia el compilador |
| `File 'src/experiencia.tex' not found` | Estás compilando desde otra carpeta, o subiste solo `main.tex` sin la carpeta `src/` |

---

## 📫 Contacto

- **Email:** juanjimenezg207@gmail.com
- **LinkedIn:** [Añade aquí tu URL de LinkedIn]
- **GitHub:** [@JuanJimenezGuardo](https://github.com/JuanJimenezGuardo)

---

<p align="center">
  <sub>Diseñado con enfoque en Arquitectura de Software y Soluciones de Negocio.</sub>
</p>
