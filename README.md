# MM Sublimados — Página web (Astro)

Sitio de una sola página para tu negocio de sublimación (tazas, cuadernos y llaveros personalizados). Estética artesanal tipo *scrapbook* con los colores de tu logo (rojo vino + celeste).

## 🟢 Lo único que necesitas tocar: `src/data/site.json`

Ahí cambias **todo el contenido** sin tocar código:

- **marca** → nombre, lema, frase y logo.
- **contacto** → número de WhatsApp (formato internacional sin `+` ni espacios, ej. `51999999999`), correo, teléfono visible y horario.
- **redes** → enlaces de Instagram, TikTok y Facebook.
- **categorias** → las 3 familias (tazas / cuadernos / llaveros) y su descripción.
- **productos** → cada tarjeta de la tienda (título, etiqueta, descripción e imagen).
- **galeria** → fotos del "mural".
- **proceso** → los pasos de cómo se pide.
- **publicaciones** → tus novedades / posts.
- **testimonios** → reseñas de clientes.

### Cómo cambiar una foto
1. Copia tu imagen dentro de `public/productos/`.
2. En el JSON escribe la ruta así: `"/productos/nombre-de-tu-foto.jpg"`.

El logo va en `public/logo.png`.

## ▶️ Cómo verla en tu computadora

Necesitas tener **Node.js 18+** instalado. Luego, en la carpeta del proyecto:

```bash
npm install      # solo la primera vez
npm run dev      # abre http://localhost:4321
```

## 🚀 Cómo publicarla en internet (gratis)

```bash
npm run build    # genera la carpeta /dist
```

Sube la carpeta `dist/` a cualquiera de estos servicios (arrastrar y soltar):

- **Netlify** → netlify.com/drop
- **Vercel** → vercel.com
- **Cloudflare Pages**

En Netlify/Vercel también puedes conectar el proyecto completo y elegir:
- Build command: `npm run build`
- Publish directory: `dist`

Cuando tengas tu dominio, cámbialo en `astro.config.mjs` (campo `site`).

## 📁 Estructura

```
mm-sublimados/
├── public/
│   ├── logo.png
│   └── productos/        ← aquí van todas las fotos
├── src/
│   ├── data/site.json    ← AQUÍ editas el contenido
│   ├── styles/global.css ← colores y tipografías
│   └── pages/index.astro ← la página (no hace falta tocarla)
├── astro.config.mjs
└── package.json
```
