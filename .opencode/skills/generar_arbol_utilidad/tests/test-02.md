Test 02 — Varios escenarios del mismo atributo
Entrada
Se tienen los siguientes escenarios de calidad generados previamente mediante el template SEI de seis partes:

Escenario 1 — Performance
Fuente: Usuario

Estímulo: Realiza una consulta de productos.

Entorno: Operación normal.

Artefacto: Sistema de consultas.

Respuesta: El sistema procesa la consulta y muestra los resultados.

Medida de respuesta: La respuesta debe producirse en menos de 2 segundos.

Escenario 2 — Performance
Fuente: Usuarios concurrentes

Estímulo: 500 usuarios realizan consultas simultáneamente.

Entorno: Período de alta demanda.

Artefacto: Sistema de consultas.

Respuesta: El sistema continúa procesando las consultas.

Medida de respuesta: El tiempo de respuesta debe mantenerse por debajo de 4 segundos.

Escenario 3 — Performance
Fuente: Sistema externo

Estímulo: Envía solicitudes de consulta.

Entorno: Operación normal.

Artefacto: API del sistema.

Respuesta: La API procesa las solicitudes correctamente.

Medida de respuesta: Debe procesar al menos 100 solicitudes por segundo.

Escenario 4 — Modificabilidad
Fuente: Equipo de desarrollo

Estímulo: Necesita modificar una regla de negocio.

Entorno: Durante el mantenimiento del sistema.

Artefacto: Módulo de reglas de negocio.

Respuesta: El cambio se implementa sin modificar otros módulos.

Medida de respuesta: La modificación debe poder realizarse en menos de 4 horas.

Resultado esperado
La skill debe agrupar los tres escenarios de Performance bajo una única rama de Performance.

La estructura debe conceptualmente ser:

Utilidad
├── Performance
│   ├── Escenario 1
│   ├── Escenario 2
│   └── Escenario 3
│
└── Modificabilidad
    └── Escenario 4
Los tres escenarios de Performance deben permanecer diferenciados y conservar sus respectivas medidas de respuesta.

No debe crearse una rama Performance separada para cada escenario.

La skill debe asignar importancia y dificultad a cada escenario y justificar las prioridades.

Criterios de aprobación
 Existe una única rama Performance.

 Los tres escenarios de Performance están agrupados correctamente.

 Los tres escenarios permanecen diferenciados.

 Las medidas de respuesta se conservan.

 Modificabilidad aparece como una rama independiente.

 Todos los escenarios tienen importancia y dificultad.

 Las prioridades están justificadas.

 No se pierde ningún escenario.

 No se duplican atributos.

 Se identifican los escenarios arquitectónicamente prioritarios.

