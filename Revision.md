# Revisión.

El archivo MAT ***featuredata13letters.mat*** contiene una tabla (***features***) con las mismas características que antes. Sin embargo, ahora los datos incluyen muestras de 13 letras diferentes.

### Tarea 1. Utilice la función *gscatter* para representar las observaciones en *features*, con la relación de aspecto en el eje horizontal y la duración en el eje vertical, coloreadas por clase (almacenadas en la variable *Character*). No se evaluarán los límites del eje, pero puede que quiera experimentar con los límites para ampliar el grueso de las observaciones.

```MatLab
load featuredata13letters.mat
features
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-17%2019-05-16.png)

```MatLab
testdata
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-17%2019-09-38.png)

```MatLab
%Solución:
gscatter(features.AspectRatio, features.Duration, features.Character)
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-17%2019-14-38.png)

### Tarea 2. Utilice la función *fitcknn* para ajustar un modelo a los datos. Establezca la propiedad *NumNeighbors* en 5. Almacene el modelo en una variable llamada *knnmodel*. Utilice el modelo para predecir las clases para las observaciones almacenadas en *testdata*. Almacene las predicciones en una variable llamada *predictions*.

```MatLab
knnmodel = fitcknn(features, "Character", "NumNeighbors",5);
predictions = predict(knnmodel, testdata);
```

La tabla ***testdata*** contiene las clases conocidas de la variable ***Character***.

### Tarea 3. Calcule la tasa de clasificación errónea del modelo y cree una gráfica de confusión. Almacene la tasa de clasificación errónea en una variable llamada *misclass*.

```MatLab
misclass = sum(predictions ~= testdata.Character) / numel(predictions)
```
```
misclass = 0.7692
```

```MatLab
confusionchart(testdata.Character, predictions);
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-17%2019-31-07.png)
