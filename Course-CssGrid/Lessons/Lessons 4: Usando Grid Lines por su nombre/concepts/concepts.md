# Concepts

Otra manera de crear el grid y posicionar cada elemento es dando nombres a las grid line. De esa manera podemos especificamos donde empieza y el tamaño que tiene.

```
  grid-template-columns:
        [sidebar-start] 1fr
        [contenido-start] 2fr;

  grid-template-rows:
        [header-start] 1fr
        [contenido-start] 2fr
        [footer-start] 1fr;
```

Esto se puede hacer con las filas y las columnas. Después de esto desde cada elemento directamente le especificamos donde empieza y donde termina.

```
  header {
    grid-column: sidebar-start / span 2;
  }

  aside {
    grid-row: contenido-start / span 2;
  }

  footer {
    grid-column: contenido-start;
  }
````
En este caso el header empezara en _sidebar-start_ y ocupara 2 columnas.

En este caso el aside empezara en _contenido-start_ y ocupara 2 filas.

En este caso el footer empezara en _contenido-start_ y como a la hora de nombrar las lineas ya especificamos que ocupara 2fr, en este caso no hace falta volverlo a poner nuevamente.

**span 2** : de esta manera le estamos diciendo los grid cell debe ocupar, en caso de que queramos que **siempre** llegue hasta el final podemos colocar -1. Pero hay que tener en cuenta que si añadimos otra fila o columna, el elemento al que le hayamos colocado esto siempre llegara hasta el final.
