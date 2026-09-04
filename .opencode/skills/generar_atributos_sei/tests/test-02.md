# Test 02

## Objetivo

Verificar que la skill pueda detectar información faltante y completar un escenario mediante supuestos explícitos.

## Entrada

El sistema debe responder rápidamente cuando muchos usuarios realicen consultas al mismo tiempo.

## Resultado esperado

La skill debe detectar que existen datos insuficientes para construir una medida precisa y proponer valores razonables marcados como `[Supuesto]`.

## Criterios de aprobación

- Detecta que "rápidamente" no es una medida cuantificable.
- Detecta que "muchos usuarios" no especifica una cantidad.
- Propone valores para completar la información.
- Marca los valores agregados con `[Supuesto]`.
- Genera las seis partes del escenario.
