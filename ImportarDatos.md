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
