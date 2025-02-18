# Crear almacenes de datos.

Puede utilizar comodines a fin de crear un almacén de datos para archivos o carpetas que coincidan con un patrón particular.

```MatLab
ds = datastore("data*.xlsx");
```

Los archivos de datos de escritura a mano tienen nombres con el formato ***user003_B_2.txt***.

### Tarea 1. TAREA
Utilice la función datastore para crear un almacén de datos para todos los archivos que contengan la letra M. Estos archivos tienen _M_ en el nombre y la extensión .txt. Almacene el almacén de datos en una variable llamada letterds.
