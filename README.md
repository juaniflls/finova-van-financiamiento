# FINOVA — VAN con Financiamiento

> Aplicación web interactiva para evaluar proyectos de inversión con financiamiento bancario mediante **Valor Actual Neto (VAN)**, amortización, TIR y análisis de sensibilidad.

![Versión](https://img.shields.io/badge/versión-1.0.0-153b9b)
![HTML](https://img.shields.io/badge/app-HTML%20autónomo-16b9d4)
![Jupyter](https://img.shields.io/badge/notebook-Jupyter-f37626)
![Licencia](https://img.shields.io/badge/licencia-MIT-0e9f6e)

## ¿Qué es FINOVA?

**FINOVA** es un pequeño proyecto académico de modelación financiera que convierte un ejercicio tradicional de VAN con financiamiento en una herramienta interactiva de decisión.

En lugar de limitarse a una hoja de cálculo, permite modificar los supuestos del proyecto y observar inmediatamente cómo cambian la viabilidad, el servicio de la deuda y los principales indicadores.

El objetivo es sencillo: **hacer visibles los números antes de tomar una decisión de inversión**.

## Funcionalidades

- Evaluación de **VAN con financiamiento bancario**.
- Ingresos y gastos editables por año.
- Inversión inicial y costo de fondos configurables.
- Porcentaje financiado, tasa bancaria, plazo y periodicidad.
- Cuota nivelada mediante **sistema francés**.
- Separación de cada cuota entre **interés y amortización de capital**.
- TIR del flujo ajustado.
- Payback descontado.
- Tabla anual de amortización.
- Auditoría completa del cálculo del VAN.
- Matriz de sensibilidad de ingresos y gastos.
- Puntos de equilibrio:
  - ingresos;
  - gastos;
  - tasa bancaria;
  - inversión máxima.
- Recomendaciones cuantitativas para replantear el proyecto.
- **Modo exposición** con introducción, datos, resultado y conclusiones.
- Exportación del escenario a JSON.
- HTML completamente autónomo: no necesita servidor ni dependencias externas.

## Demo rápida

La aplicación principal está en:

```text
index.html
```

Puede abrirse directamente en el navegador.

También se conserva una copia descriptiva en:

```text
app/FINOVA_VAN_Financiamiento_EC300.html
```

## Caso base incluido

El escenario inicial reproduce un ejercicio académico con:

| Variable | Valor |
|---|---:|
| Inversión inicial | ₡5.600.000 |
| Financiamiento | 60% |
| Tasa nominal anual del crédito | 14% |
| Plazo | 4 años |
| Periodicidad | Mensual |
| Tasa de descuento / costo de fondos | 20% |

El modelo permite reemplazar completamente estos valores por los de otro proyecto.

## Metodología

La lógica principal implementada es:

```text
Flujo neto_t = Ingresos_t − Gastos_t

Monto financiado = Inversión × % de financiamiento

Cuota periódica = P × i / [1 − (1+i)^(-n)]

Flujo de caja_t = Flujo neto_t − Cuotas_t

Flujo ajustado_t = Flujo de caja_t + Capital_t
                  = Flujo neto_t − Interés_t

VP_t = Flujo ajustado_t / (1+k)^t

VAN = − Inversión inicial + Σ VP_t
```

La aplicación mantiene visible cada componente para facilitar la revisión y la explicación del procedimiento.

La metodología completa se encuentra en [`docs/METODOLOGIA.md`](docs/METODOLOGIA.md).

## Estructura del repositorio

```text
FINOVA/
├── index.html
├── README.md
├── LICENSE
├── CITATION.cff
├── CHANGELOG.md
├── CONTRIBUTING.md
├── requirements.txt
├── .gitignore
├── app/
│   └── FINOVA_VAN_Financiamiento_EC300.html
├── notebooks/
│   └── FINOVA_VAN_Financiamiento_EC300.ipynb
├── docs/
│   ├── METODOLOGIA.md
│   ├── PUBLICAR_EN_GITHUB.md
│   └── GITHUB_METADATA.md
└── .github/
    └── ISSUE_TEMPLATE/
```

## Ejecutar el notebook

El notebook documenta la lógica matemática y puede regenerar la aplicación HTML.

### Opción 1 — JupyterLab

```bash
pip install -r requirements.txt
jupyter lab
```

Luego abra:

```text
notebooks/FINOVA_VAN_Financiamiento_EC300.ipynb
```

### Opción 2 — Solo usar la app

No necesita instalar nada. Abra `index.html`.

## Publicarlo con GitHub Pages

FINOVA puede funcionar como un sitio estático gratuito.

1. Cree un repositorio en GitHub.
2. Suba **el contenido de esta carpeta**, no el ZIP como un único archivo.
3. Abra **Settings → Pages**.
4. En **Build and deployment**, seleccione **Deploy from a branch**.
5. Seleccione la rama `main` y la carpeta `/ (root)`.
6. Guarde.

GitHub publicará automáticamente `index.html`.

Hay una guía más detallada en [`docs/PUBLICAR_EN_GITHUB.md`](docs/PUBLICAR_EN_GITHUB.md).

## Contexto académico

FINOVA nació como una forma de transformar un ejercicio de evaluación de proyectos con financiamiento bancario en una herramienta tecnológica más clara, reproducible e interactiva.

Fue desarrollado en el contexto del curso **EC-300 — Herramientas Tecnológicas Aplicadas**, Universidad Fidélitas.

Este repositorio contiene únicamente el software y documentación propia del proyecto; **no distribuye presentaciones, transcripciones ni materiales privados del curso**.

## Autor

**Juan Ignacio Garbanzo Fallas**  
Economía · Universidad Fidélitas

## Alcance

FINOVA es una herramienta académica y demostrativa. Un VAN positivo no constituye una garantía de éxito y un VAN negativo no sustituye un análisis empresarial completo.

La calidad del resultado depende de los supuestos utilizados. Para decisiones reales pueden ser necesarios, entre otros:

- impuestos;
- inflación;
- capital de trabajo;
- valor residual;
- depreciación;
- riesgo;
- variabilidad de precios y cantidades;
- costos regulatorios;
- escenarios probabilísticos.

## Licencia

Este proyecto se distribuye bajo la licencia **MIT**. Consulte [`LICENSE`](LICENSE).

---

**FINOVA**  
*De la hoja de cálculo a una decisión financiera explicable.*
