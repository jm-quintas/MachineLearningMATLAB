# Importar datos

Puede utilizar la función ***readtable*** para **importar datos tabulares** de una hoja de cálculo o un archivo de texto y almacenar el resultado como una tabla.

```MatLab
data = readtable("myfile.xlsx");
```

Esto importa los datos de la hoja de cálculo myfile.xlsx y los almacena en una tabla llamada data.

### Tarea 1. Lea los datos almacenados en el archivo "J.txt" en una variable llamada ***letter***.

```MatLab
letter = readtable("J.txt")
```

![Tabla J.txt](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-09%2022-22-08.png)

Puede utilizar la notación de puntos para hacer referencia a cualquier variable individual dentro de una tabla.

```MatLab
x = mytable.Xdata;
y = mytable.Ydata;
```

Esto ***extrae la variable Xdata de la tabla mytable y almacena el resultado en una nueva variable llamada x***. De manera similar, la variable Ydata se extrae en y.

### Tarea 2. Visualice la letra representando la variable X de letter en el eje horizontal y la variable Y en el eje vertical.

```MatLab
X = letter.X;

Y = letter.Y;

plot(X, Y)
```

![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-09%2022-35-28.png)

Los límites de eje predeterminados distorsionan la relación de aspecto de la letra. Puede usar el comando ***axis*** para forzar los ejes de forma que se conserve la relación de aspecto de los datos.

### Tarea 3. Use el comando axis equal para corregir la relación de aspecto de la representación.

```MatLab
X = letter.X;

Y = letter.Y;

plot(X, Y)
axis equal
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-09%2022-43-40.png)

### Tarea 4. Repita las mismas tareas de importación y representación para los datos del archivo M.txt.

```MatLab
letter = readlatble("M.txt");
plot(letter.X, letter.Y)
axis equal
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-09%2022-55-34.png)

### Tarea 5. Pruebe a ver los datos del archivo V.txt.

```MatLab
letter = readtable("V.txt")
plot(letter.X, letter.Y)
axis equal
```
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-09%2023-00-22.png)
