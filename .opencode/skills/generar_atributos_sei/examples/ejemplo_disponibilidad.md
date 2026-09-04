# Ejemplo — Disponibilidad

## Situación

Un sistema utiliza un servidor principal y un servidor de respaldo. Si el servidor principal falla, el sistema debe continuar funcionando mediante el servidor de respaldo.

## Atributo de calidad

Disponibilidad (Availability)

## Escenario SEI

| Fuente del estímulo | Estímulo | Entorno | Artefacto | Respuesta | Medida de respuesta |
|---|---|---|---|---|---|
| Sistema de monitoreo | Detecta la falla del servidor principal | Operación normal | Servicio de aplicación | Activa el servidor de respaldo y continúa brindando el servicio | El servicio debe recuperarse en menos de 30 segundos y la pérdida de solicitudes no debe superar el 1% |

## Por qué es un buen escenario

- El evento que provoca la situación está claramente definido.
- Se especifica el contexto en el que ocurre.
- Se identifica el componente afectado.
- La respuesta del sistema es concreta.
- La respuesta puede medirse mediante tiempo de recuperación y porcentaje de solicitudes perdidas.
