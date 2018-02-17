# Concepts

**_Fraction (fr)_**: es una unidad de medida que reparte el espacio disponible entre todos los elementos. 

```
  main{
     grid-template-columns: 1fr 2fr 1fr;
  }
```
> El main en este caso tendria tres columnas, se divide el espacio disponible en 4 partes, y la columna central tendra 2 partes y las otras dos columnas se llevaran una parte.

**_grid-gap_**: propiedad que establece la distancia entre los grid items. 

```
  main{
     grid-gap: 10px;
  }
```

>En este caso tanto las filas como las columnas tienen una separacion de 10px.

```
  main{
    grid-gap: 10px 30px;
  }
```

>En este caso cuando ponemos dos valores, le estamos indicando con el primer valor la separacion de las filas y el segundo valor la separacion de las columnas.

Otra manera de indicar la distancia entre 
filas y columnas seria: 

```
  main{
    grid-column-gap: 30px;
    grid-row-gap: 10px;
  }
```
Esta opcion seria la "descomposicion" de la propiedad grip-gap (metodo acortado). Es una buena practica usar metodos acortados, pero es completamente valido usar esta forma que puede ser mas expresion y visible a lo hora de leer el codigo.

Hay dos tipos de grid:

1. Implicit grid: Es el grid que diseñamos y le damos las medidas que necesitamos.

2. Explicit grid: Es el grid que se genera y no se le ha diseñado ni dado medidas. Una manera de solucionar esto es con la propiedad grid-auto-rows.

```
  main{
    grid-auto-rows: 1fr;
  }
```

De esta manera ya le estariamos dando una medida a ese grid y a todos los elementos que añademos.



