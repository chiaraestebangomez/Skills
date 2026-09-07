# Ejemplos de Prueba para Utility Tree Generator

Este archivo contiene casos de prueba adicionales para validar que la skill `utility-tree-generator` desglose correctamente la estructura de 4 niveles de ATAM, aplique las tuplas `(Importancia Negocio, Riesgo Arquitectura)` y garantice métricas cuantitativas en todos los escenarios.

---

## Ejemplo 2: Aplicación de Telemedicina y Salud

### Entrada (Prompt del Usuario)
> "Crea el Árbol de Utilidad para una app de telemedicina que transmite video en vivo y maneja historias clínicas electrónicas. Enfócate en Security, Interoperability y Usability."

### Salida Esperada

```text
Utility
├── Security
│   ├── Data Confidentiality (H, H) ──> Un usuario no autorizado intenta acceder a registros médicos. El sistema bloquea el acceso y aplica cifrado bajo normativa HIPAA al 100%.
│   └── Role Authorization (H, M) ──> Un médico accede a la ficha del paciente. La verificación de permisos por token toma < 100 ms.
├── Interoperability
│   └── HL7/FHIR Sync (M, H) ──> El sistema recibe una actualización de laboratorio externo mediante el estándar FHIR. La sincronización se completa en < 5 segundos.
└── Usability
    └── Video Call Setup (H, L) ──> Un paciente inicia la consulta médica. La videollamada se conecta en máximo 2 clics y en menos de 4 segundos.
