# Boston Barber Shop — Sitio web

Sitio web oficial de **Boston Barber Shop** (C. José Arcones Gil 4, 28017 Madrid).

Página única, sin dependencias externas: todo el diseño, las fotos y el vídeo van
incrustados en `index.html`. No hay build, no hay frameworks — lo que ves en el
archivo es lo que se sirve.

## Despliegue

Cada push a `main` publica el sitio automáticamente en GitHub Pages mediante
[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml).

- **URL de producción:** https://david-zequeira.github.io/boston-barbershop-web/
- El despliegue tarda ~1 minuto. Estado: pestaña **Actions** del repositorio.

## Cómo editar los datos del negocio

Todo está en `index.html`. Busca y cambia:

| Dato | Buscar en el archivo |
|------|----------------------|
| Teléfono / WhatsApp | `602 15 71 63` y `34602157163` |
| Dirección | `Arcones Gil` |
| Horario | `10:00 — 21:00` y las franjas de `nextChair()` |
| Servicios | sección `SERVICIOS` (`menu-row`) y los `pill-set` de reservas |
| Reseñas | sección `OPINIONES` (`blockquote`) |
| Logo | `assets/logo.png`, `assets/favicon.png` y los `src` incrustados |
| Redes sociales | sección `PIE` (`Síguenos`) |

> Todos los botones de «Reservar» abren la agenda oficial de Treatwell:
> `https://widget.treatwell.es/establecimiento/boston-barber-shop/`.
> Para cambiarla, busca esa URL en `index.html` y sustitúyela.

## Dominio propio (bostonbarbershop.es)

1. En el repositorio: **Settings → Pages → Custom domain** → `bostonbarbershop.es`.
2. En el DNS del dominio: registro `CNAME` de `www` a `david-zequeira.github.io`
   y registros `A` del apex a las IPs de GitHub Pages
   (`185.199.108.153`, `.109.`, `.110.`, `.111.`).
3. Activar **Enforce HTTPS** cuando el certificado esté listo.

## Enlace de reseñas de Google

El botón «Deja tu reseña en Google» abre la ficha del negocio en Google Maps.
Para reseña directa en un clic, sustituir la URL por el enlace corto de
**Google Business Profile → Solicitar reseñas** (formato `g.page/r/…`).
