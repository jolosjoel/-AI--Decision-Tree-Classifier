# AI Decision Tree Classifier

Métodos de inteligencia artificial utilizando pandas, numpy, sklearn, matplotlib y seaborn.

Los primeros pasos serán importar las librerías a Jupyter Notebook y cargar la base de datos CSV.

## Limpieza de datos

Se visualizan los tipos de datos, el tamaño de la base de datos y se verifica la presencia de datos nulos.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/443b2cb7-6be2-401d-8e86-711a5694f386)

## Selección de variables

Se seleccionaron tres variables aleatoriamente para generar los modelos: Buying, Person y Safety. Además, se observa la distribución de los datos. La variable "class" se eligió como target debido a un desbalance en los datos.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/84208b1b-1ac5-413e-b0ca-9e1bca814a52)
![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/90bb8b28-6e88-4415-9b5e-54278fae6735)
![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/ae72fefe-7941-4427-95c6-6370266d7a21)
![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/72e20457-a19f-47aa-adaa-aaaff93fd4c7)

## Análisis de la variable "class"

La variable "class" tiene 1215 instancias en el atributo "unacc" desbalanceado con respecto a los demás atributos. Se muestra una gráfica de barras para una mejor visualización..

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/c1c02e75-69b0-40e0-9510-7528ce013d7f)

## Preparación de los datos

Se selecciona la variable "class" como el target y se eliminan algunas variables para facilitar la manipulación de los datos. Luego, se utiliza el código get.dummies() para convertir las variables categóricas en instancias numéricas. **Nota: El target sigue siendo una variable categórica en este caso la variable "class".**

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/0df24cc0-800c-43b9-8486-d9329d1934a9)

## Modelos de Inteligencia Artificial

### Modelo de KNeighborsClassifier

Se utiliza el modelo de K vecinos más cercanos para calcular la precisión del modelo de prueba con un 30% de los datos y entrenamiento con un 70% de los datos. Se obtiene una precisión de 0.7847 en prueba y 0.7877 en entrenamiento.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/1a3411e8-1f5f-4579-8935-1cc8729e068f)
![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/0995898b-ae9f-4241-a682-38d29884e6db)


### Modelo de DecisionTreeClassifier

Se entrena el modelo de árbol de decisiones y se calcula una precisión de 0.8133. Se imprime la matriz de confusión para evaluar el rendimiento del modelo.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/898f6837-b97e-45a6-bf6b-3ab9b8b39a3d)

Se realiza una validación cruzada para verificar que el modelo de K vecinos más cercanos no esté sobreentrenado.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/6b5c8613-45fa-4c16-8890-163f9dc8e7f4)

Se imprime el árbol de decisiones para una mejor visualización de las diferentes opciones tomadas por el modelo de clasificación.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/4922386e-0029-4080-baa5-f8b837045083)


### Modelo de RandomForestClassifier

Se separan los datos de entrenamiento y prueba, y se utiliza un estimador de 100 árboles. Se obtiene una precisión de 0.8171.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/f2493581-e118-41f9-b417-79c8a0b1ab0a)


## Conclusión

En resumen, el modelo que obtuvo la mejor precisión fue el de RandomForest con un 0.8171 de precisión en su clasificación. Esta opción tiene la ventaja de generar múltiples clasificaciones y elegir la mejor a través de la votación. La desventaja es que puede ser complicado para las personas comprender por qué se elige un árbol en particular.





