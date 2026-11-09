# SAMO CONCEPT

Sitio estático para GitHub Pages: https://samoconcept.github.io

## Incluye
- Landing responsive con franja roja, logo blanco y lema «Curaduría de libros y objetos», más secciones Libros y Objetos.
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
- Fondo unificado rojo `#CC0C0B` en toda la web, con textos y bordes blancos. Amarillo `#FFCA30` exclusivamente para los recuadros de libros y objetos.
- Tipografía principal: Space Mono.
- El logo vectorial en `assets/logo.svg` está trazado a partir del documento de marca proporcionado.
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
