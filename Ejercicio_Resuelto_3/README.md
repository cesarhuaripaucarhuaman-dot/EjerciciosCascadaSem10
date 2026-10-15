# Ejercicio resuelto 3: Tarjeta que voltea (flip card) y animación de entrada

**Qué solicita:** una tarjeta 3D que gira al pasar el cursor con `perspective`, `rotateY` y `backface-visibility`, y que además entre con una animación `@keyframes`, combinando transiciones y animaciones.

**Cómo se resolvió:** `.escena` (padre) lleva `perspective: 900px` y la animación `entrada`; `.tarjeta` (hijo) lleva `transform-style: preserve-3d` y la transición de giro `rotateY(180deg)`. Al estar en elementos distintos, animación y transición no compiten por `transform`. Las caras usan `backface-visibility: hidden` y el reverso parte girado 180°.

**Diferencia con la guía:** no incluí el bloque `@media (prefers-reduced-motion)` que trae el código de la guía, porque en equipos con las animaciones de Windows desactivadas apaga la entrada y el giro y parece que el ejercicio no funciona. Si quieres respetarlo, puedes pegarlo al final de `styles.css`.

**Cómo comprobar:** abrir `index.html` y recargar (Ctrl + F5): la tarjeta sube y aparece. Pasar el cursor: gira 180° y muestra el reverso. Probar quitar `backface-visibility: hidden` o cambiar `rotateY` por `rotateX`.

**Dependencias:** ninguna.
