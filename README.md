# Uwata 🌿

Web (y futura app) de **turismo comunitario en las comunidades ribereñas de Loreto, Perú**.

El viajero descubre las comunidades en un mapa, solicita su visita por WhatsApp, siembra un árbol durante el viaje y, desde su país, sigue viéndolo crecer con su código QR.

👉 **Web:** https://uwata-peru.github.io

> ⚠️ Las comunidades marcadas como "ejemplo", los precios, los cuidadores y el número de WhatsApp son datos de ejemplo. Las fotos de las comunidades son imágenes referenciales hechas con IA; se reemplazarán por fotos reales.

## Qué tiene

- **Bienvenida animada:** atardecer sobre el río, selva, luciérnagas, aves y un bufeo colorado que salta.
- **Mapa real** (vista clara y satélite) enfocado en Loreto. En la portada se ve en un recuadro; con "Ver mapa completo" se abre para moverlo. Alejado, las comunidades se agrupan; al acercar, se separan con su imagen.
- **Ficha de cada comunidad:** cómo es, por qué ir, distancia desde Iquitos, cómo llegar, experiencias y solicitud de visita por WhatsApp.
- **Leyendas:** una leyenda gratis por comunidad (texto y audio). La colección completa y el libro impreso aparecen como "Próximamente".
- **Mi árbol:** el padrino o madrina entra con el código de su árbol (por ejemplo `UWATA-0001`), ve sus novedades y su código QR, que abre WhatsApp con un mensaje listo.
- **Idiomas:** español, inglés y francés.

## Cómo editar los datos

Casi todo se cambia en **`js/data.js`**:

| Qué cambiar | Dónde |
|---|---|
| Número de WhatsApp | `config.whatsapp` (con código de país, sin `+`). Luego pon `whatsappEsEjemplo: false`. |
| Comunidades | lista `comunidades` |
| Ubicación de una comunidad | `lat` y `lng`. En Google Maps, mantén presionado el lugar y copia los dos números. Si están en `null`, no aparece en el mapa. |
| Zona que se ve al abrir el mapa | Se acomoda sola para que entren todas las comunidades e Iquitos |
| Foto de una comunidad | `foto` (grande) y `fotoMini` (círculo del mapa), en la carpeta `img/fotos/` |
| Ocultar una comunidad sin borrarla | `oculta: true` |
| Leyendas | `leyendas` |
| Árboles sembrados | `arboles` (cada uno con su código) |
| Precios de los planes | `planes` |

Los textos de botones y títulos están en **`js/i18n.js`**.

## Archivos

```
index.html        estructura de la página
css/styles.css    diseño
js/data.js        datos (comunidades, leyendas, árboles, precios)
js/i18n.js        textos en español, inglés y francés
js/app.js         funcionamiento (mapa, vistas, WhatsApp, QR)
img/fotos/        fotos de las comunidades (imágenes referenciales hechas con IA)
img/video/        video de la portada (portada-h.mp4) y su foto mientras carga (portada-h.webp)
vendor/           librerías: Leaflet (mapa), MarkerCluster (agrupar) y qrcode-generator (QR)
```
