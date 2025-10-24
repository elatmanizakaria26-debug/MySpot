# MySpot — Landing estática (Vercel + GitHub)

Landing lista para publicar en Vercel, con lista de espera (temporalmente desactivada) y botón de contacto de cofundador por email.

## Estructura

/
├─ index.html  
├─ public/  
│  ├─ logo.svg  
│  └─ favicon.svg  
├─ robots.txt  
├─ sitemap.xml  
└─ vercel.json  (solo si es SPA; ver notas)

## Deploy

1. Sube todo este contenido a tu repositorio (raíz).  
2. Conecta el repo en **Vercel** → **Deploy**.  
3. En **Settings → Build & Output Settings**:
   - **Framework Preset:** `Other`  
   - **Build Command:** *(vacío)*  
   - **Output Directory:** *(vacío)* ← importante porque `index.html` está en la raíz.  
4. Verifica primero la URL de preview: `https://<tu-proyecto>.vercel.app`  
5. Asigna el dominio en **Settings → Domains**:
   - `globalmyspot.com`
   - `www.globalmyspot.com`
   - Deben quedar **Assigned** y **Valid**.

## Notas SPA (si usas rutas del lado del cliente)

Si tu app es una SPA y necesitas que todas las rutas sirvan `index.html`, añade un archivo `vercel.json` en la raíz con este contenido:

```json
{
  "cleanUrls": true,
  "trailingSlash": false,
  "rewrites": [{ "source": "/(.*)", "destination": "/" }]
}
