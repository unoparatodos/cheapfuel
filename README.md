# CheapFuel

Dónde repostar más barato, con los precios oficiales de todas las gasolineras de España. Y cuánto ahorras cada mes. En línea en https://cheapfuel.netlify.app/

Publicada por [unoparatodos](https://unoparatodos.netlify.app/): gratis, sin anuncios, sin registro y sin rastro.

## Qué hace

- **Mi trayecto**: guardas tu ruta habitual (origen y destino) y ves las gasolineras más baratas en el corredor, con un desvío máximo de 2, 4 u 8 km medido desde la línea recta del trayecto. Es lo que no hace el buscador oficial.
- **Cerca de mí**: las más baratas a 5, 10 o 25 km de donde estás.
- **Por provincia y localidad**: el buscador clásico.
- **Mi ahorro**: desde cualquier gasolinera de la lista pulsas «Repostado aquí», pones litros o euros, y la app guarda el repostaje junto con el **precio de referencia de la zona**: la mediana de las gasolineras a 5 km de esa gasolinera ese día (si hay menos de tres, amplía a 10 y 25 km). El ahorro es (referencia − precio pagado) × litros, sumado por semana, mes y año. Si pagaste más que la mediana, lo muestra en negativo. Se puede exportar e importar en un archivo y compartir como imagen.

Se usa la mediana y no la media para que una gasolinera muy cara (autopista, por ejemplo) no infle el ahorro.

## Datos

- [Geoportal de Gasolineras](https://geoportalgasolineras.es/) del Ministerio para la Transición Ecológica y el Reto Demográfico, a través de su servicio REST público (`sedeaplicaciones.minetur.gob.es/ServiciosRESTCarburantes/`). Cada gasolinera comunica sus precios cuando cambian; el servicio se refresca cada 30 minutos.
- La app pide solo el combustible elegido y guarda los precios en el dispositivo durante 30 minutos con su fecha y hora, que siempre se muestran.
- Todo lo que registra quien la usa (trayecto, repostajes, combustible) se queda en el dispositivo. No hay cuentas ni servidor propio.

## Qué hay aquí

- `index.html`: toda la app en un solo archivo, sin dependencias externas.
- `sw.js`: service worker para que abra al instante y funcione sin conexión (sube la versión de caché `cheapfuel-vNN` en cada cambio).
- `manifest.webmanifest`, iconos y `og.png`.
- `fonts/`: Archivo y Public Sans autoalojadas, con sus licencias OFL.
- `_headers`, `netlify.toml`: cabeceras de seguridad y configuración de Netlify.

## Publicar

Sitio estático: arrastra la carpeta a Netlify (Deploys) o sírvela desde cualquier servidor. Tras cada cambio, sube la versión de caché en `sw.js`.

## Contribuir

Errores, precios que no cuadran con el Geoportal, ideas que pasen los filtros de unoparatodos: abre un *issue*.

## Licencia

Código bajo licencia MIT (ver `LICENSE`). Las tipografías conservan su licencia SIL Open Font License (ver `fonts/`). Los datos pertenecen a su fuente.

Contacto: unoparatodos.app@proton.me
