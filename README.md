# 📄 Juan José Jiménez Guardo — Curriculum Vitae

<p align="center">
  <img alt="LaTeX" src="https://img.shields.io/badge/LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white">
  <img alt="XeLaTeX" src="https://img.shields.io/badge/Compilador-XeLaTeX-blue?style=for-the-badge">
  <img alt="ATS Friendly" src="https://img.shields.io/badge/Formato-Harvard%20%2F%20ATS--Friendly-success?style=for-the-badge">
  <img alt="moderncv" src="https://img.shields.io/badge/Clase-moderncv%20%7C%20banking-9cf?style=for-the-badge">
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

## 👨‍💻 Sobre mi perfil

Soy **Estudiante de Ingeniería de Sistemas** a punto de graduarme, enfocado en el
**Análisis Funcional**, la **Arquitectura de Software** y la **Integración de Sistemas (ERP/SAP)**.

Me especializo en actuar como el puente estratégico entre las necesidades operativas complejas
(entornos industriales, manufactura ETO) y los equipos de desarrollo de software bajo
metodologías ágiles (Scrum). No me limito a codificar: diseño la arquitectura relacional y
orquesto las reglas de negocio para que la tecnología genere impacto real.

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

Este repositorio contiene el código fuente para generar el CV en PDF.

### Opción 1 — Overleaf (recomendada)

1. Crea un nuevo proyecto vacío en [Overleaf](https://www.overleaf.com/) (`New Project → Blank Project`).
2. Sube el archivo `CV_Juan_Jimenez.tex` de este repositorio (`Upload`).
3. **Importante:** abre `Menu → Compiler` y selecciona **XeLaTeX** (o LuaLaTeX). Es obligatorio
   para renderizar la fuente *Noto Sans* mediante el paquete `fontspec`; con `pdfLaTeX` falla.
4. Pulsa `Recompile` y descarga el PDF.

### Opción 2 — Entorno local

Necesitas una distribución completa de TeX (TeX Live o MiKTeX) y la fuente *Noto Sans*
instalada en el sistema.

```bash
xelatex CV_Juan_Jimenez.tex
```

Si prefieres LuaLaTeX:

```bash
lualatex CV_Juan_Jimenez.tex
```

En Debian/Ubuntu, las dependencias se instalan así:

```bash
sudo apt install texlive-xetex texlive-latex-extra texlive-lang-spanish fonts-noto
```

### Solución de problemas

| Error | Solución |
|---|---|
| `Font "Noto Sans" not found` | Instala la fuente, o cambia `\setmainfont{Noto Sans}` por `Lato`, `Open Sans` o `Carlito` |
| `Unknown option "spanish" for package polyglossia` | Reemplaza la línea de `polyglossia` por `\usepackage[spanish,es-nodecimaldot]{babel}` |
| `fontspec error: The fontspec package requires XeTeX or LuaTeX` | Estás compilando con `pdflatex`; cambia el compilador |
| Acentos mal renderizados | Mismo caso anterior: el compilador no es XeLaTeX/LuaLaTeX |

---

## 📫 Contacto

- **Email:** juanjimenezg207@gmail.com
- **LinkedIn:** [Añade aquí tu URL de LinkedIn]
- **GitHub:** [@JuanJimenezGuardo](https://github.com/JuanJimenezGuardo)

---

<p align="center">
  <sub>Diseñado con enfoque en Arquitectura de Software y Soluciones de Negocio.</sub>
</p>
