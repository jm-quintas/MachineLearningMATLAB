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
![]()

```MatLab
iscorrect = predictions == testdata.Character
```
![]()

