# TP3 - Ejercicio Integrador

## 👥 Integrantes
* Canale Vilanova, Gian Franco
* Esteban Gomez, Chiara

## 🔗 Repositorio
* **GitHub:** [Skills](https://github.com/chiaraestebangomez/Skills.git)

---

## ⚙️ Procedimiento

Comenzamos enviándole un *prompt* a OpenCode en el que detallamos las siguientes consideraciones y pasos para la elaboración de la *skill* encargada de generar escenarios de calidad (basados en el *template* de 6 partes del SEI) y de verificar si los escenarios provistos por el usuario están completos:

* **Propósito de la *skill*:** Generar atributos de calidad siguiendo el *template* de seis partes del SEI y completar escenarios de calidad según corresponda.
* **Formato del *template*:** Una tabla estructurada con las columnas: `Fuente del estímulo`, `Estímulo`, `Ambiente`, `Artefacto`, `Respuesta` y `Medida de la respuesta`.
* **Gestión de escenarios incompletos:** Ante un escenario incompleto, la *skill* debe generar supuestos y marcarlos explícitamente como tales, de modo que el usuario pueda identificarlos y validar si son correctos.

Una vez que OpenCode devolvió la primera versión de la *skill*, evaluamos y debatimos lo generado. Formulamos *prompts* de corrección para ajustar los aspectos erróneos o mal planteados, hasta obtener una versión que consideramos correcta.

Con la *skill* definida, procedimos a cargarle ejemplos generados por IA junto con sus respectivas salidas esperadas (*few-shot prompting*). Se incluyeron cuatro ejemplos correspondientes a distintos atributos de calidad: **Disponibilidad**, **Modificabilidad**, **Performance** y **Seguridad**.

---

### 🧪 Fase de Testing

A continuación, pasamos a la fase de pruebas, la cual se dividió en dos etapas:

1. **Pruebas con escenarios generados por IA:** Se evaluaron tres tipos de casos:
   * **Escenario completo:** La *skill* no debía generar supuestos.
   * **Escenario incompleto:** La *skill* debía realizar los supuestos necesarios para completar el escenario.
   * **Escenario con información insuficiente:** La *skill* debía solicitar información adicional al usuario antes de generar la respuesta.

   > 📁 *Todas las salidas resultantes se almacenaron en el directorio `/results`.*

2. **Pruebas con ejercicios del Trabajo Práctico 3 (TP3):** Se ingresaron ejercicios del práctico y se comparó la salida de la *skill* con las resoluciones elaboradas previamente por el equipo (sin asistencia de la IA).

En ambos procesos de prueba, mantuvimos una actitud crítica frente a las respuestas generadas, cotejándolas de forma rigurosa con los criterios y soluciones que hubiéramos propuesto manualmente.

---

### 🌳 Skill: Árbol de Utilidad y Material Complementario

El proceso para la creación de la *skill* del **Árbol de Utilidad** fue similar:
* Definimos el contenido deseado, el formato de salida y consideraciones adicionales.
* Como ejemplos de entrenamiento, proporcionamos conjuntos de escenarios de calidad con sus correspondientes árboles de utilidad.
* Para su validación, cada prueba consistió en procesar tres escenarios de calidad estructurados bajo las seis partes del SEI.

**Material complementario:**
Finalmente, incorporamos material complementario para guiar las respuestas de la *skill*, sumando los capítulos 4 y 5 del libro *Design It!* (Michael Keeling) e instruyendo explícitamente a la *skill* para que utilice dicha bibliografía como marco de referencia.

---

## 📌 Conclusiones

A partir del análisis de las salidas generadas por la *skill*, concluimos que, ante la falta de restricciones estrictas, el modelo tiende a elaborar supuestos excesivamente detallados cuando se enfrenta a escenarios con información incompleta.

Si bien estas generaciones resultan sumamente concretas y minuciosas, determinamos que **no son técnicamente erróneas**, sino que presentan un nivel de especificidad y representación mayor al estrictamente necesario. Esto demuestra una capacidad adecuada para contextualizar las faltantes del escenario, aunque sugiere la conveniencia de acotar el alcance de los supuestos automáticos para no sobreespecificar el dominio del problema.
