# 🎬 Autoreel — Página web oficial

Sitio de presentación de **Autoreel**, el estudio de video que se maneja solo:
una herramienta personal (single-user) que convierte una idea de una línea en un
video corto terminado — guion, voz, subtítulos, música, motion design, miniatura —
y lo publica en las cuentas propias de su dueño ([@kagonzalezdev](https://www.tiktok.com/@kagonzalezdev))
en YouTube y TikTok.

🌐 **Sitio en vivo:** https://revkelo.github.io/autoreel-web/

## ¿Qué es Autoreel?

Un pipeline de producción de video 100% automatizado para contenido educativo tech
(programación, cloud, DevOps, ciberseguridad):

```
IDEA → guion + project_json → TTS + subtítulos → render → miniatura → publicación → métricas
```

### Capacidades

- **Motor de capas propio** — texto, formas e imágenes animados con keyframes por
  propiedad y curvas de easing; auto-ajuste de texto dentro de cards.
- **TTS neuronal local** — voz generada localmente con cues de tiempo por palabra,
  que sincronizan subtítulos y cambios de escena.
- **Formatos vertical y horizontal** — Shorts/TikTok (15–45s) y formatos largos
  1920×1080 como quizzes de 5 minutos con temporizador segmentado.
- **Plantillas reutilizables** — los videos formulaicos (listas, quizzes) se
  instancian desde código en segundos, sin costo de diseño.
- **Cola + worker desatendidos** — un scheduler reclama videos encolados y los
  produce end-to-end; los fallos son reintentables.
- **Servidor MCP** — todo el estudio expuesto como tools de Model Context Protocol,
  operable conversacionalmente por un agente de IA.
- **Publicación directa** — YouTube Data API v3 (los verticales se vuelven Shorts)
  y TikTok Content Posting API (subida directa de archivo).
- **Métricas** — snapshots periódicos de vistas/likes/comentarios de los videos
  propios para decidir el siguiente contenido.

### Stack tecnológico

| Área | Tecnologías |
|---|---|
| Web & API | Next.js (App Router) · TypeScript · React |
| Motor de render | Canvas 2D · WebCodecs · Chromium headless · edge-tts |
| Datos & jobs | PostgreSQL · worker Node.js · Docker Compose |
| Integraciones | YouTube Data API v3 · TikTok Content Posting API · MCP |
| Calidad | Vitest · Playwright |

Sin APIs de pago en el pipeline: el render y la voz corren en infraestructura propia.

## Este repo

Sitio estático publicado con GitHub Pages. Incluye las páginas legales requeridas
por las integraciones de plataforma:

| Archivo | Página |
|---|---|
| `index.html` | Landing: pipeline, capacidades y stack |
| `terms.html` | [Terms of Service](https://revkelo.github.io/autoreel-web/terms.html) |
| `privacy.html` | [Privacy Policy](https://revkelo.github.io/autoreel-web/privacy.html) |

> Autoreel es un proyecto personal, no comercial y de un solo usuario: publica
> únicamente contenido original en las cuentas de su propietario y no accede a
> datos de terceros.
