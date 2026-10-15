# Cuestionario: Sesión 10, Transiciones y Transformaciones

**1. ¿Qué es una transición CSS y en qué estado (base o :hover) conviene declararla? ¿Por qué?**
Una transición hace que el cambio de una propiedad CSS ocurra de forma gradual durante un intervalo de tiempo, en lugar de instantáneamente; se dispara cuando el elemento cambia de estado (`:hover`, `:focus`, `:active`, una clase). Conviene declararla en el estado **base**, porque así funciona en los dos sentidos: al entrar y al salir del estado. Si solo se declara en `:hover`, la entrada es suave pero la salida es brusca, porque el estado base no tiene transición.

**2. Las cuatro propiedades del atajo `transition` y un valor de cada una.**
- `transition-property`: `transform` (también `background-color`, `all`).
- `transition-duration`: `0.3s` (o `300ms`).
- `transition-timing-function`: `ease-out` (también `linear`, `ease-in-out`, `cubic-bezier()`, `steps(4)`).
- `transition-delay`: `0.2s` (o `0s`).

**3. Diferencia entre `translate()`, `rotate()`, `scale()` y `skew()`. ¿Qué papel cumple `transform-origin`?**
- `translate(x, y)` desplaza el elemento.
- `rotate(ángulo)` lo gira.
- `scale(x, y)` aumenta o reduce su tamaño.
- `skew(x, y)` lo inclina.
Ninguna altera el flujo del documento (los demás elementos no se mueven). `transform-origin` define el punto fijo de la transformación (por defecto `center center`): por ejemplo, con `bottom center` la aguja de un reloj gira desde su base y no desde su centro.

**4. ¿Qué se necesita para que una transformación 3D (ej. `rotateY`) muestre profundidad?**
- `perspective`, en el elemento padre, fija la distancia del observador (menor valor = efecto más dramático, ej. 800px). Sin ella, la rotación se ve plana.
- `transform-style: preserve-3d` mantiene el espacio 3D de los hijos del elemento (por ejemplo, las caras de un cubo o de una tarjeta).
- `backface-visibility: hidden` oculta la cara posterior cuando el elemento está girado, para que no se vea al revés ni se superpongan las caras.

**5. ¿Por qué `transform` y `opacity` en lugar de `width` o `top`? ¿Qué problema ocurre si una animación y una transición modifican `transform` en el mismo elemento y cómo se resuelve?**
`transform` y `opacity` no obligan al navegador a recalcular el diseño de la página y aprovechan la GPU, así que la animación es fluida; `width`, `height`, `margin` o `top` provocan un nuevo cálculo de layout en cada fotograma. Si una animación `@keyframes` y una transición modifican `transform` en el mismo elemento, la animación tiene prioridad y anula la transición. Se resuelve aplicando cada una a un elemento distinto (padre e hijo), como en la flip card: la animación de entrada en `.escena` y la transición del giro en `.tarjeta`.
