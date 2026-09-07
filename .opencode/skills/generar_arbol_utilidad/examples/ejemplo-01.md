# Ejemplos de Prueba para Utility Tree Generator

Este archivo contiene casos de prueba de diversos dominios para validar que la skill `utility-tree-generator` desglose correctamente la estructura de 4 niveles de ATAM, aplique las tuplas `(Importancia Negocio, Riesgo Arquitectura)` y garantice métricas cuantitativas en todos los escenarios.

---

## Ejemplo 1: Plataforma de Comercio Electrónico (E-commerce)

### Entrada (Prompt del Usuario)
> "Genera el Árbol de Utilidad para una plataforma de e-commerce durante un evento de alta demanda (CyberMonday). Prioriza Performance, Availability, Security y Scalability."

### Salida Esperada

```text
Utility
├── Performance
│   ├── Checkout Latency (H, H) ──> Un usuario procesa un pago durante el pico de ventas. El checkout se completa en menos de 2 segundos.
│   └── Catalog Throughput (M, M) ──> El catálogo recibe 50,000 peticiones por minuto. El sistema responde el 99% de las consultas en < 200 ms.
├── Availability
│   └── Database Failover (H, H) ──> La base de datos principal sufre una caída. El failover a la réplica secundaria ocurre automáticamente en menos de 10 segundos sin pérdida de datos.
├── Security
│   └── PCI-DSS Compliance (H, M) ──> Un atacante intenta interceptar datos de tarjetas de crédito. Toda la transmisión utiliza TLS 1.3 y los datos en reposo están cifrados al 100%.
└── Scalability
    └── Auto-scaling (H, H) ──> El tráfico aumenta un 300% en 5 minutos. El sistema auto-escala instancias manteniendo el uso de CPU por debajo del 70%.
