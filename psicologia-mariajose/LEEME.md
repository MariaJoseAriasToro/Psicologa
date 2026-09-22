# Sitio web — Ps. María José Arias Toro

Sitio estático de una sola página, adaptado del sitio de Matilde Pizarro Toro
(fonoaudiología): misma arquitectura, estilos, animaciones, selector de idioma
ES/EN y estructura SEO, **sin el sistema de agenda**. Todos los botones de
"Reservar hora" llevan al perfil de Doctoralia; las consultas, a WhatsApp.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | Todo el sitio (HTML, CSS y JavaScript en un solo archivo) |
| `assets/img/mariajose-foto.jpg` | Tu foto de la sección "Sobre mí" (falta subirla) |
| `robots.txt` | Permite que los buscadores indexen el sitio |
| `sitemap.xml` | Mapa del sitio para Google |
| `llms.txt` | Resumen del sitio para asistentes de IA (ChatGPT, Claude, etc.) |

## Estado: listo para publicar

✅ **Foto**: ya está cargada en `assets/img/mariajose-foto.jpg` (800×800 px,
   recortada y optimizada a partir de la foto que enviaste).
✅ **WhatsApp**: se usó **+56 9 9135 6265**, el número publicado en Doctoralia
   (consulta Alt Potencial), en todos los enlaces (botón flotante, valores,
   contacto) y en el `telephone` del JSON-LD. Si tu WhatsApp real es otro,
   busca `56991356265` en `index.html` y reemplázalo en todas sus apariciones.
✅ **Dominio**: `canonical`, `og:image`, `twitter:image`, `robots.txt` y
   `sitemap.xml` ya apuntan a `psicologamariajoseat.com`. Si el dominio final
   cambia, actualiza esas mismas referencias.

## Pendientes solo de contenido (decisión tuya, no técnicos)

1. **Valores**: los precios vienen de tu perfil de Doctoralia (orientación
   online $18.000, talleres $35.000, técnicas proyectivas $35.000). La sesión
   presencial quedó como "Consultar valor" — confírmame el monto y lo dejo fijo.
2. **Opiniones**: los tres textos de esa sección son un *resumen* de reseñas de
   Doctoralia, no citas textuales. Si quieres publicar palabras exactas de un
   paciente, pídele autorización y reemplaza el texto.

Estos dos puntos siguen marcados en la página con **subrayado punteado
naranja** (clase `fill-me` en el código) para que se noten a simple vista.
Todo lo demás —estructura, SEO, JSON-LD, i18n, enlaces, imagen— está
verificado y funcionando.

## Cómo cambiar textos

Cada texto tiene una "llave" (por ejemplo `hero.title`). Si editas una frase en
el HTML, cámbiala también en el diccionario `I18N_STATIC` del final del archivo
(bloque `<script>`), porque el selector ES/EN reescribe los textos al cargar la
página. Si no vas a usar la versión en inglés, puedes borrar el botón ES/EN del
`<header>` y el diccionario quedará sin efecto.

## Cómo publicar

Igual que el sitio de fonoaudiología: sube `index.html`, la carpeta `assets/`,
`robots.txt`, `sitemap.xml` y `llms.txt` a GitHub Pages, Netlify o al hosting
del dominio. No necesita servidor ni base de datos.
