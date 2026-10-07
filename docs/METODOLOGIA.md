# Metodología de FINOVA

## 1. Objetivo

FINOVA evalúa un proyecto de inversión que puede estar parcialmente financiado mediante deuda bancaria.

El modelo busca responder dos preguntas:

1. ¿El proyecto genera valor por encima del rendimiento mínimo exigido?
2. ¿Qué variables tendrían que cambiar para fortalecer o rescatar la viabilidad del proyecto?

## 2. Flujo operativo

Para cada año:

```text
Flujo neto = Ingresos − Gastos
```

Los ingresos y gastos son supuestos del proyecto y deben justificarse de forma independiente.

## 3. Financiamiento

El monto financiado se calcula como:

```text
Deuda inicial = Inversión inicial × porcentaje financiado
```

FINOVA utiliza cuota nivelada o sistema francés.

Para una tasa periódica `i`, principal `P` y `n` pagos:

```text
Cuota = P × i / [1 − (1+i)^(-n)]
```

La tasa periódica se obtiene a partir de la tasa nominal anual:

```text
i = tasa nominal anual / pagos por año
```

Cada cuota se divide en:

```text
Interés = saldo pendiente × i

Capital = cuota − interés
```

El capital amortizado disminuye el pasivo; el interés representa el costo financiero.

## 4. Flujo ajustado usado para VAN

FINOVA replica el tratamiento académico del ejercicio base:

```text
Flujo de caja = Flujo neto − cuota

Flujo ajustado = Flujo de caja + capital
```

Como:

```text
cuota = interés + capital
```

entonces:

```text
Flujo ajustado = Flujo neto − interés
```

Esta equivalencia queda visible en la aplicación para facilitar la auditoría del cálculo.

## 5. Valor presente y VAN

Cada flujo ajustado se descuenta:

```text
VP_t = Flujo ajustado_t / (1+k)^t
```

donde:

- `k` = tasa de descuento o costo de fondos;
- `t` = período.

El Valor Actual Neto es:

```text
VAN = − Inversión inicial + Σ VP_t
```

Criterio de decisión:

```text
VAN > 0  → el proyecto crea valor bajo los supuestos del modelo
VAN = 0  → el proyecto cubre exactamente el rendimiento requerido
VAN < 0  → el proyecto no cubre el rendimiento requerido
```

## 6. TIR

La Tasa Interna de Retorno es la tasa `r` que satisface:

```text
0 = − Inversión inicial + Σ [Flujo ajustado_t / (1+r)^t]
```

FINOVA la calcula numéricamente cuando los flujos permiten identificar una raíz.

## 7. Payback descontado

El período de recuperación descontado acumula los valores presentes hasta recuperar la inversión inicial.

Debe interpretarse como un indicador complementario; no sustituye al VAN.

## 8. Sensibilidad

FINOVA permite modificar simultáneamente ingresos y gastos.

Además calcula puntos de equilibrio manteniendo las demás variables constantes.

### Ingresos de equilibrio

Se calcula el factor uniforme de ingresos que lleva el VAN a cero.

### Gastos de equilibrio

Se calcula el factor uniforme de gastos que lleva el VAN a cero.

### Tasa bancaria de equilibrio

Se busca numéricamente la tasa del crédito que hace que:

```text
VAN = 0
```

manteniendo los demás supuestos constantes.

### Inversión máxima

Es la suma del valor presente de los flujos ajustados:

```text
Inversión máxima ≈ Σ VP_t
```

Por encima de ese monto, y manteniendo los flujos constantes, el VAN sería negativo.

## 9. Interpretación

FINOVA pretende apoyar una decisión, no automatizarla.

Los cálculos deben acompañarse de preguntas como:

- ¿Son realistas las ventas proyectadas?
- ¿Se incluyeron todos los costos?
- ¿La tasa de descuento está justificada?
- ¿El plazo de la deuda es coherente con la vida del proyecto?
- ¿Existe un margen suficiente ante escenarios adversos?
- ¿Qué supuestos tienen mayor impacto sobre el VAN?

## 10. Limitaciones

La versión 1.0.0 no incorpora automáticamente:

- impuestos;
- inflación;
- depreciación;
- capital de trabajo;
- valor residual;
- costos de emisión del crédito;
- riesgo probabilístico;
- correlación entre variables;
- Monte Carlo.

Estos elementos pueden incorporarse en versiones futuras.
