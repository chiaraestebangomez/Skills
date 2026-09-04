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

- **Con contexto completo**: Si el usuario proporciona el atributo de calidad
  y contexto del sistema, genero el escenario directamente.
- **Con contexto parcial**: Si falta informacion, identifico que falta, propongo
  valores razonables y presento el escenario con las partes propuestas marcadas
  explicitamente como supuestos. No me limito a preguntar.

## Manejo de informacion faltante

Cuando el usuario no proporciona toda la informacion necesaria:

1. **Identificar** que partes del escenario estan presentes y cuales faltan.
2. **Proponer** valores posibles para completar las partes faltantes, basandome
   en el contexto disponible y en buenas practicas del dominio.
3. **No presentar** los supuestos como informacion proporcionada por el usuario.
4. **Marcar explicitamente** cada valor propuesto con el prefijo `[Supuesto]`
   para que el usuario pueda identificar y corregir facilmente lo que no
   corresponda.

Ejemplo de formato:

| Fuente del estimulo       | Estimulo                | Entorno   | Artefacto         | Respuesta              | Medida de respuesta      |
|---------------------------|-------------------------|-----------|-------------------|------------------------|--------------------------|
| [Supuesto] Usuario final  | Peticion HTTP GET       | Normal    | [Supuesto] API    | Retorna 200 OK         | [Supuesto] < 200ms       |

Si el usuario no especifica el atributo de calidad, preguntar ese unico dato
antes de generar, ya que es el eje central del escenario.

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

## Ejemplos de referencia

Los archivos ubicados en `examples/` contienen escenarios SEI correctamente resueltos.

Utilizarlos como referencia para:
- mantener la estructura de seis partes;
- identificar el nivel de especificidad esperado;
- distinguir estímulos de respuestas;
- formular medidas de respuesta cuantificables;
- mantener coherencia entre atributo, estímulo y respuesta.

Los ejemplos son referencias de formato y criterio, no deben copiarse literalmente cuando se resuelve un nuevo escenario.

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
