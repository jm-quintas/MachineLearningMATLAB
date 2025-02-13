# Creando un modelo.

![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-12%2022-36-42.png)
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-12%2022-37-13.png)

Una forma fácil de clasificar una observación es usar la misma clase que los ejemplos conocidos más cercanos. Esto se denomina ***modelo k-nearest neighbor (kNN)***. Puede ajustar un ***modelo kNN*** pasando una tabla de datos a la ***función fitcknn***.

```MatLab
mdl = fitcknn(data,"ResponseVariable");
```

La segunda entrada es el nombre de la variable de respuesta de la tabla (es decir, la clase que quiere que prediga el modelo). La salida es una variable que contiene el modelo ajustado. Las características y las clases de los 470 ejemplos conocidos se almacenan en la tabla features, que se encuentra en featuredata.mat.

### Tarea 1. Utilice la función fitcknn para ajustar un modelo a los datos almacenados en features. Las clases conocidas se almacenan en la variable llamada Character. Almacene el modelo resultante en una variable llamada knnmodel.

```MatLab
load featuredata.mat
features
testdata

knnmodel = fitcknn(features, "Character")
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-12%2022-50-45.png)
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-12%2022-51-00.png)
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-12%2022-51-22.png)

![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-12%2022-54-37.png)
