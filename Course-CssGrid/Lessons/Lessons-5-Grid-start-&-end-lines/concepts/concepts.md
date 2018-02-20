# Concepts

Igual que se pueden nombrar el inicio de las lineas, se puede nombrar el final. De esa manera a la hora de especificar en cada elemento su posicion y tamaño quedara mucho mas expresivo.

```
  grid-template-columns:
        [sidebar-start] 1fr
        [sidebar-end contenido-start] 2fr
        [contenido-end];

    grid-template-rows:
        [header-start] 1fr
        [header-end contenido-start] 2fr
        [footer-start] 1fr
        [footer-end];
```
En cada elemento podemos dejar de usar span 2, -1... Ya solo necesitaremos especificar la linea final.

```
  header {
    grid-column: sidebar-start / contenido-end;
  }

  aside {
    grid-row: header-end / footer-end;
  }

  footer {
    grid-column: contenido-start / contenido-end;
  }
```
Es buena practica al usar este metodo colocar los prefijos start o end con el fin de evitar confusiones y ser mas expresivos.