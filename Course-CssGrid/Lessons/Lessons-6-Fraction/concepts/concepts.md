# Concepts

Fraction (fr) es una unidad de medida que hace referencia a la fraccion del espacio total disponible. 

```
 grid-template-rows: 1fr 2fr 1fr;

 ```

 En este ejemplo se divide el espacio total disponible en 4 fracciones, en la que la primera y tercera fila se llevaran 1fr y la segunda se llevara 2fr.

 Es muy importante que fr se puede combinar perfectamente con cualquier otra unidad de medida.

 ```
 grid-template-rows: 50px 2fr 1fr;

 ```

 En este caso la primera fila medira 50px y fraction cogera el espacio disponible menos 50px, ese espacio se dividira en 3 partes. La segunda fila se llevara 2 partes y la tercera fila se llevara 1 parte.

 **MUY IMPORTANTE**

 Fraction es totalmente flexible al espacio disponible, si el ancho es menor los elementos seran mas pequeños. Siempre se puede añadir un punto de ruptura para que a partir de determinado tamaño tenga otra disposicion. Y esto se hace de manera muy sencilla.

 ```
 @media (max-width: 500px) {
    main {
        grid-template-columns: 1fr 1fr;
        grid-template-rows: repeat(5, 1fr);
    }
}

@media (max-width: 300px) {
    main {
        grid-template-columns: 1fr;
        grid-template-rows: repeat(9, 1fr);
    }
}
```

> repeat(9, 1fr) = 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr

> Para rejillas mas grande es un coñazo tener que repetir n veces 1fr, para eso tenemos la propiedad repeat que nos evitara eso. 