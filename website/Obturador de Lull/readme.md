# Obturador Lull — Rueda Fotográfica Combinatoria

Motor generativo visual y conceptual inspirado en la combinatoria del *Ars Magna* de Ramon Llull y adaptado a la dirección fotográfica, narrativa visual y generación de prompts de alta fidelidad.

El sistema implementa 9 anillos concéntricos desacoplados con 20 variables ortogonales por anillo ($20^9 \approx 5.12 \times 10^{11}$ combinaciones únicas posibles).

---

## Características

- **Arquitectura combinatoria estricta (9 anillos):**
  1. **Lugares:** Escenarios y espacialidad.
  2. **Épocas:** Contexto temporal, movimientos de diseño y cine.
  3. **Poses:** Lenguaje corporal y gestualidad.
  4. **Punto de Vista (POV):** Ángulo, altura y encuadre.
  5. **Luz:** Esquema lumínico y calidad de la fuente.
  6. **Técnica:** Modificadores ópticos, tiempos y procesos de captura.
  7. **Hora:** Temporalidad, calidad espectral y posición del sol.
  8. **Estación:** Factores meteorológicos y estacionales.
  9. **Atmósfera:** Textura perceptual, tono narrativo y peso visual.
- **Motor gráfico Canvas 2D:** Renderizado procedural en tiempo real ajustado dinámicamente al Device Pixel Ratio (DPR) de la pantalla.
- **Micro-interacciones y UI táctil:**
  - Animación con curva de desaceleración quíntica (*ease-out*) escalonada por anillo.
  - Efecto de obturador, retroiluminación y flash sincronizado.
  - Perspectiva 3D interactiva en el dial según la posición del cursor.
  - HUD cinemático con parámetros variables de cámara (ISO, apertura, obturación, distancia focal).
- **Audio procedural:** Síntesis sonora del clic mecánico del obturador mediante Web Audio API (sin dependencias de archivos de audio externos).
- **Zero Build:** Implementación autocontenida en un único archivo HTML con soporte offline total.

---

## Controles e Interacción

| Disparador | Acción |
| :--- | :--- |
| `Espacio` / **Botón Central** | Disparo simultáneo de los 9 anillos (rotación escalonada con flash). |
| `1` a `9` | Giro individual del anillo correspondiente. |
| **Palancas laterales (Desktop)** | Selección/rotación individual por categoría e inspección visual al hacer *hover*. |
| **Dial táctil (Móvil)** | Selector optimizado con cuadrícula compacta. |

---

## Instalación y Despliegue

Al no requerir compilación ni empaquetadores (*bundlers*), puedes ejecutarlo directamente:

### 1. Clonar el repositorio
```bash
git clone [https://github.com/tu-usuario/obturador-lull.git](https://github.com/tu-usuario/obturador-lull.git)
cd obturador-lull
