# Ejemplo — Modificabilidad

## Situación

El sistema de gestión de películas debe permitir agregar nuevos campos a la información de una película sin modificar los módulos que realizan las búsquedas.

## Atributo de calidad

Modificabilidad (Modifiability)

## Escenario SEI

| Fuente del estímulo | Estímulo | Entorno | Artefacto | Respuesta | Medida de respuesta |
|---|---|---|---|---|---|
| Desarrollador | Solicita agregar un nuevo campo a la información de las películas | Durante el mantenimiento del sistema | Módulo de gestión de películas | Incorpora el nuevo campo sin modificar el módulo de búsqueda | El cambio debe poder implementarse en menos de 4 horas y no debe requerir modificaciones en más de 2 módulos existentes |

## Por qué es un buen escenario

- El estímulo representa una modificación concreta.
- Se identifica que ocurre durante mantenimiento.
- Se especifica qué parte del sistema será modificada.
- La respuesta indica qué debe permitir la arquitectura.
- El esfuerzo y el impacto del cambio pueden medirse.
