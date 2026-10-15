# Propuesto 4: Cubo 3D giratorio

**Qué solicita:** un cubo 3D de seis caras (`rotateY`, `rotateX`, `translateZ`) con `transform-style: preserve-3d`, que gire continuamente con `@keyframes`, se detenga (`animation-play-state: paused`) y se amplíe con una transición al pasar el cursor, e incluya `prefers-reduced-motion`.

**Cómo se resolvió:** `.escena` tiene `perspective: 800px`; `.cubo` tiene `preserve-3d` y la animación `girar` (`rotateX(-25deg)` fijo y `rotateY` de 0 a 360°) con `linear infinite`. Las seis caras se orientan con `rotateY`/`rotateX` y se alejan 80 px con `translateZ`. En `:hover` de la escena, el cubo se pausa y `.ampliar` hace `scale(1.35)` con transición. La animación y la transición están en elementos distintos (`.cubo` y `.ampliar`) para no competir por `transform`.

**Importante:** si en tu Windows están desactivadas las animaciones, el cubo se verá quieto por la media query `prefers-reduced-motion` (es el comportamiento esperado). Para verlo girar: Configuración → Accesibilidad → Efectos visuales → activar "Efectos de animación".

**Cómo comprobar:** abrir `index.html`; el cubo gira solo; pasar el cursor para detenerlo y ampliarlo.

**Dependencias:** ninguna.
