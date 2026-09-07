# Test 03 — Resultado: Información incompleta y supuestos

## Información proporcionada

Escenarios de calidad originales:

- **Disponibilidad**: El sistema de reservas debe estar disponible la mayor parte del tiempo. *(medida no cuantitativa)*
- **Seguridad**: El sistema de autenticación verifica credenciales antes de permitir el acceso. *(sin medida cuantitativa)*
- **Performance**: La búsqueda en el sistema de reservas debe responder rápidamente. *(medida no cuantitativa)*

## Identificación de información faltante

- Disponibilidad: no se especifica un porcentaje de disponibilidad objetivo (p. ej. 99.9%).
- Seguridad: no se especifica la métrica (p. ej. % de intentos no autorizados rechazados).
- Performance: no se especifica un tiempo de respuesta cuantitativo (p. ej. < X segundos).

## Supuestos realizados

> Los siguientes valores **NO fueron proporcionados por el usuario**; son supuestos razonables marcados explícitamente para permitir la priorización.

- **S1 (Disponibilidad)**: Se asume un objetivo de disponibilidad del 99.9% (sistema de reservas orientado a servicio al cliente).
- **S2 (Seguridad)**: Se asume que el 100% de los intentos de acceso con credenciales inválidas son rechazados.
- **S3 (Performance)**: Se asume una meta de respuesta de < 3 segundos para la búsqueda de reservas.

## Árbol de Utilidad

> Las métricas entre corchetes `[S1]`, `[S2]`, `[S3]` corresponden a supuestos, no a datos originales.

```text
Utility
├── Availability
│   └── System Availability (H, H) ──> Un usuario intenta utilizar el sistema de reservas en operación normal. El sistema está disponible para recibir solicitudes, con una disponibilidad del 99.9% [S1].
├── Security
│   └── Authentication Check (H, M) ──> Un usuario intenta acceder a una cuenta en el sistema de autenticación. El sistema verifica las credenciales antes de permitir el acceso, rechazando el 100% de los intentos con credenciales inválidas [S2].
└── Performance
    └── Search Responsiveness (M, L) ──> Un usuario realiza una búsqueda en el sistema de reservas en operación normal. El sistema devuelve los resultados, respondiendo en menos de 3 segundos [S3].
```

## Justificación de prioridades

| Atributo | Escenario | Importancia | Dificultad | Justificación |
|----------|-----------|-------------|------------|---------------|
| Availability | System Availability | H | H | La disponibilidad constante es crítica en un sistema de reservas (pérdida de servicio directa); lograr alta disponibilidad suele requerir alta complejidad. |
| Security | Authentication Check | H | M | El control de acceso es esencial para la confianza; implementable con soluciones estándar de autenticación (dificultad media). |
| Performance | Search Responsiveness | M | L | La búsqueda rápida importa para la experiencia de usuario, pero su dificultad es baja con optimización de consultas. |

## Escenarios arquitectónicamente prioritarios

Requieren mayor atención arquitectónica:

1. **Availability — System Availability (H, H)**: Mayor dificultad y alto impacto; condiciona el diseño de redundancia.
2. **Security — Authentication Check (H, M)**: Alto impacto de negocio; debe ser transversal a la arquitectura.

## Verificación de criterios de aprobación

- [x] Se genera el árbol con los tres atributos.
- [x] Los escenarios están agrupados correctamente.
- [x] Se asignan importancia y dificultad.
- [x] Se identifican las partes de información faltante.
- [x] Los supuestos realizados se indican explícitamente.
- [x] No se presentan los supuestos como requisitos originales.
- [x] No se inventan métricas concretas sin justificarlas (se marcan como supuestos).
- [x] Se conserva la información proporcionada originalmente.
- [x] Se justifican las prioridades.
- [x] Se identifican los escenarios prioritarios.
