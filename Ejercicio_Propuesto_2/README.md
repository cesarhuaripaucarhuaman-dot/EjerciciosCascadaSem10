# Propuesto 2: Ícono hamburguesa animado

**Qué solicita:** un ícono de tres líneas que, al hacer clic o al pasar el cursor, se transforme en una "X": la línea superior y la inferior rotan (`rotate(±45deg)`) mientras la central desaparece (`opacity: 0`), con `transform-origin` y transiciones.

**Cómo se resolvió:** se eligió el **clic** (el enunciado permite clic o cursor). Un script mínimo alterna la clase `activo`; en ese estado la línea 1 hace `translateY(10px) rotate(45deg)`, la 3 hace `translateY(-10px) rotate(-45deg)` y la 2 pasa a `opacity: 0`. Las líneas usan `transform-origin: center` y `transition: transform 0.35s, opacity 0.25s`. El botón actualiza `aria-expanded` y un texto de estado.

**Cómo comprobar:** abrir `index.html` y hacer clic en el ícono; otro clic lo devuelve a tres líneas. También funciona con Tab y Enter.

**Dependencias:** ninguna (JavaScript básico, sin librerías).
