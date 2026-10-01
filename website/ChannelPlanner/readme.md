# ChannelPlanner

> Planificador integral de contenidos y cursos para creadores de YouTube, educadores y productores audiovisuales.

**ChannelPlanner** es una aplicación web *single-page* diseñada para organizar formaciones estructuradas, planificar grabaciones y estructurar la metodología didáctica de cada video. No requiere backend, bases de datos externas ni pasos de compilación: funciona directamente en el navegador con persistencia local.

---

## Características principales

- **Panel de control (Dashboard):**
  - Métricas clave en tiempo real: total de videos, publicados, en progreso y planificados.
  - Cola cronológica de próximos estrenos programados.
  - Barras de progreso de completado por serie/formación.

- **Gestor de Formaciones / Series:**
  - Agrupación modular de videos por bloques temáticos o cursos.
  - Paleta de colores distintiva y subida/compresión automática de portadas en Base64 mediante Canvas API.
  - Reordenación secuencial de episodios (*drag-free* con botones de desplazamiento arriba/abajo).

- **Ficha pedagógica y técnica por Video:**
  - **Metadatos básicos:** Título, serie asociada, estado del flujo de trabajo (`Planificado`, `En producción`, `Editando`, `Publicado`), fecha de publicación programada y enlace a YouTube.
  - **Estructura didáctica:**
    - *Descripción:* Sinopsis temática del episodio.
    - *Conocimientos adquiridos:* Objetivos de aprendizaje clave que dominará la audiencia.
    - *Metodología:* Estrategia de enseñanza, dinámicas o recursos prácticos a emplear.
    - *Notas internas:* Recordatorios de producción, fallos a corregir o marcas de tiempo.
  - **Recursos complementarios:** Gestión dinámica de enlaces externos y documentación de apoyo.
  - **Galería visual adjunta:** Soporte para imágenes de referencia tanto por URL como por subida local (escaladas y comprimidas automáticamente).

- **Calendario editorial:**
  - Vista mensual interactiva con indicadores visuales por estado de producción para cada día del mes.
  - Desglose contextual de entregas al pulsar sobre una fecha concreta.

- **Búsqueda y filtros avanzados:**
  - Búsqueda en tiempo real por palabras clave sobre títulos, descripciones y conceptos clave.
  - Filtrado cruzado simultáneo por formación y estado de producción.

- **Privacidad y portabilidad (Cero dependencias de servidor):**
  - Persistencia total en `localStorage` del cliente.
  - Exportación e importación completa de la base de datos en formato JSON estructurado.
  - Función de borrado seguro con confirmación modal destructiva.

---

## Flujo de Estados del Contenido

```
[ Planificado ] ➔ [ En producción ] ➔ [ Editando ] ➔ [ Publicado ]
    (Ámbar)            (Cian)           (Naranja)       (Esmeralda)
```

---

## Estructura de Datos (Schema)

La información se persiste bajo la clave `cp2` en `localStorage` con la siguiente estructura:

```json
{
  "settings": {
    "channelName": "Nombre del Canal",
    "channelDescription": "Línea editorial del canal"
  },
  "series": [
    {
      "id": "uuid-v4",
      "name": "Nombre de la Formación",
      "description": "Descripción del curso o bloque temático",
      "color": "#00e68a",
      "thumbnail": "data:image/jpeg;base64,...",
      "createdAt": 1740000000000
    }
  ],
  "videos": [
    {
      "id": "uuid-v4",
      "seriesId": "uuid-serie-o-null",
      "order": 0,
      "title": "Título del video",
      "description": "Resumen del contenido",
      "conocimientos": "Conceptos y destrezas adquiridas",
      "metodologia": "Estrategia pedagógica aplicada",
      "notes": "Notas internas de grabación y montaje",
      "status": "planificado",
      "scheduledDate": "2026-10-15",
      "youtubeLink": "[https://youtube.com/](https://youtube.com/)...",
      "links": [
        { "id": "uuid", "title": "Documentación", "url": "https://..." }
      ],
      "images": [
        { "id": "uuid", "type": "base64", "data": "data:image/jpeg...", "description": "Esquema" }
      ],
      "createdAt": 1740000000000
    }
  ]
}
```

---

## Puesta en marcha

Al tratarse de una solución autocontenida (*vanilla stack* en un único fichero HTML), no requiere entorno Node ni gestor de paquetes.

### 1. Clonar el repositorio
```bash
git clone [https://github.com/tu-usuario/channel-planner.git](https://github.com/tu-usuario/channel-planner.git)
cd channel-planner
```

### 2. Abrir en local
Haz doble clic sobre el archivo `index.html` o lánzalo desde terminal:

```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

Si prefieres usar un servidor local ligero:
```bash
# Con Python
python3 -m http.server 8080

# Con Node / npx
npx serve .
```

### 3. Despliegue en producción
Puedes hospedar el proyecto de forma estática y gratuita en:
- **GitHub Pages** (directamente desde la rama `main`, raíz `/`)
- **Cloudflare Pages**
- **Vercel** o **Netlify**

---

## Tecnologías utilizadas

- **Core:** HTML5 semántico, JavaScript Vanilla (ES6+ modular sin transpilación).
- **Estilos y Maquetación:** [Tailwind CSS CDN](https://tailwindcss.com/) + CSS Grid / Flexbox nativo con variables CSS (*design tokens* en modo oscuro).
- **Tipografía:** [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) (titulares) y [DM Sans](https://fonts.google.com/specimen/DM+Sans) (cuerpo y datos) vía Google Fonts.
- **Iconografía:** [Font Awesome 6](https://cdnjs.com/libraries/font-awesome).
- **Motor Gráfico:** HTML5 Canvas 2D nativo para compresión y escalado reactivo de imágenes en cliente.

---

## Licencia

Distribuido bajo la Licencia **MIT**. Consulta el archivo `LICENSE` para más detalles.
