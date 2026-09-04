# Ejemplo — Seguridad

## Situación

Una aplicación de gestión de películas requiere autenticación para acceder a información privada. Un usuario que no tiene autorización intenta acceder a dicha información.

## Atributo de calidad

Seguridad (Security)

## Escenario SEI

| Fuente del estímulo | Estímulo | Entorno | Artefacto | Respuesta | Medida de respuesta |
|---|---|---|---|---|---|
| Usuario no autorizado | Intenta acceder a información privada | Sistema en operación normal | Módulo de autenticación y autorización | Rechaza el acceso y registra el intento | El 100% de los intentos no autorizados debe ser rechazado y registrado |

## Por qué es un buen escenario

- Se identifica quién genera el estímulo.
- El estímulo representa un evento concreto.
- Se establece el estado del sistema.
- Se identifica el módulo involucrado.
- La respuesta es verificable.
- La medida establece un objetivo cuantificable.
