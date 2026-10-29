# 1. ¿Qué es la IA? 🤖

## Definiciones de IA
*   **Inteligencia Artificial General (IAG):** Una máquina hipotética capaz de realizar cualquier tarea intelectual que un ser humano pueda llevar a cabo.
*   **IA estrecha (o específica):** Un sistema de IA diseñado para gestionar una tarea concreta, como el reconocimiento facial, los algoritmos de recomendación o jugar al ajedrez.

## Pilares fundamentales de la IA
La IA se define, por lo general, mediante dos características clave:

1.  **Autonomía:** La capacidad de realizar tareas en entornos complejos sin necesidad de una intervención constante por parte del usuario.
2.  **Adaptabilidad:** La capacidad de mejorar su rendimiento aprendiendo a partir de datos y experiencias.

## El concepto de «término maleta»
Marvin Minsky, uno de los pioneros de la IA, acuñó el término **«término maleta»** (*word suitcase*) para describir la IA, ya que este concepto encierra en su interior muchos significados distintos. Esto suele dar lugar a interpretaciones erróneas.

> [!TIP]
> En lugar de preguntarse si algo *es* IA, suele ser más útil plantearse **hasta qué punto** presenta características propias de la IA.

## La IA como disciplina
Es importante recordar que la IA es una **disciplina científica**, no simplemente un programa informático aislado.
*   **Uso correcto:** «Este sistema utiliza IA».
*   **Uso incorrecto:** «He construido una IA». (Del mismo modo que no dirías «he construido una biología» o «he comprado una física»).

---

# 2. Campos relacionados 🌐

| Campo | Descripción |
| :--- | :--- |
| **Aprendizaje automático** (*Machine Learning*) | Un subcampo de la IA que abarca sistemas que mejoran su rendimiento a medida que acumulan datos. |
| **Aprendizaje profundo** (*Deep Learning*) | Un subcampo especializado del aprendizaje automático basado en redes neuronales (que se tratará en el Tema 5). |
| **Ciencia de datos** | Un término general que engloba la IA, la estadística y el análisis de datos. |
| **Robótica** | El diseño de agentes físicos. Combina la IA, que actúa como «cerebro», con la ingeniería mecánica, que constituye el «cuerpo». |

### ¿Qué es un robot?
Un robot es una máquina equipada con:
1.  **Sensores:** Para percibir el entorno (por ejemplo, cámaras o micrófonos). 2.  **Actuadores:** Elementos que permiten interactuar con el entorno (por ejemplo, ruedas, motores, altavoces).

---

# 3. Filosofía de la IA 🦉

## El test de Turing
*   **Objetivo:** ¿Puede una máquina interactuar con un ser humano de forma lo suficientemente convincente como para resultar indistinguible de otra persona?
*   **Crítica:** Se centra exclusivamente en el **comportamiento** (resultados externos) y no en la **conciencia** (procesos internos).

## El argumento de la «habitación china»
*   **Autor:** John Searle (1980).
*   **La idea:** Una persona dentro de una habitación que sigue un manual de reglas para responder a caracteres chinos podría *parecer* que entiende chino ante alguien que está fuera; sin embargo, en realidad solo está siguiendo instrucciones mecánicas.
*   **Implicación:** Simular inteligencia no equivale a una comprensión biológica o auténtica.

## IA fuerte frente a IA débil
*   **IA fuerte:** Una máquina que posee realmente una mente, conciencia y capacidad de sentir.
*   **IA débil:** Una máquina que actúa como si fuera inteligente para resolver problemas, pero que carece de conciencia interna.

---
---

## **Lecturas recomendadas** 📚
*   **John McCarthy:** Considerado el «padre de la IA», acuñó el término en 1956. Es conocido por haber calificado el debate entre «IA fuerte» e «IA débil» como irrelevante para el progreso de la ingeniería en este campo.
*   ***The Mind's I***, de **Hofstadter y Dennett:** Una colección clásica de ensayos que exploran la naturaleza del «yo» y la conciencia.
*   ***Computing Machinery and Intelligence***, de **Alan Turing:** El artículo fundacional de 1950 en el que se presenta el «juego de la imitación».

> [!NOTA]
> Para consultar una lista completa de libros, artículos y vídeos sobre estos temas, visita nuestra [Guía maestra de recursos](RESOURCES.md).

---
---

## 2.1: Búsqueda y resolución de problemas

La IA clásica se basa en la premisa de que pensar equivale a realizar cálculos. Bajo este enfoque, la resolución de problemas no depende de la intuición, sino de algoritmos lógicos que exploran sistemáticamente un mapa de posibilidades. Por lo tanto, para que una máquina resuelva un problema, debemos traducirlo a un lenguaje matemático basado en los siguientes conceptos:

| Concepto | Definición |
|---|---|
| **Espacio de estados** | El «mapa» completo: el conjunto de todas las situaciones posibles en las que puede encontrarse el sistema. |
| **Transiciones** | Los movimientos o acciones permitidos que permiten al sistema pasar de un estado a otro. |
| **Costes** | El valor asociado a cada transición, como el tiempo, la distancia o la energía. El objetivo es minimizar el coste total. |

### Metodología de resolución de problemas

- **Estado inicial:** El punto de partida; por ejemplo, la posición actual en un sistema GPS.
- **Estado objetivo:** La meta final; por ejemplo, el destino.
- **Filtrado:** Identificación y eliminación de estados o acciones prohibidos que infringen las reglas (por ejemplo, evitar que el zorro se coma a la gallina).
- **Búsqueda automatizada:** Una vez definido el diagrama, el ordenador realiza una búsqueda automática para encontrar la ruta óptima.

### ¿Por qué fueron los juegos el primer campo de pruebas?

Durante las décadas de 1950 y 1960, la IA se centró en juegos como el ajedrez por tres razones:

- **Entornos cerrados:** Reglas rígidas sin eventos ni cambios inesperados, que ofrecen información completa.
- **Evaluación objetiva:** Es sencillo programar cuándo se ha alcanzado el éxito, es decir, el estado objetivo.
- **Prestigio y referencia (benchmarking):** Superar a los seres humanos en tareas «intelectuales» demostraba la potencia de las máquinas.

### Hitos históricos

- **Alan Turing (1936):** Introdujo la idea de que una máquina universal podría realizar cualquier tarea, siempre que contara con el algoritmo adecuado.
- **John McCarthy (1956):** Acuñó el término «inteligencia artificial» y propuso la Conjetura de McCarthy: cualquier aspecto de la inteligencia puede describirse con la suficiente precisión como para que una máquina pueda simularlo.

# III: Búsqueda y juegos

## 1. El concepto: Árboles de juego

Un juego puede visualizarse como un **árbol**:

- **Nodo raíz:** La posición actual del tablero.
- **Nodos hijos:** Todas las posiciones posibles resultantes de un movimiento legal.
- **Hojas (nodos terminales):** Estados en los que finaliza el juego: victoria, derrota o empate.

## 2. El algoritmo Minimax

Minimax es una estrategia lógica para juegos entre dos jugadores, como el ajedrez o el tres en raya, basada en la competencia directa:

- **MAX (Tú):** Buscas **maximizar** el valor del resultado, representado por una puntuación de +1.
- **MIN (Oponente):** El oponente busca **minimizar** el valor del resultado, representado por una puntuación de -1.
- **Lógica:** Para decidir qué movimiento realizar, la IA analiza el futuro asumiendo que el oponente siempre elegirá la opción más perjudicial para ti. El valor del nodo actual se determina propagando los valores hacia arriba, desde las hojas del árbol. ## 3. Limitaciones: Explosión combinatoria

El algoritmo Minimax puro resulta poco práctico para juegos complejos:

- **Ajedrez:** Cuenta con más de $10^{120}$ variaciones posibles. Analizar solo 10 movimientos hacia adelante requeriría examinar billones de nodos.
- **Heurística:** Dado que es imposible llegar hasta el final del árbol de decisiones, la búsqueda se detiene a una profundidad determinada —por ejemplo, cinco movimientos hacia adelante— y emplea una **función de evaluación heurística**. Esta función estima qué jugador se encuentra en una mejor posición, considerando factores como el material, la ubicación de las piezas y la disposición en el tablero.

## 4. Clasificación de juegos para la IA

No todos los juegos pueden resolverse de la misma manera. El algoritmo Minimax funciona mejor en juegos que presentan:

- **Información perfecta:** Ambos jugadores pueden ver el tablero al completo, como ocurre en el ajedrez o el Go.
- **Resultados deterministas:** No existe ningún componente de azar —como el lanzamiento de dados o el barajado de cartas—, tal como sucede en el tres en raya.

> **Punto clave:** Si un juego implica azar —como el póker o el Monopoly— o contiene información oculta, el Minimax puro resulta insuficiente. En tales casos, es necesario recurrir a la **probabilidad**, tema que abordaremos en el siguiente capítulo.

---
---

# El concepto: IA frente a la incertidumbre

**La IA, desde la década de 1960 hasta la de 1980,** fracasó en el mundo real porque se basaba en reglas rígidas (si ocurre A, entonces haz B). El mundo real es caótico, está lleno de «ruido» y plagado de incertidumbres. La IA moderna tiene éxito precisamente porque utiliza la probabilidad para gestionar dicha incertidumbre.

**Hoy en día,** la IA ha evolucionado: ha pasado de ser un «jugador de ajedrez perfecto» a convertirse en un «jugador experto» que siempre actúa a favor de las probabilidades.

Este fragmento es fundamental, ya que marca la transición de una «IA de laboratorio» (basada en reglas fijas) a una IA capaz de desenvolverse en el mundo real.

# Los tres pilares de este capítulo

Para que la IA pueda «comprender» el mundo real, necesita estas tres herramientas que estudiarás a continuación:

| Herramienta | Función práctica |
|---|---|
| Probabilidades y azar | La forma matemática de cuantificar la probabilidad de que algo ocurra (p. ej., ¿lloverá hoy?). |
| Teorema de Bayes | Cómo actualizar nuestras creencias al recibir nueva información (p. ej., si una prueba da positivo, ¿cuál es la probabilidad real de que esté enfermo?). |
| Clasificador bayesiano | Una técnica para categorizar datos automáticamente (p. ej., ¿es este correo electrónico *spam* o no?). |

# ¿Por qué es importante?

A diferencia de un árbol de decisión (donde todo es predecible), la IA en el mundo real se enfrenta a:

- **Información incompleta:** No vemos todas las cartas de nuestro oponente.
- **Sensores con ruido:** La cámara de un vehículo autónomo puede estar sucia o haber niebla.
- **Resultados no deterministas:** Una acción no siempre produce el mismo resultado.

---
---

# 1. Aprendizaje frente a programación

La diferencia fundamental radica en **quién crea las reglas**:

- **Programación tradicional:** Un ser humano escribe reglas lógicas. 
> Ejemplo: «Si el correo electrónico contiene la palabra «GRATIS», es *spam*».

- **Aprendizaje automático (*machine learning*):** Un ser humano proporciona datos a la máquina, y esta descubre los patrones por sí misma. 
> Ejemplo: 10 000 correos electrónicos marcados como **spam** o **deseados**.

# 2. ¿Por qué es esto la clave de la inteligencia?

Tanto en los seres humanos como en las máquinas, la inteligencia no es estática. El aprendizaje permite:

- **Adaptabilidad:** Mejorar el rendimiento a medida que se dispone de más datos.
- **Generalización:** Tomar decisiones correctas ante datos que la máquina nunca ha visto antes.

# 3. Hoja de ruta del capítulo

| Sección | Enfoque práctico |
|---|---|
| **I. Tipos de aprendizaje** | Distinguir entre aprendizaje supervisado, no supervisado y por refuerzo. |
| **II. Vecino más cercano** | Clasificar algo simplemente observando lo que tiene a su alrededor, basándose en la proximidad. |
| **III. Regresión** | Predecir un valor numérico, como el precio de una vivienda, a partir de distintas variables. |

# 4. Un adelanto: El modelo y los datos

En el aprendizaje automático (*machine learning*), siempre hablamos de un **modelo**. Imagina el modelo como un *estudiante* y los datos como su *libro de texto*.

El éxito de la IA depende de:

- **La calidad de los datos:** Si los datos están sesgados o contienen errores, la IA aprenderá esos mismos errores.
- **La capacidad del algoritmo:** Qué tan bien puede el «estudiante» descubrir la lógica oculta en los números.

---
---
