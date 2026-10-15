# Ejercicio resuelto 1: Botones y tarjetas con transiciones

**Qué solicita:** un botón que cambia de color y se eleva al pasar el cursor, y tarjetas que se levantan con sombra, usando `transition` sobre `transform`, `background-color` y `box-shadow`.

**Cómo se resolvió:** la transición se declara en el estado base (`.boton`, `.tarjeta`) para que funcione al entrar y al salir. El botón reacciona a `:hover`, `:focus-visible` (teclado) y `:active` (efecto de presión). Las tarjetas animan `transform` y `box-shadow`.

**Cómo comprobar:** abrir `index.html`. Pasar el cursor sobre el botón y las tarjetas; usar Tab para enfocar el botón; mantener presionado el botón. Para ver por qué la transición va en el estado base, moverla a `.tarjeta:hover`: la salida deja de ser suave.

**Dependencias:** ninguna.
