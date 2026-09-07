---
name: utility-tree-generator
description: Genera, analiza y valida Árboles de Utilidad para arquitectura de software.
---

# Skill: Utility Tree Generator (ATAM)

## Propósito
Esta skill ayuda a descomponer los requerimientos no funcionales (Atributos de Calidad) de un sistema de software mediante la creación de un **Árbol de Utilidad** estandarizado.

## Estructura del Árbol de Utilidad

Todo Árbol de Utilidad generado debe seguir estrictamente esta jerarquía de 4 niveles:

1. **Raíz**: `Utility` (Utilidad del Sistema).
2. **Nivel 1 (Atributos de Calidad)**: Atributos principales (ej. *Performance*, *Usability*, *Availability*, *Security*, *Modifiability*).
3. **Nivel 2 (Sub-atributos / Refinamientos)**: Aspectos específicos del atributo (ej. *Latency*, *Peak load*, *SW failure*, *Authentication*).
4. **Nivel 3 (Prioridad)**: Tupla de evaluación `(Importancia de Negocio, Dificultad Arquitectónica)`.
   - **Valores válidos**: `H` (Alto), `M` (Medio), `L` (Bajo).
   - Ejemplo: `(H, H)`, `(M, L)`.
5. **Nivel 4 (Escenario de Calidad)**: Descripción del escenario concreto. Debe incluir:
   - **Estímulo**: El evento que llega al sistema.
   - **Respuesta Medible**: Métrica cuantitativa verificable (ej. "< 1 segundo", "99.999%").
  
## Material complementario

El material ubicado en `../../references/material-sei.pdf` se utiliza como
referencia conceptual para orientar la construcción del Árbol de Utilidad
según el enfoque ATAM.

Utilizar este material para:

* comprender la finalidad y estructura de un Árbol de Utilidad;
* organizar los atributos de calidad y sus respectivos escenarios;
* identificar los escenarios relevantes para la evaluación arquitectónica;
* orientar la priorización de los escenarios según su importancia para el
  negocio y su dificultad arquitectónica;
* mantener la relación entre los atributos de calidad y los escenarios SEI
  utilizados como entrada.

El material complementario debe utilizarse como guía conceptual y no como
fuente para inventar información específica del sistema proporcionada por
el usuario.

Cuando la información necesaria para construir o priorizar el árbol no sea
proporcionada, la skill puede realizar supuestos razonables, pero debe
identificarlos explícitamente como `[Supuesto]`.


## Formato de Salida Requerido

Cuando el usuario pida generar un árbol de utilidad, debes entregar **dos secciones**:

### Sección A: Árbol Jerárquico (Formato Texto / ASCII)
```text
Utility
├── <Atributo_1>
│   ├── <Subatributo_1.1> (<Importancia_Negocio>, <Dificultad_Arquitectura>) ──> <Escenario con concreto métrica>
│   └── <Subatributo_1.2> (<Importancia_Negocio>, <Dificultad_Arquitectura>) ──> <Escenario con concreto métrica>
└── <Atributo_2>
    └── <Subatributo_2.1> (<Importancia_Negocio>, <Dificultad_Arquitectura>) ──> <Escenario con concreto métrica>
