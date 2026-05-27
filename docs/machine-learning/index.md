---  
title: Indice Machine Learning
summary: Tabla de contenidos y breve descripción del área
new: true
keywords: machine learning,intro,begginers
author: arces
order: 0
sidebar_title: Indice
external_links:
  "Adicionales": http://ema.cri-info.cm/wp-content/uploads/2019/07/2019BurkovTheHundred-pageMachineLearning.pdf
  GitHub: "https://github.com/asiffer/mkdocs-shadcn"

#extra_javascript:
#  - js/custom-script.js

---

En esta sección introduciremos el tema de "Machine Learning", qué es, para qué y por qué. 

Este índice pretende explicar conceptos que luego en el analisis de los *papers* nombraremos. Es de utilidad tenerla cerca para facilitar la lectura del analisis

# ¿Qué es *Machine Learning*?

En una sola palabra: **algoritmo**. En esencia, son una serie de reglas basadas en una colección de ejemplos de la situación a resolver, por eso, a veces escuchamos que **la calidad del contenido de los datos** es mas importante que el algoritmo en sí. 

~{diagram}(ml-diagram-02.svg)

al ser fórmulas matemáticas, si mis datos son érroneos o bien o estan incompletos, esto se reflejará en el resultado de mi modelo. 


# ¿Para qué sive *Machine Learning*?
Bueno, es la base de todo el desarrollo de la inteligencia artificial. En el mundo moderno en el que vivimos, los datos estan por todos lados, por sí solos, no son nada mas que datos. Pongamos un ejemplo: 

~{diagram}(ml-diagram-03.svg)

Tux es un estudiante, que durante su semana de examenes anotó cuántas horas estudió y la calificación obtenida. Entonces, quiere saber si el hecho de estudiar mas horas lo ayudará a mejorar sus notas. 

Miremos los datos:

    Semana 1: 2 horas → 4

    Semana 2: 3 horas → 5

    Semana 3: 1 hora → 8 ← ¡este se sale de lo esperado!

    Semana 4: 3 horas → 7

En la semana 3, estudió menos pero sacó una nota más alta.

Esto nos dice que la relación no es perfectamente lineal (no siempre estudiar más = mejor nota). Puede que haya otros factores (motivación, facilidad del examen, suerte, etc.).

### ¿Se puede hacer un modelo?

Sí. Aunque no sea perfecto, podemos intentar encontrar una recta (regresión lineal) para ver si existe una tendencia general.

Dicho de forma sencilla:

    "Si cambio X, ¿cómo cambia Y?"

Ejemplo:

    X = Horas de estudio

    Y = Nota del examen

Un modelo estadístico intenta encontrar un patrón general en los datos, aunque no siempre lo logre perfectamente.

En este caso, estudiar más generalmente ayuda, pero no garantiza una mejor nota.

Hay excepciones (como la semana 3), que pueden deberse a otros factores (tema del examen, estado de ánimo, etc.).

Ese primer modelo estadístico es el primer paso para construir sistemas inteligentes porque aprende de los datos, encuentra patrones y puede hacer predicciones. 

En modelos más avanzados, como los que usan las IA, se pueden tener muchas variables: sueño, estrés, comida, concentración, etc. Pero todo comienza con algo simple como esto.

En resumen, *Machine Learning* sirve para encontrar la mejor FÓRMULA que represente la mejor recta que se ajuste a mis datos. 

Mas adelante desarrollaremos conceptos matemáticos relacionados. 

# ¿Para qué usar *Machine Learning*?

En la programación normal, tú le dices a la computadora exactamente qué hacer con instrucciones claras.

Ejemplo tradicional:

Si estás haciendo un programa para saber si un email es spam, escribes reglas como:

    Si el correo contiene "dinero rápido" → marcar como spam

    Si el correo tiene muchos signos de exclamación → marcar como spam

Esto funciona, pero es limitado:

No se pueden escribir todas las reglas posibles porque algunas se contradicen.

En cambio, con los modelos de machine learning, en lugar de escribir reglas, haces que la computadora aprenda por sí misma observando muchos ejemplos.


## Glosario de conceptos fundamentales en Machine Learning

/// details | a
/// details | b
/// details | c
/// details | d
/// details | e
/// details | f
/// details | g
/// details | h
/// details | i
/// details | j
/// details | k
/// details | l
/// details | m
/// details | n
/// details | o
/// details | p
/// details | q
/// details | r
/// details | s
/// details | t
/// details | u
/// details | v
/// details | w
/// details | x
/// details | y
/// details | z




### Vector de Características
---


Es una lista ordenada de datos (también llamada vector) que describe un ejemplo. Cada dato en esa lista se llama característica o feature, y representa alguna propiedad del ejemplo.
Por ejemplo:


~{diagram}(ml-diagram-04.svg)

Todos los ejemplos del conjunto de datos tienen el mismo tipo de características en el mismo orden
///



### Dimensión
---

La dimensión es el número de características que tiene un vector. Osea, la cantidad de elementos que tenga mi lista. 

~{diagram}(ml-diagram-04.svg)

En el ejemplo de arriba, se dice que el vector *"tiene dimensión 3*"


### Apredizaje Supervisado
---

Es cuando el algoritmo aprende a partir de ejemplos que ya tienen la respuesta correcta. A estos ejemplos se les llama **etiquetados**. El objetivo es predecir una etiqueta para un nuevo dato. Por ejemplo: 

Si se quiere predecir el precio de una casa:
-   Le pasas al modelo datos de muchas casas con características como tamaño, número de habitaciones y ubicación, junto con su precio real. 
- El modelo analiza esos ejemplos, aprende las relaciones (descubre patrones entre las entradas y las salidas (los precios reales de las casas)) entre las características y el precio, y luego puede estimar el valor de una nueva casa usando esas mismas variables. 
 
Se llama "supervisado" porque el aprendizaje se guía usando datos etiquetados, es decir, con las respuestas conocidas.

### Aprendizaje No Supervisado
---

cuando el modelo aprende a partir de datos sin etiquetas, es decir, no conoce la respuesta correcta. En lugar de predecir algo específico, el objetivo es descubrir patrones ocultos o agrupar los datos.

Por ejemplo:

    Si se quiere agrupar canciones parecidas en Spotify:

        El modelo recibe datos como ritmo, duración, energía…

        No sabe el género ni la emoción, pero agrupa las canciones en categorías según sus similitudes.

        Esto se llama clustering (agrupamiento).

Este tipo de aprendizaje se usa para:

    Agrupar clientes similares

    Detectar comportamientos anómalos

    Comprimir o reducir datos


### Aprendizaje Semi-Supervisado
---

Es una combinación entre el aprendizaje supervisado y el no supervisado.
El modelo recibe unos pocos ejemplos con etiqueta (respuesta conocida) y muchos sin etiqueta, y aprende usando ambos tipos de datos.

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

        Prueba mover una pierna → se cae → recibe castigo

        Prueba otra forma → avanza → recibe recompensa

        Con el tiempo, aprende una estrategia (o política) que maximiza su éxito

Este tipo de aprendizaje se usa para:

    Jugar videojuegos (como AlphaGo o ajedrez)

    Robótica

    Control de tráfico o logística


### Escalar
---
Es simplemente, un número

### Conjunto
---
Colección de elementos únicos, sin importar el orden. Se escribe con letras como 𝒮 o {x₁, x₂, x₃}.

-   Puede ser finito: {1, 2, 3}

-   O infinito: [0, 1] = todos los números reales entre 0 y 1.

### Sigma (∑)
---

Representa la suma de una serie de valores.

    Ejemplo:
    ∑i=14xi=x1+x2+x3+x4
    i=1∑4​xi​=x1​+x2​+x3​+x4​

### PI (∏)
---

Representa el producto de varios valores.

    Ejemplo:
    ∏i=14xi=x1⋅x2⋅x3⋅x4
    i=1∏4​xi​=x1​⋅x2​⋅x3​⋅x4

### Derivada
---

Existen diferentes técnicas para calcular la derivada de una función, pero el propósito es indiciar cómo una función cambia su valor cuando cambia x.

La derivada en una gráfica representa la pendiente o el cambio de un valor con respecto al eje x (en este caso, el mes). Para ilustrar la idea de derivada, lo ideal es:

- Tomar una función continua (por ejemplo, f(x)=x2f(x)=x2)
- Dibujar su curva
- Dibujar una recta tangente en un punto específico
- Mostrar cómo la pendiente (derivada) cambia

<div id="main" style="width: 100%; height: 400px;"></div>
<script src="https://cdn.jsdelivr.net/npm/echarts@5.4.2/dist/echarts.min.js"></script>
<script>
  const chart = echarts.init(document.getElementById("main"));

  const x0 = 1.5;
  const slope = 2 * x0;
  const y0 = x0 * x0;

  const fx = [], tangent = [];
  for (let x = -3; x <= 3; x += 0.1) {
    const xRounded = Math.round(x * 10) / 10;
    fx.push([xRounded, xRounded ** 2]);
    tangent.push([xRounded, slope * (xRounded - x0) + y0]);
  }

  chart.setOption({
    title: { text: "f(x) = x² y su derivada", left: "center" },
    tooltip: { trigger: "axis" },
    xAxis: { type: "value" },
    yAxis: { type: "value" },
    series: [
      { name: "f(x) = x²", type: "line", data: fx },
      {
        name: "Tangente",
        type: "line",
        data: tangent,
        lineStyle: { type: "dashed", color: "#EF4444" }
      }
    ]
  });
</script>


### Gradiente
---

El gradiente de una función con varias variables es un vector que indica en qué dirección aumenta más rápidamente la función. 

Ejemplo:    
    Si f(x₁, x₂) = 2x₁ + 3x₂,
entonces:

    ∇f=[∂f/∂x1,∂f/∂x2]=[2,3]

Una analogía del mundo real sería: Estás en una colina y tienes los ojos vendados.
Tocas el suelo y sientes que la tierra sube más hacia la derecha que hacia el frente.
El gradiente es como una brújula que te dice:

*“¡Gira hacia el noreste y camina! Allí subirás más rápido.”*

### Clasificación 
---

La clasificación consiste en asignar una etiqueta o clase a un dato nuevo.

El conjunto de posibles etiquetas es finito (por ejemplo: "perro" o "no perro").
El objetivo es predecir a qué categoría pertenece un nuevo ejemplo.

Tipos:

- Binaria: Solo dos clases posibles (ej. enfermo/sano, spam/no spam).

- Multiclase: Tres o más clases (ej. tipo de flor: iris setosa, iris versicolor, iris virginica).

El modelo aprende a separar clases.

### Regresión
---

La regresión busca predecir un valor numérico continuo en lugar de una etiqueta.

- La salida es un número real (por ejemplo, 12.5, 154.3).
- Se usa cuando lo que queremos predecir no es una categoría, sino una cantidad(un número).

El modelo aprende la reclación entre variables para estimar un valor numérico.

### Aprendizaje basado en Modelos
---

Estos algoritmos usan los datos de entrenamiento para construir un modelo con parámetros aprendidos. Una vez que el modelo está construido, los datos de entrenamiento pueden descartarse, ya que el modelo encapsula el conocimiento aprendido

Ejemplo clásico: SVM (Support Vector Machine), donde se aprenden parámetros como ww y bb.

### Aprendizaje basado en instancias
---
No construyen un modelo general, sino que utilizan directamente todo el conjunto de datos de entrenamiento para hacer predicciones. Aquí, los datos se usan directamente durante la predicción, no se crea un modelo simplificado.

Cuando llega un nuevo ejemplo, se compara con las instancias de entrenamiento.

Ejemplo popular: k-Nearest Neighbors (kNN).

Para clasificar un nuevo punto, el algoritmo busca los k ejemplos más cercanos en el espacio de características.

La etiqueta que más se repite entre esos vecinos es la predicción.

### Aprendizaje Superficial
---

El modelo aprende directamente los parámetros a partir de las características originales de los datos. La mayoría de los algoritmos supervisados tradicionales son de esta categoría.

Ejemplos: regresión lineal, máquinas de soporte vectorial, árboles de decisión simples.

### Aprendizaje Profundo
--- 

Usa redes neuronales profundas con varias capas ocultas entre la entrada y la salida. Los parámetros del modelo se aprenden a partir de las salidas intermedias de las capas anteriores, no directamente de las características originales.

Esto permite aprender representaciones jerárquicas y complejas de los datos.

Ejemplos: redes neuronales convolucionales (CNN), redes recurrentes (RNN), transformers.


