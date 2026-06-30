# Genesis Barbería — Hero + Servicios

Sitio estático (HTML + CSS + JS vanilla). Listo para Vercel.

## Estructura
```
index.html              ← página (nav · hero · servicios · CTA)
vercel.json             ← config de deploy (cache de assets)
assets/images/          ← logo y fotos (REEMPLAZABLES)
data/services.json      ← edita nombres, precios y tiempos aquí
data/site.json          ← WhatsApp, ubicación y estadísticas
```

## Desplegar en Vercel
1. Sube esta carpeta a un repo de Git (o arrástrala en vercel.com/new).
2. Framework Preset: **Other** (sitio estático, sin build).
3. Deploy. No requiere comandos de build.

## Cosas que vas a querer cambiar
- **Precios:** abre `data/services.json` y reemplaza cada `"$—"` por el precio real (ej. `"$180"`).
- **WhatsApp:** `data/site.json` → campo `whatsapp`.
- **Foto del hero:** reemplaza `assets/images/hero-shave.png` (misma ruta) o cambia a video:
  en `index.html`, sustituye la `<img>` dentro de `.hero__media` por
  `<video src="assets/video/tiktok.mp4" autoplay muted loop playsinline poster="assets/images/hero-shave.png"></video>`.

> Los datos se leen de `data/*.json` al cargar; si esos archivos faltan, el sitio
> usa valores por defecto embebidos en `index.html` (nunca se rompe).
