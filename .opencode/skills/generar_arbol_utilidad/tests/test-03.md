Test 03 — Información incompleta y supuestos
Entrada
Se tienen los siguientes escenarios de calidad:

Escenario 1 — Disponibilidad
Fuente: Usuario

Estímulo: Intenta utilizar el sistema.

Entorno: Operación normal.

Artefacto: Sistema de reservas.

Respuesta: El sistema debe estar disponible para recibir solicitudes.

Medida de respuesta: El sistema debe estar disponible la mayor parte del tiempo.

Escenario 2 — Seguridad
Fuente: Usuario

Estímulo: Intenta acceder a una cuenta.

Entorno: Operación normal.

Artefacto: Sistema de autenticación.

Respuesta: El sistema verifica las credenciales antes de permitir el acceso.

Medida de respuesta: No se especifica una medida cuantitativa.

Escenario 3 — Performance
Fuente: Usuario

Estímulo: Realiza una búsqueda.

Entorno: Operación normal.

Artefacto: Sistema de reservas.

Respuesta: El sistema devuelve los resultados.

Medida de respuesta: La búsqueda debe responder rápidamente.

Resultado esperado
La skill debe generar un Árbol de Utilidad con los tres atributos:

Disponibilidad

Seguridad

Performance

Debe asignar importancia y dificultad a cada escenario.

Como la información proporcionada no permite determinar con precisión algunas prioridades o medidas, la skill debe realizar supuestos razonables y marcarlos explícitamente como supuestos.

No debe presentar los valores asumidos como si hubieran sido proporcionados por el usuario.

La skill no debe inventar métricas concretas para los escenarios que no las tienen.

La salida debe diferenciar claramente:

Información proporcionada.

Supuestos realizados.

Árbol de utilidad.

Priorización de escenarios.

Criterios de aprobación
 Se genera el árbol con los tres atributos.

 Los escenarios están agrupados correctamente.

 Se asignan importancia y dificultad.

 Se identifican las partes de información faltante.

 Los supuestos realizados se indican explícitamente.

 No se presentan los supuestos como requisitos originales.

 No se inventan métricas concretas sin justificarlas.

 Se conserva la información proporcionada originalmente.

 Se justifican las prioridades.

 Se identifican los escenarios prioritarios.

