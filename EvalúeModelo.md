# Evalúe el modelo.

¿En qué medida es bueno el modelo kNN? La tabla ***testdata*** incluye la clase conocida para las observaciones de prueba. Puede comparar las clases conocidas con las predicciones del modelo kNN para ver hasta qué punto el modelo funciona bien con datos nuevos.

### Tarea 1. Utilice el operador == para comparar *predictions* con las clases conocidas (almacenadas en la variable *Character* en la tabla *testdata*). Almacene el resultado en una variable llamada *iscorrect*.

```MatLab
load featuredata.mat
testdata
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-17%2015-21-32.png)

```MatLab
knnmodel = fitcknn(features,"Character","NumNeighbors",5);
predictions = predict(knnmodel,testdata)
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-17%2015-21-53.png)

```MatLab
iscorrect = predictions == testdata.Character
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-17%2015-22-04.png)

### Tarea 2. Calcule la proporción de predicciones correctas dividiendo el número de predicciones correctas entre el número total de predicciones. Almacene el resultado en una variable llamada *accuracy*. Puede utilizar la función *sum* para determinar el número de predicciones correctas y la función *numel* para determinar el número total de predicciones.

```MatLab
accuracy = sum(iscorrect)/numel(predictions)
```
```
accuracy = 0.8000
```

En lugar de la precisión (la proporción de predicciones correctas), una métrica comúnmente utilizada para evaluar un modelo es la tasa de clasificación errónea (la proporción de predicciones incorrectas).

### Tarea 3. Utilice el operador ~= para determinar la tasa de clasificación errónea. Almacene el resultado en una variable llamada *misclassrate*.

```MatLab
iswrong = predictions ~= testdata.Character
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-17%2015-38-41.png)

```MatLab
misclassrate = sum(iswrong)/numel(predictions)
```
```
misclassrate = 0.2000
```

La tasa de precisión y de clasificación errónea ofrece un único valor para el rendimiento global del modelo, pero puede ser útil ver un desglose más detallado de las clases que el modelo confunde. Una ***matriz de confusión*** muestra el número de observaciones por cada combinación de clase real y predicha.

![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-17%2015-40-36.png)

Una ***matriz de confusión*** se visualiza normalmente sombreando los elementos según su valor. A menudo, los elementos diagonales (las clasificaciones correctas) están sombreados en un color y el resto de elementos (las clasificaciones incorrectas) en otro color. Puede visualizar una matriz de confusión utilizando la función ***confusionchart***.

```MatLab
confusionchart(ytrue,ypred);
```

Donde ***ytrue*** es un vector de las ***clases conocidas*** e ***ypred*** es un vector de las ***clases predichas***.

### Tarea 4. Utilice la función *confusionchart* para comparar *predictions* con las etiquetas conocidas (almacenadas en la variable *Character* en la tabla *testdata*).

```MatLab
confusionchart(testdata.Character, predictions)
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-17%2015-48-26.png)
