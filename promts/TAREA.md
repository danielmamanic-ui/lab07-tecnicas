# Tarea: Mi prompt avanzado

## Tarea elegida
Diseñar y generar pruebas unitarias automatizadas con JUnit 5 para un módulo de cálculo de promedio de notas en Java.

## Version 1: prompt basico

```text
Crea pruebas unitarias para un sistema de notas estudiantiles en Java.



Actúa como un Especialista en Aseguramiento de Calidad de Software (QA Automation) en Java.
Genera clases de prueba con JUnit 5 para un método `calcularPromedio(List<Double> notas)`.
Asegúrate de incluir pruebas para notas negativas y mayores a 20.



<rol>
Actúa como un Especialista en Aseguramiento de Calidad de Software (QA Automation) sénior.
</rol>

<contexto>
Estamos probando el método `double calcularPromedio(List<Double> notas)` de la clase `CalculadoraNotas`.
Las notas válidas están en el rango de 0 a 20. El método debe lanzar `IllegalArgumentException` si la lista está vacía o contiene valores fuera de rango.
</contexto>

<ejemplos>
Ejemplo de prueba exitosa:
Input: [15.0, 18.0, 12.0] -> Output esperado: 15.0

Ejemplo de excepción:
Input: [] -> Lanza IllegalArgumentException ("La lista no puede estar vacía")
</ejemplos>

<instrucción>
Analiza paso a paso los escenarios límite (lista vacía, notas negativas, notas > 20, lista nula).
Luego, genera la clase completa de prueba en JUnit 5.
</instrucción>

<formato>
1. Muestra primero la lista de casos probados paso a paso.
2. Muestra el código Java dentro de un bloque de código.
</formato>


Tecnicas usadas en el prompt finalParte del Prompt FinalTécnica Correspondiente<rol>Actúa como un Especialista en Aseguramiento de Calidad...</rol>Role Prompting<ejemplos>Input: [15.0, 18.0] -> Output: 15.0...</ejemplos>Few-Shot<instrucción>Analiza paso a paso los escenarios límite...</instrucción>Chain of ThoughtUso de etiquetas <rol>, <contexto>, <formato>Prompt Estructurado


Evaluacion del resultadoCriterio de EvaluaciónCumple (Sí / No)¿Incluye configuración del rol especificado de QA?Sí¿Aplica formato estructurado usando etiquetas delimitadoras?Sí¿Evalúa casos de borde (lista vacía, nula, valores fuera de rango)?Sí¿El código generado compila y utiliza JUnit 5 correctamente?Sí