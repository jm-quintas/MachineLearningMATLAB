# Extraiga características (Calcular características).

Una ***característica es simplemente un valor calculado a partir de la señal***, como su duración.

### Tarea 1. Calcule el tiempo que se tarda en escribir la letra extrayendo el último valor de letter.Time y almacenando el resultado en una variable llamada dur.

```MatLab
letter = readtable("M.txt");
letter.X = letter.X*1.5;
letter.Time = (letter.Time - letter.Time(1))/1000
plot(letter.X,letter.Y)
axis equal
```
Sol:  
```MatLab
dur = letter.Time(end)
```
```
dur = 0.6080
```

La función ***range*** **devuelve el rango de valores de un arreglo**. Es decir, range(x) es equivalente a max(x) - min(x).

### Tarea 2. Utilice la función range para calcular la relación de aspecto de la letra dividiendo el rango de valores de letter.Y entre el rango de valores de letter.X. Asigne el resultado a una variable llamada aratio.

```MatLab
aratio = range(letter.Y) / range(letter.X)
```
```
aratio = 1.1228
```

El archivo MAT ***featuredata.mat*** contiene una tabla de las características extraídas de 470 letras escritas por diversas personas. La tabla features tiene tres variables: ***AspectRatio*** y ***Duration*** (las dos características calculadas en la sección anterior), y Character (la letra conocida).

### Tarea 3. Utilice la función scatter para representar las características extraídas, con la relación de aspecto en el eje horizontal y la duración en el eje vertical.

```MatLab
load featuredata.mat
features

scatter(features.AspectRatio, features.Duration)
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-12%2022-22-47.png)

![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-12%2022-23-09.png)
