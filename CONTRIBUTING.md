# Contributing to FINOVA

Gracias por tu interés en mejorar FINOVA.

## Principios del proyecto

FINOVA busca mantener tres características:

1. **Trazabilidad financiera**: cada resultado debe poder explicarse desde sus supuestos y fórmulas.
2. **Interfaz clara**: los cambios deben preservar un flujo de uso sencillo y una presentación ejecutiva legible.
3. **Portabilidad**: la aplicación principal debe seguir funcionando como HTML autónomo, sin depender de un servidor.

## Cómo proponer cambios

1. Crea una rama descriptiva a partir de `main`.
2. Realiza cambios pequeños y enfocados.
3. Verifica que el escenario `FINOVA_Ejemplo_Centro_Logistico_Aurora.json` pueda cargarse correctamente.
4. Comprueba, como mínimo:
   - CAPM / Ke
   - WACC
   - VAN
   - TIR
   - amortización
   - DSCR
   - escenarios
   - presentación
5. Abre un Pull Request explicando:
   - qué cambia,
   - por qué cambia,
   - cómo verificaste el resultado,
   - y, si modifica la interfaz, adjunta una captura.

## Cambios al modelo financiero

Las modificaciones a fórmulas o criterios de decisión deben incluir una explicación metodológica. Evita introducir una dependencia externa cuando el cálculo pueda mantenerse auditable con JavaScript o Python estándar.

## Estilo

- Mantén el contenido de la interfaz en español.
- Prefiere nombres de variables y funciones claros.
- Evita valores de ejemplo codificados dentro del motor principal.
- Conserva la separación entre el análisis del proyecto y la capacidad de pago de la deuda cuando se utiliza WACC.

## Licencia

Al contribuir, aceptas que tus contribuciones se distribuyan bajo la licencia MIT del proyecto.
