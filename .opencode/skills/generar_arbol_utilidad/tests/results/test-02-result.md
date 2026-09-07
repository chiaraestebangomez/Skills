# Test 02 — Resultado: Varios escenarios del mismo atributo

## Árbol de Utilidad

```text
Utility
├── Performance
│   ├── Query Latency (M, M) ──> Un usuario realiza una consulta de productos en operación normal. El sistema de consultas procesa la consulta y la respuesta se produce en menos de 2 segundos.
│   ├── Concurrent Load (H, H) ──> 500 usuarios realizan consultas simultáneamente en período de alta demanda. El sistema de consultas continúa procesando las consultas, manteniendo el tiempo de respuesta por debajo de 4 segundos.
│   └── API Throughput (M, M) ──> Un sistema externo envía solicitudes de consulta en operación normal. La API procesa las solicitudes correctamente, procesando al menos 100 solicitudes por segundo.
└── Modifiability
    └── Business Rule Change (M, L) ──> El equipo de desarrollo necesita modificar una regla de negocio durante el mantenimiento. El cambio se implementa en el módulo de reglas de negocio sin modificar otros módulos, en menos de 4 horas.
```

## Justificación de prioridades

| Atributo | Escenario | Importancia | Dificultad | Justificación |
|----------|-----------|-------------|------------|---------------|
| Performance | Query Latency | M | M | Métrica de 2s asumible con optimización estándar de consultas; relevante pero no crítica aislada. |
| Performance | Concurrent Load | H | H | Soportar 500 usuarios concurrentes con respuesta < 4s exige escalabilidad/caching, alto impacto de negocio y alta dificultad técnica. |
| Performance | API Throughput | M | M | 100 req/s es alcanzable con una API bien dimensionada; importante para integraciones. |
| Modifiability | Business Rule Change | M | L | Cambiar una regla en < 4h sin afectar otros módulos es el objetivo del diseño modular; dificultad baja con buena separación de responsabilidades. |

## Escenarios arquitectónicamente prioritarios

Requieren mayor atención arquitectónica:

- **Performance — Concurrent Load (H, H)**: El escenario de mayor dificultad y que condiciona la arquitectura de escalabilidad.
- **Performance — API Throughput (M, M)**: Define los límites de capacidad de la capa de integración, a tener en cuenta junto al escenario de carga concurrente.

## Verificación de criterios de aprobación

- [x] Existe una única rama Performance.
- [x] Los tres escenarios de Performance están agrupados correctamente.
- [x] Los tres escenarios permanecen diferenciados.
- [x] Las medidas de respuesta se conservan.
- [x] Modificabilidad aparece como una rama independiente.
- [x] Todos los escenarios tienen importancia y dificultad.
- [x] Las prioridades están justificadas.
- [x] No se pierde ningún escenario.
- [x] No se duplican atributos.
- [x] Se identifican los escenarios arquitectónicamente prioritarios.
