# -AI-Decision-Tree-Classifier
Metodos de inteligencia artifical utilizando pandas, numpy, sklearn, matplotlib y seaborn

Los primeros pasos seran importar las librerias a jupyter notebook y carga la base de datos csv.

Limpieza de datos:
Se vusializa los tipos de datos, el tamnano de la base datos y verificar si existen datos nulos

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/443b2cb7-6be2-401d-8e86-711a5694f386)

Se seleccionaron tres variables aleatoriamente para generar los modelos, las cuales fueron (Buying, Person y safety) y se procedió a observar la distribución de los datos como se muestra en las imágenes. Así como también se tomó la variable “class” como target ya que muestra un desbalance en los datos.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/84208b1b-1ac5-413e-b0ca-9e1bca814a52)
![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/90bb8b28-6e88-4415-9b5e-54278fae6735)
![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/ae72fefe-7941-4427-95c6-6370266d7a21)
![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/72e20457-a19f-47aa-adaa-aaaff93fd4c7)


Se puede observar que la variable “class” tiene 1215 instancias en el atributo unacc desbalanceado de los demás atributos. Para una mejor visualización se muestra la siguiente grafica de barras.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/c1c02e75-69b0-40e0-9510-7528ce013d7f)

Se selecciona la variable "class" como "target: la cual tiene los valores mas distribuidos y se eliminan algunas variables para una mejor manipulacion de la data y realizar la prueba. Ya teniendo la base de datos solo con las variables seleccionadas se utiliza el código get.dummies() para convertir las variables categóricas en instancias numéricas. **Nota: El target sigue siendo una variable categorica**

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/0df24cc0-800c-43b9-8486-d9329d1934a9)

Ya teniendo las base de datos a modelar se procede con los datos con algotritomos de inteligencia artifial pirncipalmente de clasificacion

**Modelo de Kneighborsclassifier**
Primer modelo de clasificación, en este caso se utilizó de K de vecinos más cercanos para calcular la precisión del modelo de prueba utilizando un 30% de los datos y entrenamiento con un 70% de los datos. Obteniendo como resultado de 0.7847 de presión en de prueba y 0.7877 de precisión en entrenamiento como se muestra en la imagen. 

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/1a3411e8-1f5f-4579-8935-1cc8729e068f)
![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/0995898b-ae9f-4241-a682-38d29884e6db)


**Modelo de DecisionTreeClassifier**
Segiundo modelo de calisificacin el cual una vez ya entrnados los datis se procede a calcular el porcentaje de precisión de este modelo el cual dio como resultado 0.8133 de precisión y se imprime la matriz de confusión para validar que tanto se acertó y se equivocó el modelo

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/898f6837-b97e-45a6-bf6b-3ab9b8b39a3d)

Se realizo también una validación cruzada para verificar el modelo K de vecinos más cercanos, por lo que dio como resultado que el modelo no está sobre entrenado ya que los valores están en orden como se muestra en la imagen.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/6b5c8613-45fa-4c16-8890-163f9dc8e7f4)

para terminar se imprime el árbol de decisiones para una mejor visualización de las diferentes opciones que tomo el modelo de clasificación como mas importantes.

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/4922386e-0029-4080-baa5-f8b837045083)


**Modelo de Randomforest**
Segiundo modelo de calisificacin se separaron los modelos de entrenamiento y prueba, se agrego un estimador de 100 arboles de los cuales elegiría el mas conveniente y se imprimo el resultado obteniendo un 0.8171 de precisión 

![image](https://github.com/jolosjoel/-AI-Decision-Tree-Classifier/assets/45809759/f2493581-e118-41f9-b417-79c8a0b1ab0a)


**Conclusión:**

En conclusión, a la actividad el modelo que obtuvo mejor precisión fue el de RandomForest con 0.8171 de precisión en su clasificación. Las ventajas de este modelo son que genera una cantidad más grande de clasificaciones y al final elige el que por medio de votación es el mejor. La desventaja es que es un poco complicado para las personas observar 100 o más arboles e identificar la razón de por qué ese árbol fue elegido y por que es el mejor.  Por otro lado, el método de árboles de clasificación tiene la desventaja de no siempre dar el mejor resultado y la persona tiene que probar diferentes parámetros para encontrar el mejor y de los cuales existen muchas opciones. Pero la ventaja de este modelo es que al imprimir el árbol de clasificaciones puedes ver todas las ramas o clasificación del árbol con su porcentaje de asertividad, valores, así como el Gini o entropía ya sea su caso. 




