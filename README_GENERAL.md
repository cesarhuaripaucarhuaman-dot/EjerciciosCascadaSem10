# Guía de Práctica, Sesión 10: Transiciones y Transformaciones
Hojas de Estilo en Cascada Avanzado (100000SI58), UTP

## Menú
Abre `index.html` (en la raíz de la carpeta) para ver el menú con todos los ejercicios; cada fila lleva a su carpeta. Los archivos del menú son `index.html` y `styles.css` de la raíz. Para volver al menú desde un ejercicio, usa el botón "Atrás" del navegador (los ejercicios no se modificaron; solo la página del cuestionario tiene un enlace de vuelta).

## Ejercicios encontrados y ubicación

| # | Ejercicio (según el PDF) | Carpeta |
|---|---|---|
| 1 | Ejercicio resuelto 1: Botones y tarjetas con transiciones | `Ejercicio_Resuelto_1/` |
| 2 | Ejercicio resuelto 2: Transformaciones 2D en una galería | `Ejercicio_Resuelto_2/` |
| 3 | Ejercicio resuelto 3: Tarjeta que voltea (flip card) y animación de entrada | `Ejercicio_Resuelto_3/` |
| 4 | Propuesto 1: Menú lateral deslizable | `Ejercicio_Propuesto_1/` |
| 5 | Propuesto 2: Ícono hamburguesa animado | `Ejercicio_Propuesto_2/` |
| 6 | Propuesto 3: Galería de imágenes con zoom | `Ejercicio_Propuesto_3/` |
| 7 | Propuesto 4: Cubo 3D giratorio | `Ejercicio_Propuesto_4/` |
| 8 | Cuestionario (5 preguntas) | `Cuestionario/` |

Cada carpeta de ejercicio contiene `index.html`, `styles.css` y un `README.md` (el cuestionario contiene `index.html`, `styles.css` y `respuestas.md`; el Propuesto 3 incluye además la carpeta `imagenes/`).

## Cómo ejecutar
No se necesita instalar nada: abrir `index.html` de cada carpeta en Chrome, Edge o Firefox (o con la extensión Live Server de VS Code).

## Si no ves animaciones
Solo el Propuesto 4 incluye `prefers-reduced-motion` (lo pide el enunciado). Si tu Windows tiene desactivados los efectos de animación (Configuración → Accesibilidad → Efectos visuales → "Efectos de animación"), ese cubo se verá quieto a propósito.

## Suposiciones
- Los tres ejercicios resueltos reproducen el código de la guía, con comentarios añadidos. En el resuelto 3 omití el bloque `prefers-reduced-motion` que trae la guía (explicado en su README) para que el ejercicio funcione en equipos con animaciones desactivadas.
- Los propuestos son soluciones propias: colores, textos y medidas son libres según el enunciado.
- Propuesto 1: se usó el checkbox con `:checked` (sin JavaScript). Propuesto 2: se eligió el clic, con JavaScript básico.
- Propuesto 3: la guía no entrega imágenes, así que se crearon seis ilustraciones SVG propias en `imagenes/`.
- El PDF de esta sesión solo muestra una imagen de portada (el logo de la UTP); no hay ejercicios ni datos dentro de imágenes.
- Cada ejercicio usa `index.html` + `styles.css` en su propia carpeta, como indica la guía.
