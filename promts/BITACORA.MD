# Bitácora de Técnicas Avanzadas
Laboratorio 07: Técnicas Avanzadas de Prompting.  
Herramienta de IA usada: ChatGPT

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Sí/No) |
| :--- | :---: | :--- | :---: |
| Zero-shot | 5 | Texto con explicaciones adicionales e introducción | No |
| One-shot | 5 | Lista de párrafos con flechas | Sí |
| Few-shot | 5 | "texto" -> Etiqueta | Sí |

## Ejercicio 3: Chain of Thought

| Pedido | Respuesta de la IA | Muestra los pasos (Sí/No) | Correcta (Sí/No) |
| :--- | :--- | :---: | :---: |
| Directo | 318.60 | No | Sí |
| Paso a paso | Muestra precio con descuento (90), precio con IGV (106.20) y total por 3 unidades (318.60) | Sí | Sí |

Ver el razonamiento paso a paso es útil porque permite auditar la lógica y los cálculos intermedios de la IA. Si el resultado final fuese incorrecto, la cadena de pensamiento revela exactamente en qué paso ocurrió la falla para corregirla rápidamente.

## Ejercicio 4: Role prompting

| Versión | Vocabulario (sencillo/técnico) | Usa ejemplos o código | A quién le sirve más |
| :--- | :--- | :--- | :--- |
| A. Sin rol | General y conceptual | Explicación breve de texto | Público general o principiantes |
| B. Rol docente | Sencillo y cotidiano | Analogía (caja etiquetada para guardar cosas) | Estudiantes sin experiencia previa |
| C. Rol senior | Técnico (memoria, tipos de datos, alcance) | Snippet de código Java | Desarrolladores o compañeros de equipo |

## Ejercicio 5: Descomposición

* **Paso 1:** Entregó la lista de los 5 requisitos principales (gestión de productos, control de stock, registrar ventas, alertas de stock mínimo y reportes).
* **Paso 2:** Generó el diseño de clases (`Producto`, `Inventario`, `Venta`) con sus respectivos atributos y tipos de datos en Java.
* **Paso 3:** Entregó el código Java completo de la clase `Producto` con atributos, constructor y sus métodos `get` y `set`.
* **Paso 4:** Revisó el código y propuso 3 mejoras: validación en setters para evitar precios/stock negativos, implementación de `toString()` y control de encapsulamiento.

Al pedir la tarea de una sola vez se obtiene un sistema muy general o resumido, mientras que mediante la descomposición se obtiene un diseño detallado y un código modular que sigue con precisión el contexto construido en cada paso.

## Ejercicio 6: Prompt estructurado y autocrítica

```text
<rol>Actúa como analista de pruebas de software.</rol>
<contexto>Login web con correo y contraseña. La cuenta se bloquea después de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso qué puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>

[Mensaje de autocrítica]
Revisa tu tabla: ¿faltan casos límite como campos vacíos, correo sin @ o contraseña con espacios? Agrega los que falten e indica cuáles agregaste.