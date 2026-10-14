# FINOVA v4 — Cambios incorporados tras la retroalimentación de clase

## 1. Tasa de descuento técnicamente fundamentada
- Capital propio: Ke mediante CAPM.
- Estructura mixta: WACC.
- Parámetros editables: tasa libre de riesgo, beta, prima de mercado, prima país y tasa impositiva.
- Campo para documentar fuentes y fecha de los parámetros.

## 2. Internacionalización y sector
- País/mercado y sector se vuelven parte explícita del proyecto.
- El beta y la prima país se ingresan según sector y jurisdicción.

## 3. Separación entre decisión de inversión y deuda
- El VAN con WACC usa flujos operativos antes del servicio de deuda.
- La deuda se analiza aparte con amortización, tasa efectiva, flujo después de deuda y DSCR.
- Esto evita contabilizar dos veces el costo financiero.

## 4. Escudo fiscal
- El costo de deuda después de impuestos se calcula como Kd × (1−T).
- Se muestra la composición del WACC y la estructura deuda/capital.

## 5. Escenarios más ricos
- Matriz VAN con variaciones simultáneas del flujo operativo y de la tasa de descuento.
- Escenario personalizado con cambios en ingresos, gastos y tasa.

## 6. Uso para más tipos de proyecto
- Nuevo negocio.
- Expansión de capacidad o bodega.
- Nuevo producto o servicio.
- Nueva ubicación o mercado.
- Compra de vehículos/equipo.
- Proyecto dentro de una empresa existente.

## 7. Riesgos más allá de los números
- Diferenciador difícil de replicar.
- Validación de mercado.
- Dependencia de persona clave.
- Intensidad competitiva.

## 8. Presentación automática mejorada
- Introducción.
- Proyecto.
- Financiamiento.
- CAPM/WACC.
- VAN/TIR.
- Conclusión y riesgos.

## 9. Notebook reforzado
El notebook ya no muestra solamente dos funciones. Documenta explícitamente: cuota nivelada, tasa efectiva anual, CAPM, WACC, amortización, VAN, TIR por bisección, payback descontado y DSCR, además de pruebas básicas y el generador HTML.
