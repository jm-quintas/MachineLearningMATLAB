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
