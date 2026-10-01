# OSTINIA Vault

Gestor minimalista de notas y enlaces enfocado en la privacidad, la velocidad y la persistencia local. Diseñado con una interfaz monocromática de estética ciberpunk/terminal (`#0a0a0a`, `#d0d0d0`, `#e02020`), efectos CRT y tipografía técnica.

No requiere servidores, cuentas de usuario, telemetría ni conexión a bases de datos remotas.

---

## Características principales

- **Almacenamiento 100% Local:** Todos los datos se gestionan y persisten exclusivamente en el navegador del usuario a través de `localStorage`.
- **Gestión dual de contenido:**
  - **Links:** Validación automática de esquema (`http/https`), extracción de dominios y apertura segura con `rel="noopener"`.
  - **Notas:** Soporte para títulos descriptivos y bloques de contenido multilínea.
- **Portabilidad de datos (JSON):**
  - **Exportar:** Descarga manual de respaldos con marca de tiempo precisa (`ostinia_backup_YYYYMMDD_HHMM.json`).
  - **Importar:** Lectura de backups con validación de esquema, reasignación automática de IDs y control de conflictos (opción de **Fusionar** o **Reemplazar** el contenido existente).
- **Filtrado y Búsqueda en Vivo:** Filtrado por categoría (`Todo`, `Links`, `Notas`) y búsqueda en tiempo real sobre títulos, URLs y notas de texto con debounce.
- **Micro-interacciones y UI Terminal:**
  - Efectos visuales procedurales de scanlines CRT, grano SVG animado y glitch en el logotipo.
  - Interacciones rápidas: confirmación inline para eliminación no destructiva y copia al portapapeles con un clic.
  - Atajos de teclado: <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>Enter</kbd> para guardar; <kbd>Escape</kbd> para cerrar modales.
  - Notificaciones no invasivas mediante sistema de toasts.
  - Adaptabilidad para usuarios con preferencia de movimiento reducido (`prefers-reduced-motion`).

---

## Estructura de Datos (Schema)

Los elementos se almacenan bajo la clave `ostinia_vault_data` con la siguiente estructura JSON:

### Enlace (`link`)
```json
{
  "id": "m1ab2c3def4",
  "type": "link",
  "url": "[https://example.com/recurso](https://example.com/recurso)",
  "title": "Recurso de Investigación",
  "ts": 1785500000000
}
```

### Nota (`note`)
```json
{
  "id": "m1ab2c3xyz9",
  "type": "note",
  "title": "Arquitectura de Agentes",
  "content": "Puntos clave sobre orquestación local y buffers de contexto...",
  "ts": 1785500000000
}
```

---

## Atajos de Teclado

| Atajo | Contexto | Acción |
| :--- | :--- | :--- |
| <kbd>Ctrl</kbd> + <kbd>Enter</kbd> / <kbd>Cmd</kbd> + <kbd>Enter</kbd> | Modal de creación | Guardar entrada activa |
| <kbd>Escape</kbd> | Modales / Cuadros de diálogo | Cancelar y cerrar |

---

## Ejecución y Despliegue

La aplicación es un ejecutable web autocontenido en un único archivo (`index.html`).

### Ejecución Local
Descarga o clona el repositorio y ábrelo en cualquier navegador web moderno:
```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

O sírvelo mediante un servidor HTTP estático básico:
```bash
python3 -m http.server 8080
```

### Despliegue Estático
Compatible directamente con cualquier servicio de hosting de páginas estáticas:
- **GitHub Pages**
- **Cloudflare Pages**
- **Vercel**
- **Netlify**

---

## Stack Tecnológico

- **Lenguaje:** HTML5 semántico / Vanilla JavaScript (ES6+).
- **Estilos:** CSS3 nativo (Variables CSS, Flexbox, CSS Grid, animaciones `@keyframes`).
- **Fuentes:** [Space Mono](https://fonts.google.com/specimen/Space+Mono) & [Inter](https://fonts.google.com/specimen/Inter) vía Google Fonts.
- **Iconografía:** [Font Awesome 6](https://cdnjs.com/libraries/font-awesome).

---

## Licencia

Distribuido bajo la Licencia MIT. Consulta el archivo `LICENSE` para más información.
