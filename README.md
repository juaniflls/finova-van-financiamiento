# FINOVA · Evaluación financiera de proyectos

<p align="center">
  <img src="docs/assets/branding/finova-hero.png" alt="FINOVA hero" width="100%" />
</p>

<p align="center">
  <strong>Aplicación HTML para evaluar proyectos con CAPM, WACC, VAN, TIR, DSCR, escenarios y presentación ejecutiva.</strong>
</p>

<p align="center">
  <img src="docs/assets/branding/finova-social-preview.jpg" alt="Social preview" width="80%" />
</p>

## Descripción general

**FINOVA** es una aplicación de evaluación financiera de proyectos diseñada para convertir supuestos de inversión en una decisión clara y trazable.  
Integra en un solo flujo:

- definición del proyecto,
- proyección de ingresos y gastos,
- estructura de financiamiento,
- cálculo del costo de capital,
- evaluación financiera,
- análisis de escenarios,
- y presentación ejecutiva automática.

La aplicación se entrega como un **archivo HTML independiente**, acompañada por su **notebook de generación** y por un **escenario JSON de ejemplo** listo para abrir desde la interfaz.

---

## Qué incluye este paquete

- `FINOVA_v4.1_Profesional.html` → aplicación lista para usar.
- `FINOVA_v4.1_Profesional.ipynb` → notebook fuente.
- `FINOVA_Ejemplo_Centro_Logistico_Aurora.json` → escenario demostrativo.
- `docs/assets/branding/` → identidad visual y social preview.
- `docs/assets/screenshots/` → capturas organizadas del producto.
- `docs/assets/finova-grid-overview.png` → grilla visual general.
- `docs/assets/finova-grid-before.png` → grilla del estado inicial.
- `docs/assets/finova-grid-demo.png` → grilla del caso cargado.
- `docs/CAMBIOS_FINOVA_v4.md` → registro de cambios.
- `archive/finova-van-financiamiento-original.zip` → zip original de referencia.

---

## Características principales

### 1) Flujo completo en 7 pasos
1. **Proyecto**
2. **Flujos operativos**
3. **Financiamiento**
4. **Costo de capital**
5. **Evaluación**
6. **Escenarios**
7. **Presentación**

### 2) Decisión financiera técnicamente sustentada
FINOVA permite trabajar con:

- **CAPM** para costo de capital propio,
- **WACC** para estructuras mixtas deuda + patrimonio,
- **VAN** como criterio de creación de valor,
- **TIR** como rentabilidad interna,
- **DSCR** como capacidad de pago de deuda,
- **escenarios** para sensibilidad del VAN,
- y una **lectura ejecutiva** automática para exposición.

### 3) Interfaz lista para demostración
La aplicación está pensada para lucir bien en una presentación, clase, demo o repositorio:

- dashboard visual,
- matrices coloreadas,
- composición anual del crédito,
- vista ejecutiva,
- y presentación tipo diapositiva dentro de la misma aplicación.

---

## Vista general del producto

### Grilla principal
<p align="center">
  <img src="docs/assets/finova-grid-overview.png" alt="Grilla visual de FINOVA" width="100%" />
</p>

### Estado inicial de la aplicación
<p align="center">
  <img src="docs/assets/finova-grid-before.png" alt="Estado inicial de FINOVA" width="100%" />
</p>

### Caso cargado y resultados
<p align="center">
  <img src="docs/assets/finova-grid-demo.png" alt="Caso demo cargado en FINOVA" width="100%" />
</p>

---

## Estructura de carpetas

```text
FINOVA-Repo-Final/
├── FINOVA_v4.1_Profesional.html
├── FINOVA_v4.1_Profesional.ipynb
├── FINOVA_Ejemplo_Centro_Logistico_Aurora.json
├── README.md
├── .gitignore
├── archive/
│   └── finova-van-financiamiento-original.zip
└── docs/
    ├── CAMBIOS_FINOVA_v4.md
    └── assets/
        ├── branding/
        │   ├── finova-hero.png
        │   └── finova-social-preview.jpg
        ├── finova-grid-before.png
        ├── finova-grid-demo.png
        ├── finova-grid-overview.png
        └── screenshots/
            ├── before/
            └── after/
```

---

## Cómo usar la aplicación

### Opción 1: abrir la app directamente
1. Descargue o clone el repositorio.
2. Abra `FINOVA_v4.1_Profesional.html` en su navegador.
3. Use la aplicación manualmente o cargue un escenario.

### Opción 2: cargar el caso demostrativo
1. Abra `FINOVA_v4.1_Profesional.html`.
2. Pulse **Abrir**.
3. Seleccione `FINOVA_Ejemplo_Centro_Logistico_Aurora.json`.
4. Revise los pasos 1 a 4.
5. En **Costo de capital**, pulse **Calcular y evaluar**.
6. Explore:
   - **Evaluación**
   - **Escenarios**
   - **Presentación**

---

## Escenario de ejemplo incluido

### Expansión Centro Logístico Aurora

Proyecto demostrativo para enseñar el funcionamiento integral de FINOVA.

**Supuestos principales**
- Inversión inicial: **₡28 000 000**
- Horizonte: **5 años**
- Valor residual: **₡4 000 000**
- Deuda: **45%**
- Capital propio: **55%**
- Tasa nominal de deuda: **10.50%**
- Tasa efectiva anual de deuda: **11.02%**
- Impuesto: **30%**
- Ke: **13.18%**
- WACC: **10.72%**

**Resultados esperados aproximados**
- **VAN:** ₡3 237 411
- **TIR:** 14.57%
- **Spread TIR – WACC:** 3.85 p.p.
- **DSCR mínimo:** 1.78x

Este caso fue construido para que la interfaz muestre:
- un resultado viable,
- una matriz de sensibilidad útil,
- una estructura de deuda visible,
- y una presentación ejecutiva completa.

---

## Capturas destacadas

### Dashboard de evaluación
<p align="center">
  <img src="docs/assets/screenshots/after/05-evaluacion-dashboard.png" alt="Dashboard de evaluación" width="100%" />
</p>

### Análisis de escenarios
<p align="center">
  <img src="docs/assets/screenshots/after/07-escenarios.png" alt="Análisis de escenarios" width="100%" />
</p>

### Presentación ejecutiva
<p align="center">
  <img src="docs/assets/screenshots/after/13-presentacion-06-conclusion.png" alt="Presentación ejecutiva" width="100%" />
</p>

---

## Base metodológica

FINOVA utiliza relaciones financieras estándar:

### CAPM
```text
Ke = rf + β × ERP + CRP
```

### WACC
```text
WACC = Ke × E / (D + E) + Kd × (1 − T) × D / (D + E)
```

### VAN
```text
VAN = -Inversión inicial + Σ Flujo_t / (1 + tasa)^t
```

### Cuota nivelada
```text
Cuota = P × i / (1 - (1 + i)^(-n))
```

### DSCR
```text
DSCR = Flujo operativo / Servicio de deuda
```

---

## Recomendación para GitHub

Si va a publicarlo como repositorio, la recomendación es:

- usar `docs/assets/branding/finova-social-preview.jpg` como **social preview**;
- mantener `docs/assets/branding/finova-hero.png` como imagen principal del README;
- y conservar la grilla `docs/assets/finova-grid-overview.png` como resumen visual del producto.

---

## Nota

FINOVA es una herramienta de evaluación financiera de proyectos.  
CAPM, WACC, VAN, TIR, DSCR y escenarios dependen de los supuestos ingresados.  
La aplicación no reemplaza una revisión tributaria, contable, legal, de mercado o de riesgo especializada.

---

## Autoría del paquete

Paquete preparado para publicación y actualización del repositorio de **FINOVA** con:

- aplicación final,
- notebook,
- escenario demo,
- identidad visual,
- capturas organizadas,
- documentación,
- y zip listo para subir a GitHub.
