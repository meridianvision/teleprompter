# Teleprompter MV

Un teleprompter que se instala en el teléfono, funciona **sin internet** y no pide cuenta.
Un solo archivo HTML, cero dependencias, cero rastreo.

Hecho en [Meridian Vision](https://meridianvision.cl) para nuestras propias grabaciones.
Lo publicamos porque a cualquiera que grabe a cámara le sirve igual.

**Úsalo ahora:** https://meridianvision.github.io/teleprompter/

---

## Qué resuelve

Grabar leyendo sin que se note. Los teleprompters de las tiendas de aplicaciones
piden registro, cobran suscripción o dejan de funcionar cuando el estudio no tiene
señal. Este vive en el teléfono y arranca en modo avión.

## Para quién

Cualquiera que hable a cámara: periodistas, vocerías corporativas, capacitaciones,
creadores, presentaciones grabadas.

## Instalación

1. Abre el enlace en el teléfono.
2. **Android (Chrome):** menú ⋮ → *Instalar aplicación*.
   **iPhone (Safari):** Compartir → *Añadir a pantalla de inicio*.
   **Computador (Chrome/Edge):** el icono de instalar en la barra de direcciones.
3. Ábrela una vez con internet. Desde ahí funciona offline para siempre.

## Qué hace

- **Pegar** el guion desde WhatsApp, Word o cualquier parte (entra siempre como
  texto plano, así no hereda letra negra sobre fondo negro).
- **Abrir archivo** `.txt` y `.docx`. El lector de `.docx` está escrito a mano con
  `DecompressionStream` — por eso funciona sin internet y sin librerías.
- **Velocidad, tamaño, margen y posición** en vivo con deslizadores.
- **Espejo** para cristal de teleprompter, y **guía** de lectura.
- Tema claro por defecto, con **fondo oscuro** opcional para rodaje.
- Pantalla completa y botones grandes, pensados para tocarlos con el pulgar
  mientras sostienes el teléfono.
- El guion queda guardado en el navegador entre sesiones.

## Qué no hace

- No sube nada a ningún servidor. El guion no sale del dispositivo.
- No mide, no rastrea, no tiene cuentas ni analítica.
- No controla el desplazamiento con la voz ni con un mando externo.
- No graba video: es solo el apuntador. La cámara la pones tú.
- No convierte PDF. Copia y pega el texto.

## Cómo está hecho

`index.html` lleva todo el CSS y el JavaScript dentro. `sw.js` es el service
worker: *network-first* para el HTML, así una versión nueva se propaga en vez de
quedar pegada en la caché, y *cache-first* para los iconos. `manifest.webmanifest`
es lo que permite instalarla.

Para correrlo local:

```bash
python3 -m http.server 8080
# y abre http://localhost:8080
```

## Licencia

MIT. Úsalo, modifícalo, véndelo si quieres. Sin garantía de ningún tipo.

---

<sub>Meridian Vision SpA · Santiago de Chile · parte del
[Taller Abierto](https://github.com/meridianvision): las herramientas que
construimos para trabajar y publicamos gratis.</sub>
