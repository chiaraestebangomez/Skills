---
name: generar-atributos-sei
description: Genera escenarios de atributos de calidad usando el template SEI de seis partes
---

## Qué hago

Genero escenarios de atributos de calidad para sistemas software utilizando
el template de seis partes del Software Engineering Institute (SEI/Carnegie Mellon).

Cada escenario describe una situacion concreta en la que un estimulo alcanza el sistema
y el sistema responde de una manera medible.

## Cuándo usarme

Cuando el usuario solicite:
- Escenarios de atributos de calidad
- Requisitos no funcionales en formato SEI
- Analisis de calidad de software
- Validacion de escenarios existentes

## Modo de operacion

- **Con contexto**: Si el usuario proporciona el atributo de calidad y contexto del
  sistema, genero el escenario directamente.
- **Sin contexto**: Si falta informacion esencial (atributo o contexto del sistema),
  pregunto antes de generar.

Preguntas minimas cuando falte contexto:
1. ¿Que atributo de calidad te interesa?
2. ¿Que tipo de sistema o dominio estas evaluando?
3. ¿Hay restricciones o ambientes especificos?

## Template SEI — Seis partes

| #  | Parte                  | Descripcion                                                        |
|----|------------------------|--------------------------------------------------------------------|
| 1  | Fuente del estimulo    | Quien o que genera el evento (usuario, sistema externo, temporizador, fallo interno) |
| 2  | Estimulo               | El evento que llega al sistema (peticion, fallo, startup, shutdown, variacion de carga) |
| 3  | Entorno                | Estado del sistema cuando llega el estimulo (normal, degradado, arranque, mantenimiento) |
| 4  | Artefacto              | Parte del sistema afectada (sistema completo, componente, base de datos, interfaz) |
| 5  | Respuesta              | Que hace el sistema ante el estimulo (procesar, rechazar, escalar, notificar, failover) |
| 6  | Medida de respuesta    | Como se mide la respuesta (latencia, porcentaje, tiempo de recuperacion, numero de intentos) |

## Atributos de calidad soportados

| Atributo          | Que cubre                                                             |
|-------------------|-----------------------------------------------------------------------|
| Rendimiento       | Latencia, throughput, uso de recursos, tiempos de respuesta           |
| Disponibilidad    | Tiempo de actividad, tolerancia a fallos, recuperacion                |
| Seguridad         | Autenticacion, autorizacion, integridad, confidencialidad             |
| Modificabilidad   | Costo y esfuerzo de realizar cambios en el sistema                    |
| Testabilidad      | Facilidad de establecer condiciones de prueba y verificar resultados  |
| Usabilidad        | Facilidad de aprendizaje, eficiencia de uso, prevencion de errores    |
| Interoperabilidad | Capacidad de interactuar con otros sistemas o componentes externos     |
| Escalabilidad     | Capacidad de manejar incremento de carga manteniendo el rendimiento    |
| Portabilidad      | Facilidad de migrar el sistema a otro entorno o plataforma            |
| Compatibilidad    | Coexistencia con otros sistemas sin conflictos de recursos            |

## Formato de salida

Presentar cada escenario en una tabla markdown con 6 columnas:

| Fuente del estimulo | Estimulo | Entorno | Artefacto | Respuesta | Medida de respuesta |
|---------------------|----------|---------|-----------|-----------|---------------------|
| ...                 | ...      | ...     | ...       | ...       | ...                 |

Si se generan multiples escenarios para el mismo atributo, numerarlos
y mantener el formato de tabla para cada uno.

## Validacion

Antes de entregar un escenario, verificar que:
1. Las 6 partes estan presentes y no estan vacias.
2. La fuente del estimulo es un agente identificable (no ambigua).
3. El estimulo es un evento concreto (no una caracteristica general).
4. La medida de respuesta es cuantificable o al menos verificable.
5. Existe coherencia entre el estimulo y la respuesta del sistema.
6. El artefacto apunta a un componente o subsistema razonable.
