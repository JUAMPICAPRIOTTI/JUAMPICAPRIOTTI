# Mi Blog — Instrucciones

Plantilla de blog en HTML puro, lista para subir a GitHub Pages, Netlify o cualquier hosting estático. Cada artículo se puede compartir en Facebook, Twitter/X o WhatsApp **mostrando su foto de portada**.

---

## 📁 Estructura de archivos

```
mi-blog/
├── index.html             ← Página principal con la lista de artículos
├── articulo-ejemplo.html  ← Plantilla para cada artículo
└── img/                   ← Carpeta donde guardás las imágenes
    ├── articulo-1.jpg
    ├── articulo-2.jpg
    └── ...
```

Tenés que crear la carpeta `img/` y meter ahí todas las fotos.

---

## 🚀 Cómo publicarlo gratis en GitHub Pages

1. Creá una cuenta en [github.com](https://github.com) si no tenés.
2. Creá un repositorio nuevo llamado `tu-usuario.github.io` (reemplazando "tu-usuario" por tu nombre de usuario real).
3. Subí los archivos `index.html`, `articulo-ejemplo.html` y la carpeta `img/`.
4. En la pestaña **Settings → Pages**, asegurate de que esté activado (suele estarlo por defecto en este tipo de repositorio).
5. Tu blog estará en `https://tu-usuario.github.io/` en pocos minutos.

**Alternativa en Netlify:** arrastrás la carpeta entera a [app.netlify.com/drop](https://app.netlify.com/drop) y listo, te da una URL al instante.

---

## ✍️ Cómo crear un artículo nuevo

1. **Copiá** el archivo `articulo-ejemplo.html` y renombralo. Por ejemplo: `viaje-a-bariloche.html`.
2. **Abrí el archivo** con cualquier editor de texto (Bloc de notas, VS Code, Sublime).
3. **Cambiá los datos en la zona marcada arriba de todo** (entre los comentarios `<!-- COMPLETAR ESTOS CAMPOS -->`):

   | Campo | Qué poner |
   |---|---|
   | `<title>` | Título del artículo |
   | `og:url` y `twitter:url` | URL completa del artículo (ej: `https://tu-usuario.github.io/viaje-a-bariloche.html`) |
   | `og:title` y `twitter:title` | Mismo título del artículo |
   | `og:description` y `twitter:description` | Descripción corta (100-160 caracteres) |
   | `og:image` y `twitter:image` | **URL completa** de la imagen de portada (ej: `https://tu-usuario.github.io/img/bariloche.jpg`) |
   | `article:published_time` | Fecha de publicación |

4. **Editá el cuerpo del artículo** más abajo: título, bajada, párrafos, imágenes.
5. **Agregá una tarjeta nueva en `index.html`** copiando uno de los bloques `<article class="card">` existentes.

---

## 🖼️ Para que la imagen aparezca al compartir

Esto es **lo más importante** y donde la gente se traba:

1. **La URL de la imagen tiene que ser absoluta**, empezar con `https://`.
   - ✅ `https://tu-usuario.github.io/img/foto.jpg`
   - ❌ `img/foto.jpg`
   - ❌ `/img/foto.jpg`

2. **Tamaño recomendado:** 1200 × 630 píxeles (proporción 1.91:1). Es el ideal para Facebook y Twitter.

3. **Peso:** que pese menos de 5 MB. Idealmente menos de 1 MB para que cargue rápido.

4. **Formato:** JPG o PNG. No uses WebP en og:image porque algunos lectores no lo soportan.

### Probar antes de compartir

Hay validadores oficiales para ver cómo se va a ver tu link en redes:

- **Facebook / WhatsApp:** [developers.facebook.com/tools/debug](https://developers.facebook.com/tools/debug/)
- **Twitter / X:** [cards-dev.twitter.com/validator](https://cards-dev.twitter.com/validator) (si pide login, también funciona simplemente pegando el link en un tweet nuevo sin publicarlo)
- **LinkedIn:** [linkedin.com/post-inspector](https://www.linkedin.com/post-inspector/)

**Truco:** si cambiás una imagen y al compartir sigue saliendo la vieja, es porque Facebook/Twitter cachean. Pasá la URL por el validador de Facebook y hacé clic en "Scrape Again" para forzar la actualización.

---

## 🎨 Personalización rápida

En la sección `<style>` de cada archivo, arriba del todo, hay variables de color:

```css
:root {
  --bg: #f5f1ea;      /* fondo crema */
  --ink: #1a1a1a;     /* texto principal */
  --muted: #6b6258;   /* texto suave */
  --accent: #c0392b;  /* color de marca (rojo terracota) */
}
```

Cambiá esos códigos hexadecimales y se actualiza todo el sitio. Para elegir colores: [coolors.co](https://coolors.co/).

Las tipografías son **Fraunces** (titulares, estilo editorial) e **Inter** (interfaz). Si querés otras, las cambiás en el `<link>` de Google Fonts.

---

## ✅ Checklist antes de publicar un artículo

- [ ] Cambié todos los campos de meta tags arriba (título, descripción, URL, imagen)
- [ ] La URL de `og:image` empieza con `https://` y es accesible (probala pegándola en el navegador)
- [ ] La imagen mide cerca de 1200×630 px
- [ ] Agregué una tarjeta para el artículo en `index.html`
- [ ] Probé el link en [developers.facebook.com/tools/debug](https://developers.facebook.com/tools/debug/)

¡Listo!
