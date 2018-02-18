## Concepts

Grid container: "caja" que definimos como contenedor para los grid item.

  ```
    main { display: grid }
  ```

Grid items: cada elemento dentro del Grid container.

Grid-gap: propiedad con la cual definimos una separacion entre grid items. Se le pueden pasar dos valores, en ese caso el primer valor corresponde a las filas y el segundo a las columnas.

  ```
    main { grip-gap: 10px 40px }
  ```

Grip-area: Sirve para definir un nombre para cada sección con el fin de poder nombrarlos y definir el orden en el grip.

  ```
    header { grid-area: header}
  ```

Grid-template-areas: Despues de nombrar cada seccion con esta propiedad podemos definir las columnas y el orden del grid.

  ``` 
        main {
        grid-template-area:
          "header header"
          "aside ."
          "footer footer";
        }
  ```





