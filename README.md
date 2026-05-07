# Stack del desarrollador web moderno · WordPress Sevilla

Presentación construida con [Slidev](https://sli.dev).

## Desarrollo local

```bash
npm install
npm run dev
# → http://localhost:3030
```

## Construir para producción

```bash
npm run build
# → genera la carpeta /dist lista para desplegar
```

## Despliegue en Cloudflare Pages

### Opción A — desde GitHub (recomendada)

1. Sube este proyecto a un repositorio de GitHub
2. Ve a [Cloudflare Pages](https://pages.cloudflare.com)
3. **Create a project** → **Connect to Git** → selecciona el repositorio
4. Configura el build:
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`
   - **Node.js version:** `18` (en Variables de entorno: `NODE_VERSION = 18`)
5. Guarda y despliega

Cloudflare Pages desplegará automáticamente cada vez que hagas `git push`.

### Opción B — despliegue directo con Wrangler

```bash
# Instalar Wrangler
npm install -g wrangler
wrangler login

# Construir y desplegar
npm run build
wrangler pages deploy dist --project-name=stack-ia-wpsvq
```

## Exportar a PDF

```bash
npm run export
# → genera slides-export.pdf
```
