# Propuesto 1: Menú lateral deslizable

**Qué solicita:** un botón "Menú" y una barra lateral oculta con `transform: translateX(-100%)` que se deslice hacia adentro con una transición de 0,4 s al pulsar el botón; los enlaces deben reaccionar al hover con otra transición.

**Cómo se resolvió:** sin JavaScript, con un `input type="checkbox"` y el selector `:checked ~ .sidebar`. El `label` hace de botón. La barra pasa de `translateX(-100%)` a `translateX(0)` con `transition: transform 0.4s ease`. Un fondo oscuro (`opacity`) permite cerrar haciendo clic fuera. Los enlaces cambian de color y se desplazan 8 px con otra transición. `visibility` evita que Tab entre en la barra cuando está oculta.

**Cómo comprobar:** abrir `index.html`, pulsar "Menú", pasar el cursor sobre los enlaces y cerrar con clic fuera o con el mismo botón.

**Dependencias:** ninguna.
