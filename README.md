# Introducción

Propietario: Carlos Castelo
Verificación: Verificada
Etiquetas: Machine learning, Teoria
Fecha: 23 de febrero de 2024
Fecha de creación: 23 de febrero de 2024 11:10

> **Consejo:** Para aprender sobre Machine Learning, es importante comenzar con los fundamentos de la matemática y la estadística. La comprensión de los conceptos básicos de álgebra lineal, cálculo y probabilidad será esencial. Luego, puedes adentrarte en los algoritmos de aprendizaje supervisado y no supervisado, y practicar con conjuntos de datos reales para comprender cómo funcionan estos algoritmos en situaciones prácticas. Recuerda que la práctica constante y la curiosidad son clave en esta área de estudio.
> 

El aprendizaje automático o mejor conocido como machine learning son aquellos algoritmos que se ejecutan computacionalmente para aprender automáticamente en base a datos proporcionados. Se trata de programas capaces de predecir comportamientos a partir de los datos suministrados en forma de ejemplos.

El Machine learning puede dividirse en algoritmos de aprendizaje supervisado, semi-supervisado y en algoritmos de aprendizaje no supervisados. Estos tipos de algoritmos se empezó a utilizar en problemas de predicción de complejos donde los modelos estadísticos clásicos no eran muy buenos como, por ejemplo: reconocimiento de la voz humana, reconocimiento de imágenes, predicciones de series temporales no lineales, reconocimiento de texto escrito etc.

El aprendizaje supervisado utiliza ejemplos conocidos previamente para obtener inferencias por medio de una función que establece una correspondencia entre las entradas y las salidas del sistema.

## Aprendizaje Supervisado – Problemas de regresión

En los problemas de regresión la variable del sistema, así como su respuesta de salida es una variable **cuantitativa (numérica continua).** Es decir; se espera que los problemas resueltos con este tipo de algoritmos sus variables sean numéricas y no categóricas.

<aside>
💡 **Objetivo-** El objetivo del aprendizaje supervisado en problemas de regresión es predecir las respuestas que habrá en el futuro con nuevas variables de entrada.

**NOTA-** *Para realizar regresiones lineales con variables categóricas es necesario convertirlas a variables numéricas. Esto se debe a que los modelos de regresión lineal están basados en operaciones matemáticas que requieren valores numéricos para las variables predictoras.*

</aside>

El aprendizaje supervisado  en problemas de regresión generaliza las respuestas sobre datos no observados, utilizando para ello ejemplos observados previamente. En el caso de los problemas de regresión la variable respuesta y es una variable numérica continua.
****

## **Aprendizaje Supervisado – Problemas de clasificación**

En los problemas de clasificación, el aprendizaje supervisado utiliza ejemplos conocidos para inferir la etiqueta(clasificar) de los vectores de entrada eligiendo una de entre varias categorías o clases. En este tipo de algoritmo a diferencia de los problemas de regresión, las variables pueden ser de tipo categórico o de tipo numérico.

<aside>
💡 **Objetivo** - El objetivo en problemas de clasificación es identificar a qué categoría pertenece una nueva observación utilizando para ello una serie de observaciones y categorías conocidas previamente.

</aside>

El aprendizaje supervisado en problemas de clasificación generaliza utilizando para ello ejemplos conocidos. En el caso de los problemas de clasificación la variable respuesta y es una variable con 2 o más categorías o clases.

## **Conjuntos de entrenamiento, test y validación cruzada**

El objetivo principal de cualquier modelo de machine learning es su capacidad de generar situaciones del futuro en función de los datos históricos observados.

**-Fase de test 20%:**
la fase de test en realidad es un conjunto que está formado por un subconjunto de los datos de entrenamiento.

**-Fase de entrenamiento 80%:**
En la fase de entrenamiento se extraen las características o variables relevantes de los datos de entrada para construir el modelo.

**-Fase de predicción:**
Durante la fase de predicción se realiza una extracción de variables similar sobre las que se aplica el modelo previamente entrenado para obtener un resultado estimado.

<aside>
💡 Las métricas obtenidas con los datos de entrenamiento **omitiendo** la fase de prueba no son buenos indicadores del comportamiento a futuro, un modelo puede ser capaz de tener un error mínimo en datos históricos (conjunto de entrenamiento) y no ser capaz de predecir bien los valores a futuro.

</aside>

En el procedimiento de dividir los datos se utiliza para crear un modelo que es evaluado utilizando el conjunto de test. Normalmente se utiliza un 80% de los datos para crear el conjunto de entrenamiento y un 20% para generar el conjunto de test.

<aside>
💡 **Es importante remarcar que para que este método sea riguroso, no se pueden utilizar observaciones o instancias del conjunto de test para crear el clasificador.**

</aside>

**-Validación cruzada K-fold**

La técnica de validación cruzada es el estándar de la industria para estimar el rendimiento de los modelos. Esta técnica también es conocida como k-fold, donde k es un valor que indica que se han dividido los datos históricos en k particiones separadas llamadas folds o conjuntos.
Aunque k puede ser cualquier número, lo habitual es utilizar k=5 o k=10. Esto es debido a que la evidencia empírica indica que hay poco beneficio en utilizar más de 10 folds.

El conjunto de entrenamiento en aprendizaje supervisado proporciona un error que debe de ser evaluado con cautela. Es más riguroso evaluar a los modelos utilizando un conjunto separado e independiente llamado conjunto de test. Esta separación entre conjunto de test y entrenamiento se puede repetir a lo largo de los datos disponibles utilizando la técnica de validación cruzada
