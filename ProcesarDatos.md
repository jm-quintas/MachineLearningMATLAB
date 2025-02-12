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

