# Test 01 — Resultado: Árbol básico con múltiples atributos

## Árbol de Utilidad

```text
Utility
├── Performance
│   └── Search Latency (M, M) ──> Un usuario realiza una búsqueda de productos en operación normal. El sistema de búsqueda procesa la búsqueda y los resultados se muestran en menos de 2 segundos.
├── Availability
│   └── Server Failover (H, H) ──> El servidor principal sufre una falla en operación normal. El e-commerce continúa prestando servicio con un servidor alternativo, recuperándose en menos de 30 segundos.
└── Security
    └── Unauthorized Access Control (H, M) ──> Un usuario no autenticado intenta acceder a información privada en el sistema de gestión de usuarios. El sistema rechaza el acceso, de modo que ningún usuario no autorizado accede a la información.
```

## Justificación de prioridades

| Atributo | Escenario | Importancia | Dificultad | Justificación |
|----------|-----------|-------------|------------|---------------|
| Performance | Search Latency | M | M | Métrica de 2s alcanzable con arquitectura convencional; importa al negocio pero no es crítica frente a disponibilidad/seguridad. |
| Availability | Server Failover | H | H | Un corte de servicio detiene las ventas (impacto directo en ingresos) y requiere mecanismos de failover y redundancia complejos. |
| Security | Unauthorized Access Control | H | M | Proteger datos privados es crítico para la confianza y cumplimiento; el control de acceso es implementable con soluciones estándar. |

## Escenarios arquitectónicamente prioritarios

Requieren mayor atención arquitectónica:

1. **Availability — Server Failover (H, H)**: Mayor esfuerzo técnico (dificultad Alta) y alto impacto de negocio. Requiere redundancia, mecanismos de conmutación y monitoreo.
2. **Security — Unauthorized Access Control (H, M)**: Alto impacto de negocio; debe integrarse en todos los componentes.

## Verificación de criterios de aprobación

- [x] Se genera un único árbol de utilidad.
- [x] Performance, Disponibilidad y Seguridad aparecen como atributos separados.
- [x] Cada escenario está agrupado bajo el atributo correcto.
- [x] Los tres escenarios reciben importancia y dificultad.
- [x] Las prioridades tienen una justificación.
- [x] Se identifican los escenarios prioritarios.
- [x] No se crean atributos duplicados.
- [x] No se inventan escenarios adicionales.
- [x] Se conserva la información relevante de los escenarios SEI.
