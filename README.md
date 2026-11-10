# SAMO CONCEPT

Sitio estático para GitHub Pages: https://samoconcept.github.io

## Incluye
- Landing responsive con portada roja y logo blanco, seguida de la sección Sobre SAMO («Un espacio para explorar el arte en todas sus formas.»), Libros y Objetos en blanco y negro.
- Listados y fichas individuales por URL: `/producto/?id=libro-01`.
- Carrito persistente en `localStorage` con cantidades, eliminación y límites por stock.
- WhatsApp directo desde producto o desde carrito, con texto: “Buenas, me gustaría hacer el siguiente pedido:” y listado de artículos y cantidades.
- Contacto: hellosamoconcept@gmail.com e Instagram @samo.concept.

## Estado del catálogo
Los seis artículos son **fichas demostrativas**, no inventario publicado. No se proporcionaron fotos, precios ni stock confirmado. Antes de lanzar ventas reales:
1. Reemplazar registros de `assets/catalog.js` por productos reales con fotos, descripciones, precios y stock.
2. Cambiar el renderizador `art(p)` para usar imágenes reales cuando estén disponibles.
3. Integrar Supabase: tabla `products` con id, slug, name, category, subtitle, description, price, image_url, stock, status; consumir una vista pública de productos publicados.
4. Validar stock y precio en origen antes de confirmar pedidos. El carrito local no reserva unidades.
5. El pedido por WhatsApp **no procesa pagos** ni confirma automáticamente la compra.

## Identidad visual
- Portada roja `#CC0C0B`; a partir de Sobre SAMO, el sitio usa exclusivamente blanco y negro (incluidos los recuadros del catálogo). Sin amarillo.
- Tipografía principal: Space Mono.
- El logotipo vectorial de `assets/logo.svg`, trazado a partir del documento de marca, se usa también en la esquina superior izquierda: respeta la letra original de Cactus Jack sin depender de un archivo de fuente.
- Cactus Jack es una tipografía indicada por la guía; no está incorporada porque no se adjuntó archivo de fuente ni licencia para publicarla.

## Despliegue
En GitHub > Settings > Pages, elegir **Deploy from a branch**, rama `main`, directorio `/ (root)`. La web es estática, sin npm ni backend.

## WhatsApp
El número `11 5009-1103` se representa internacionalmente como `5491150091103` en `wa.me`, editable en `assets/catalog.js`.

## Pruebas manuales recomendadas
- Abrir Libros y Objetos, entrar a una ficha.
- Agregar varias unidades de un libro y una de un objeto.
- Actualizar la página y confirmar que el carrito persiste.
- Modificar cantidades, eliminar un ítem, revisar que el contador se actualiza.
- Verificar que el enlace WhatsApp de una ficha incluye solo ese artículo.
- Verificar que el enlace del carrito incluye todos los nombres y cantidades.
- Probar navegación y botones en dispositivos móviles.

## Idiomas y favicon
- ES / EN disponible desde el encabezado en todas las páginas; la preferencia se conserva con `localStorage`.
- También se traducen las fichas de demostración y el carrito. El texto predeterminado de WhatsApp permanece en español, según el pedido original.
- Favicon monocromático `assets/favicon.svg` creado con las formas de las letras S y C del logo oficial; cargado en todas las páginas.
- Se actualizó la sección de contacto a «¡Hablemos! :)».

## Prueba visual de libros (noviembre 2026)
Las tres fichas de demostración de Libros usan las portadas aportadas para:
- `The Third Eye: Early Photographs` — George Harrison.
- `David Lynch: His Work, His World` — Tom Huddleston.
- `Kitchen Confidential: Adventures in the Culinary Underbelly` — Anthony Bourdain.

Las tapas están optimizadas en un único sprite AVIF embebido en `assets/book-covers.js` y se identifican mediante `coverIndex` en `assets/catalog.js`. En la futura integración con Supabase se puede agregar `image_url` individual a cada registro; `assets/app.js` ya admite esa propiedad. Ninguna de estas fichas implica stock confirmado ni un precio definitivo.
