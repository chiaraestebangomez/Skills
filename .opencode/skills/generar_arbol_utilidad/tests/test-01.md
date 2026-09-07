Test 01 — Árbol básico con múltiples atributos
Entrada
Se tienen los siguientes escenarios de calidad generados previamente mediante el template SEI de seis partes:

Escenario 1 — Performance
Fuente: Usuario

Estímulo: Realiza una búsqueda de productos.

Entorno: Operación normal.

Artefacto: Sistema de búsqueda.

Respuesta: El sistema procesa la búsqueda y devuelve los resultados.

Medida de respuesta: Los resultados deben mostrarse en menos de 2 segundos.

Escenario 2 — Disponibilidad
Fuente: Servidor principal

Estímulo: Se produce una falla del servidor.

Entorno: Operación normal.

Artefacto: Sistema de comercio electrónico.

Respuesta: El sistema continúa prestando el servicio utilizando un servidor alternativo.

Medida de respuesta: El servicio debe recuperarse en menos de 30 segundos.

Escenario 3 — Seguridad
Fuente: Usuario no autenticado

Estímulo: Intenta acceder a información privada.

Entorno: Operación normal.

Artefacto: Sistema de gestión de usuarios.

Respuesta: El sistema rechaza el acceso.

Medida de respuesta: Ningún usuario no autorizado debe poder acceder a la información.

Resultado esperado
La skill debe generar un único Árbol de Utilidad con los atributos:

Performance

Disponibilidad

Seguridad

Cada atributo debe contener su escenario correspondiente.

Los escenarios deben conservar la información relevante del escenario SEI original.

Cada escenario debe tener una valoración de:

Importancia: Alta, Media o Baja.

Dificultad: Alta, Media o Baja.

La respuesta debe incluir una justificación de las prioridades y una identificación de los escenarios que requieren mayor atención arquitectónica.

No deben aparecer atributos duplicados.

Criterios de aprobación
 Se genera un único árbol de utilidad.

 Performance, Disponibilidad y Seguridad aparecen como atributos separados.

 Cada escenario está agrupado bajo el atributo correcto.

 Los tres escenarios reciben importancia y dificultad.

 Las prioridades tienen una justificación.

 Se identifican los escenarios prioritarios.

 No se crean atributos duplicados.

 No se inventan escenarios adicionales.

 Se conserva la información relevante de los escenarios SEI.
