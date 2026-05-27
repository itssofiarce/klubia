---  
title: Indice Machine Learning
summary: Tabla de contenidos y breve descripción del área
new: true
keywords: machine learning,intro,begginers
author: arces
order: 0
sidebar_title: Indice

---

En esta sección introduciremos el tema de "Machine Learning", qué es, para qué y por qué. 

Este índice pretende explicar conceptos que luego en el análisis de los *papers* nombraremos. Es de utilidad tenerla cerca para facilitar la lectura del análisis.

# ¿Qué es *Machine Learning*?

En una sola palabra: **algoritmo**. En esencia, son una serie de reglas basadas en una colección de ejemplos de la situación a resolver, por eso, a veces escuchamos que **la calidad del contenido de los datos** es más importante que el algoritmo en sí. 
#~{diagram}(../assets/excalidraw/ml-diagram-02.svg)

Al ser fórmulas matemáticas, si mis datos son erróneos o están incompletos, esto se reflejará en el resultado de mi modelo. 


# ¿Para qué sirve *Machine Learning*?

Bueno, es la base de todo el desarrollo de la inteligencia artificial. En el mundo moderno en el que vivimos, los datos están por todos lados; por sí solos, no son nada más que datos. Pongamos un ejemplo: 
#~{diagram}(../assets/excalidraw/ml-diagram-03.svg)

Tux es un estudiante que durante su semana de exámenes anotó cuántas horas estudió y la calificación obtenida. Entonces, quiere saber si el hecho de estudiar más horas lo ayudará a mejorar sus notas. 

Miremos los datos:

    Semana 1: 2 horas - Nota: 4
    Semana 2: 3 horas - Nota: 5
    Semana 3: 1 hora - Nota: 8 [Dato atípico]
    Semana 4: 3 horas - Nota: 7

En la semana 3, estudió menos pero sacó una nota más alta. Esto nos dice que la relación no es perfectamente lineal (no siempre estudiar más = mejor nota). Puede que haya otros factores (motivación, facilidad del examen, suerte, etc.).

### ¿Se puede hacer un modelo?

Sí. Aunque no sea perfecto, podemos intentar encontrar una recta (regresión lineal) para ver si existe una tendencia general.

Dicho de forma sencilla:

    "Si cambio X, ¿cómo cambia Y?"

Ejemplo:

    X = Horas de estudio
    Y = Nota del examen

Un modelo estadístico intenta encontrar un patrón general en los datos, aunque no siempre lo logre perfectamente. En este caso, estudiar más generalmente ayuda, pero no garantiza una mejor nota. Hay excepciones (como la semana 3), que pueden debido a otros factores (tema del examen, estado de ánimo, etc.).

Ese primer modelo estadístico es el primer paso para construir sistemas inteligentes porque aprende de los datos, encuentra patrones y puede hacer predicciones. 

En modelos más avanzados, como los que usan las IA, se pueden tener muchas variables: sueño, estrés, comida, concentración, etc. Pero todo comienza con algo simple como esto.

En resumen, *Machine Learning* sirve para encontrar la mejor FÓRMULA que represente la mejor recta que se ajuste a mis datos. 

Más adelante desarrollaremos conceptos matemáticos relacionados. 


# ¿Por qué usar *Machine Learning*?

En la programación normal, tú le dices a la computadora exactamente qué hacer con instrucciones claras.

Ejemplo tradicional: Si estás haciendo un programa para saber si un email es spam, escribes reglas como:

    Si el correo contiene "dinero rápido" -> marcar como spam
    Si el correo tiene muchos signos de exclamación -> marcar como spam

Esto funciona, pero es limitado: no se pueden escribir todas las reglas posibles porque algunas se contradicen. En cambio, con los modelos de machine learning, en lugar de escribir reglas, haces que la computadora aprenda por sí misma observando muchos ejemplos.


# Glosario de conceptos fundamentales en Machine Learning

/// details | Glosario por Letras
* **A-Z:** Utiliza las secciones desplegables a continuación para explorar los términos.
///

### Vector de Características
---
Es una lista ordenada de datos (también llamada vector) que describe un ejemplo. Cada dato en esa lista se llama característica o feature, y representa alguna propiedad del ejemplo.

Por ejemplo:
#~{diagram}(../assets/excalidraw/ml-diagram-04.svg)

Todos los ejemplos del conjunto de datos tienen el mismo tipo de características en el mismo orden.


### Dimensión
---
La dimensión es el número de características que tiene un vector. O sea, la cantidad de elementos que tenga mi lista. 
#~{diagram}(../assets/excalidraw/ml-diagram-04.svg)

En el ejemplo de arriba, se dice que el vector *"tiene dimensión 3"*.


### Aprendizaje Supervisado
---
Es cuando el algoritmo aprende a partir de ejemplos que ya tienen la respuesta correcta. A estos ejemplos se les llama **etiquetados**. El objetivo es predecir una etiqueta para un nuevo dato. Por ejemplo: 

Si se quiere predecir el precio de una casa:

* Le pasas al modelo datos de muchas casas con características como tamaño, número de habitaciones y ubicación, junto con su precio real. 
* El modelo analiza esos ejemplos, aprende las relaciones (descubre patrones entre las entradas y las salidas) entre las características y el precio, y luego puede estimar el valor de una nueva casa usando esas mismas variables. 
 
Se llama "supervisado" porque el aprendizaje se guía usando datos etiquetados, es decir, con las respuestas conocidas.


### Aprendizaje No Supervisado
---
Cuando el modelo aprende a partir de datos sin etiquetas, es decir, no conoce la respuesta correcta. En lugar de predecir algo específico, el objetivo es descubrir patrones ocultos o agrupar los datos.

Por ejemplo:

    Si se quiere agrupar canciones parecidas en Spotify:
        El modelo recibe datos como ritmo, duración, energía…
        No sabe el género ni la emoción, pero agrupa las canciones en categorías según sus similitudes.
        Esto se llama clustering (agrupamiento).

Este tipo de aprendizaje se usa para:

* Agrupar clientes similares
* Detectar comportamientos anómalos
* Comprimir o reducir datos


### Aprendizaje Semi-Supervisado
---
Es una combinación entre el aprendizaje supervisado y el no supervisado. El modelo recibe unos pocos ejemplos con etiqueta (respuesta conocida) y muchos sin etiqueta, y aprende usando ambos tipos de datos.

Por ejemplo:

    Quieres entrenar un modelo para reconocer fotos de perros y gatos.
        Tienes 100 fotos con etiqueta (dices si es perro o gato)
        Y tienes 5,000 fotos sin etiqueta
    El modelo aprende mejor que si solo usara las 100 fotos etiquetadas, porque aprovecha la estructura de los datos no etiquetados.

Esto es útil cuando es caro o difícil conseguir etiquetas, como en imágenes médicas o análisis de texto.


### Aprendizaje por Refuerzo
---
En este tipo de aprendizaje, el modelo interactúa con un entorno y aprende de las consecuencias de sus acciones. No tiene ejemplos con respuesta, sino que recibe recompensas o castigos según cómo actúe.

Por ejemplo:

    Un robot que aprende a caminar:
        Prueba mover una pierna -> se cae -> recibe castigo
        Prueba otra forma -> avanza -> recibe recompensa
        Con el tiempo, aprende una estrategia (o política) que maximiza su éxito

Este tipo de aprendizaje se usa para:

* Jugar videojuegos (como AlphaGo o ajedrez)
* Robótica
* Control de tráfico o logística


### Escalar
---
Es simplemente, un número.


### Conjunto
---
Colección de elementos únicos, sin importar el orden. Se escribe con letras como $S$ o $\{x_1, x_2, x_3\}$.

* Puede ser finito: $\{1, 2, 3\}$
* O infinito: $[0, 1]$ = todos los números reales entre 0 y 1.


### Sigma ($\sum$)
---
Representa la suma de una serie de valores.

Ejemplo:
$$\sum_{i=1}^{4} x_i = x_1 + x_2 + x_3 + x_4$$


### PI ($\prod$)
---
Representa el producto de varios valores.

Ejemplo:
$$\prod_{i=1}^{4} x_i = x_1 \cdot x_2 \cdot x_3 \cdot x_4$$


### Derivada
---
Existen diferentes técnicas para calcular la derivada de una función, pero el propósito es indicar cómo una función cambia su valor cuando cambia $x$.

La derivada en una gráfica representa la pendiente o el cambio de un valor con respecto al eje $x$. Para ilustrar la idea de derivada, lo ideal es:

* Tomar una función continua (por ejemplo, $f(x) = x^2$)
* Dibujar su curva
* Dibujar una recta tangente en un punto específico
* Mostrar cómo la pendiente (derivada) cambia
