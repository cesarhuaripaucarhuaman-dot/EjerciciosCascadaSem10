# Propuesto 3: Galería de imágenes con zoom

**Qué solicita:** una galería de al menos seis imágenes con CSS Grid; cada imagen hace zoom suave (`scale(1.1)`) dentro de su contenedor (`overflow: hidden`) y muestra un texto con `opacity` y `translateY` al pasar el cursor; las imágenes entran escalonadamente con `@keyframes` y `animation-delay`.

**Cómo se resolvió:** seis `figure` en una grilla `repeat(auto-fit, minmax(280px, 1fr))`. Cada `figure` (con `overflow: hidden`) tiene la animación `entrada` con retardos de 0.1 s a 0.85 s. La `img` interior hace `scale(1.1)` con transición, y el `figcaption` pasa de `opacity: 0; translateY(20px)` a visible. Animación y transición están en elementos distintos para no competir por `transform`. Funciona también con foco de teclado (`tabindex="0"` y `:focus-visible`).

**Imágenes:** como no se proporcionaron fotos, se crearon seis ilustraciones SVG propias en `imagenes/`. Puedes reemplazarlas por tus fotos manteniendo los nombres o cambiando el `src`.

**Cómo comprobar:** abrir `index.html` (mantener la carpeta `imagenes/` al lado) y recargar con Ctrl + F5 para ver la entrada escalonada.

**Dependencias:** ninguna.
