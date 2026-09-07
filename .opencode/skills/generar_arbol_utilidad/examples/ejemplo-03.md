# Ejemplo de Prueba: Motor de Trading de Alta Frecuencia (Finanzas)

Este archivo sirve para probar la skill `utility-tree-generator` en un entorno de sistemas financieros de baja latencia.

## Entrada (Prompt del Usuario)
> "Genera el Árbol de Utilidad para un motor de emparejamiento de órdenes bursátiles (Trading Engine) priorizando Performance, Modifiability y Auditability."

## Salida Esperada de la Skill

### Árbol de Utilidad

```text
Utility
├── Performance
│   ├── Order Matching Latency (H, H) ──> Entra una orden de compra durante alta volatilidad. El motor la empareja en menos de 500 microsegundos.
│   └── Throughput (H, H) ──> El mercado procesa 100,000 órdenes por segundo sin degradar el tiempo de respuesta.
├── Modifiability
│   └── New Asset Class (M, M) ──> Se requiere agregar un nuevo tipo de activo financiero. Un desarrollador implementa la regla en < 3 días sin alterar el core.
└── Auditability
    └── Regulatory Logging (H, L) ──> Se ejecuta cualquier transacción. El registro completo para la entidad reguladora se guarda en disco el 100% de las veces.
