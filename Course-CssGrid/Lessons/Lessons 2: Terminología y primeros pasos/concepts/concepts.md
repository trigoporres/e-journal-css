## Concepts

> La principal diferencia entre Flexbox y CSS Grid, es que Flexbox es de 1 dimension y CSS Grid es multidimensional. Por lo tanto entre ellos pueden convivir perfectamente.

**_Grid Line_** : son cada una de las lineas que delimitan tanto el grid container como cada fila o columna. Se les puede dar nombre con el fin de poderlas identificar mejor a la hora de crear el grid.

**_Grid Track_** : Nombre que define el espacio vertical u horizonta (fila o columna), entre dos Grid Line consecutivas.

**_Grid Cell_**: espacio entre 4 Grid Line adyacentes. Interseccion entre una fila y una columna.

**_grid-template-column o grid-template-row_** : con estas propiedades podemos definir tanto el numero de filas o columnas como su tamaño.

```
main{
  grid-template-row: 100px 100px 100px;
  grid-template-column: 100px 100px 100px;
}
```

> En este ejemplo tendremos una rejilla de 3 filas y 3 columnas.

**_Grid column_**: propieda con la cual podemos especificar en que columna empieza y en que columna acaba el elemento. Lo mismo se puede usar con **_grid row_**. Si queremos que un elemento llegue siempre hasta la ultima columna o fila debemos poner -1. De esta manera si añadieramos nuevas filas o columnas esta aumentara su tamaño hasta el final.

**_span_** : si añadimos a grid column o row: span 2, le estamos indicando cuantas grid cell ocupara este elemento.

```
header{
  grid-column: 3 / 4;
  grid-row: span 2;
}
```

