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
