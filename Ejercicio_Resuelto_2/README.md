# Ejercicio resuelto 2: Transformaciones 2D en una galería

**Qué solicita:** aplicar `scale`, `rotate`, `translate` y `skew` con `transform-origin` en una galería de cuadros y un reloj con aguja que gira.

**Cómo se resolvió:** cada caja tiene una transformación distinta en `:hover` con `transition: transform 0.4s ease`. La aguja del reloj usa `transform-origin: bottom center` para girar desde su base, con una curva `cubic-bezier(.4, 2, .6, 1)` que da un pequeño rebote.

**Cómo comprobar:** abrir `index.html`; pasar el cursor sobre cada caja y sobre el reloj. Para ver el efecto de `transform-origin`, quitarlo de `.aguja`: gira desde el centro. También probar `rotate(20deg) scale(1.2) translateX(10px)` y cambiar el orden de las funciones.

**Dependencias:** ninguna.
