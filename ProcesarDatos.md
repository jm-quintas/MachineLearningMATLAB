# Procesar Datos.

Puede ***usar la notación de puntos para extraer, modificar y reasignar variables en una tabla***, como lo haría con cualquier variable. 

```MatLab
x = x + 3;
data.XVal = data.XVal + 3;
```

### Tarea 1.  Multiplique los valores de la variable X de la tabla letter por la relación de aspecto 1,5. Reasigne el resultado de nuevo a X para que letter contenga los datos corregidos.

```MatLab
letter = readtable("M.txt")

% Solución de la tarea:
letter.X = 1.5*letter.X;

plot(letter.X,letter.Y)
axis equal
```
Sol:  
![](https://github.com/jm-quintas/MachineLearningMATLAB/blob/main/img/Captura%20desde%202025-02-12%2013-21-47.png)

Puede ***indexar en las variables de una tabla***, al igual que con cualquier variable. En programación, ***indexar*** **se refiere a la acción de asignar un índice numérico a cada elemento de una estructura de datos, como una matriz o una lista**. Este índice permite acceder a cada elemento de manera individual y eficiente.

