# Crear almacenes de datos.

Puede utilizar comodines a fin de crear un almacén de datos para archivos o carpetas que coincidan con un patrón particular.

```MatLab
ds = datastore("data*.xlsx");
```

Los archivos de datos de escritura a mano tienen nombres con el formato ***user003_B_2.txt***.

### Tarea 1. Utilice la función *datastore* para crear un almacén de datos para todos los archivos que contengan la letra M. Estos archivos tienen _M_ en el nombre y la extensión .txt. Almacene el almacén de datos en una variable llamada *letterds*.

```MatLab
letterds = datastore("*_M_*.txt");
```

Utilice la función ***read*** para importar los datos de un archivo del almacén de datos.

```MatLab
data = read(ds);
```

El uso de la función ***read*** la primera vez importará los datos del primer archivo. Al usarla una segunda vez, importará los datos del segundo archivo, y así sucesivamente.

### Tarea 2. Importe los datos del primer archivo a una tabla llamada data.

```MatLab
data = read(letterds)
```
![]()
