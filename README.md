# Agente recomendador de películas.

Se desarrollará un agente recomendador que sea capaz de recomendar películas a usuarios dependiendo de la calificación que tuvieron. Se entrenará un modelo de clasificación de KNeighbors que será capaz que predecir los géneros como acción, drama, romance, ciencia ficción e historia con respecto a los atributos de los usuarios como edad, años de estudio, ciudad de residencia, número de películas vistas el año pasado. El entrenamiento del modelo se desarrolló con el conjunto de datos correspondiente. 

Las variables (atributos) en el conjunto de datos son:

1. Edad: entera en rango [16,98].

2. Años de estudio; entera en rango [6,26].

3. Ciudad de residencia: entera en rango [1,49].

4. Número de películas vista el año pasado 8de cualquier categoría o clase): entera en rango [1,64].

Los atributos Acción, Drama, Romance, Ciencia ficción, Histórica, se refieren a la calificación (estrellas) que cada participante da a esos cinco géneros de películas. Rango: [0.5].

Se cargaron las librerías necesarias para cargar los datos, visualizarlos, dividir el conjunto de datos en entrenamiento y prueba, el agente y evaluar la calidad del mismo. Los datos están compuestos por 9 atributos y 1807 entradas de la cuales ninguna tiene valores nulos y todas son de tipos entero. Se hizo la separación de las características X y los valores objetivo y, luego, se dividió en conjunto de entrenamiento y prueba en 80% (**X_train**, **X_test**) y 20% (**y_train**, **y_test**) respectivamente.

Entrenamos el modelo con el conjunto de entramiento y calculamos la predicción con los valores objetivo de prueba (y_test). Una vez hecho el entrenamiento y la predicción, desarrollamos el índice de exactitud que tuvo el modelo.

Ponemos lo criterios de exactitud en una tabla:

| Género           | Exacitud     |
| -------------   |:-------------:|
| Acción          | 0.7735        |
| Drama           | 0.7044        |
| Romance         | 0.6768        |
| Ciencia ficción | 0.5782        |
| Historia        | 0.6077        |

La mejor exactitud en los géneros fue de acción y drama. Podríamos suponer que esto se debe a que los usuarios califican mejor estos géneros a comparación con los otros. Además de que el conjunto de datos no está grande y necesitaríamos más valores para aumentar la exactitud del modelo.

Hay al menos dos perspectivas, opten por la que les resulte más atractiva:

1. Con base en los cuatro primeros atributos listados, recomendar qué tipo de película (Acción, Drama, Romance, Ciencia ficción, Histórica) preferiría un nuevo usuario. Este nuevo usuario estará caracterizado por su edad, años de estudio, ciudad de residencia y número de pelícuas vistas el año pasado.

2. Con base en los cuatro primeros atributos listados, recomendar un orden de preferencia (Acción, Drama, Romance, Ciencia ficción, Histórica) para un nuevo usuario. Este nuevo usuario estará caracterizado por su edad, años de estudio, ciudad de residencia y número de pelícuas vistas el año pasado.