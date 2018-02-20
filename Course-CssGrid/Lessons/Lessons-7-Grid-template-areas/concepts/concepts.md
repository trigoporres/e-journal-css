# Concepts

Otra manera de crear el grid es usando grid-template-areas. Para utilizar esta manera primero tendremos que dar nombre a cada area de nuestro grid. 

```
header {
    grid-area: header;
}

aside:first-of-type {
    grid-area: izquierda;
}

article {
    grid-area: contenido;
}

aside:last-of-type {
    grid-area: derecha;
}

footer {
    grid-area: footer;
}
```

Con la propiedad grid-area a cada elemento le damos un nombre, es una buena practica dar un nombre coherente que nos ayude a identificar a que elemento hace referencia.

```
grid-template-areas:
        "header"
        "contenido"
        "izquierda"
        "derecha"
        "footer";
```

De esta manera podemos dar forma y colocar cada elemento dentro de nuestro grid. En el ejemplo que hay arriba el grid estaría formado por 1 columna y 5 filas. Pero tambien podemos diseñar el grid, por ejemplo:

```
grid-template-areas:
        "header header header"
        "izquierda contenido derecha"
        "footer footer .";
```
Aqui hay 3 filas y 3 columnas. El header ocupara las tres columnas, mientras que el footer solo ocupara dos. Cuando colocamos un punto estamos indicando que ese espacio debe ser reconocible pero quedarse vacio.

```
grid-template-areas:
        "izquierda header header"
        "izquierda contenido derecha"
        "izquierda footer derecha";
```

En este ejemplo el elemento izquierda ocupara las 3 filas y en el espacio que antes dejabamos vacio ahora sera ocupado por el elemento derecha

Tambien se le puede dar medidas a esas filas y columnas:

```
grid-template-columns: 1fr 2fr 1fr;
grid-template-rows: 2fr 5fr 1fr;
```

Grid-template-areas para la definicion de areas y su colocacion, y grid-template-columns o grid-template-row son perfectamente compatibles.
