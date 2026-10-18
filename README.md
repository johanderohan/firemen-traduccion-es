# The Firemen (SNES) — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/super-nintendo/the-firemen)**.

Traducción al **español de España** de *The Firemen* (Super Nintendo, 1994),
el juego de acción de Human Entertainment en el que Pete y Danny entran en el
edificio en llamas de la química Metrotech en plena Nochebuena. Se ha traducido
**directamente del japonés**, a partir de la ROM japonesa original.

La traducción se reparte como **parche**: no incluye el juego. Necesitas tu propia
copia para aplicarlo.

## Estado

Última versión: **[v1.1 — Pantallas finales en castellano](../../releases/tag/v1.1)**.

| Parte | Estado |
|---|---|
| Mensajes de radio (toda la historia, incluido el final) | **279 de 279** traducidos y revisados |
| Subtítulos de la introducción | **23 de 23** |
| Menú CONFIG, aviso de mando mal conectado y pantallas finales | Redibujados en castellano con el estilo original |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « » …** |
| Logotipo y textos en inglés del original | Se conservan (ver abajo) |
| Revisión durante una partida | Comienzo jugado y los 279 mensajes vistos en el juego (ver abajo) |

Se mantienen a propósito el logotipo (con «ファイヤーメン»), el texto en inglés
que se desplaza sobre el edificio en la introducción —en el original japonés ya
estaba en inglés, como decorado, con subtítulos japoneses debajo; ahora esos
subtítulos están en castellano— y los rótulos en inglés del juego: START, CONFIG,
PAUSE, TIME, LIFE, CONTINUE, NORMAL, STEREO, EXIT y los letreros del edificio.

### Cambios técnicos

- La ROM se **amplía a 2 MB** (16 Mbit, LoROM). Funciona en emuladores y
  flashcarts que admiten ROMs de ese tamaño.
- El juego dibuja la radio en casillas fijas de 16 píxeles (doce por renglón,
  pensadas para kanji). Cada mensaje en castellano se compone con una **fuente
  de ancho variable** nueva, con el mismo trazo blanco y contorno oscuro que la
  original, y se guarda ya troceado en esas casillas: el efecto de máquina de
  escribir, los retratos y la animación de la boca funcionan como en el original.
- Los mensajes terminan antes de los iconos del marcador, que en el original
  tapaban el final de los renglones, y su tiempo en pantalla se ha alargado
  para leer el castellano con calma. Como en el original, **SELECT** acelera o
  salta un mensaje.
- Los subtítulos de la introducción usan una variante de la fuente para el modo
  de alta resolución del juego.

### Comprobaciones y trabajo pendiente

- Una auditoría automática vuelve a leer la ROM construida y comprueba cada
  mensaje, subtítulo, parche de código y gráfico, además del *checksum* interno.
- Se ha probado en emulador (snes9x) **desde arranque en frío**: introducción
  completa con sus subtítulos, título, menú CONFIG con todas sus opciones, el
  aviso de mando mal conectado y el comienzo de la partida jugado normalmente
  (primer piso, con sus primeros mensajes, muerte y continuación). Fuera del
  cuadro de radio, el juego es idéntico al original en las capturas comparadas.
- Los **279 mensajes de radio** se han mostrado en el juego uno a uno,
  forzándolos desde la memoria, y se han revisado en capturas (texto, cortes de
  renglón, retratos, tiempos de lectura).
- **Pendiente:** una partida completa jugada de principio a fin, la prueba en
  consola física y una revisión humana independiente. La traducción y su
  revisión se han hecho con asistencia de IA. Por eso la versión figura «en
  revisión»; si encuentras algo, abre una incidencia.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego en versión **japonesa**. El parche solo funciona
   con esa versión exacta, sin cabecera de copiadora:

   | | |
   |---|---|
   | Archivo | `Firemen, The (Japan).sfc` |
   | Tamaño | 1.048.576 bytes (1 MB) |
   | MD5 | `79c9ffe304fa775ce3ec15270058f41b` |
   | CRC32 | `15F2271D` |

   ```bash
   md5sum "Firemen, The (Japan).sfc"                        # Linux
   md5 "Firemen, The (Japan).sfc"                           # macOS
   CertUtil -hashfile "Firemen, The (Japan).sfc" MD5        # Windows
   ```

   Si tu archivo mide 1.049.088 bytes tiene una cabecera de 512 bytes: quítala
   antes de parchear. Si el MD5 no coincide, el parche fallará. La versión
   europea en inglés no sirve.
3. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "Firemen, The (Japan).sfc" firemen-snes-es-v1.1.xdelta "The Firemen (ES).sfc"`
4. Comprueba que la ROM resultante mide **2.097.152 bytes** (2 MB) y tiene MD5
   **`3498b1ed99625cf34002f6dddbbf2c84`**.
5. Juega en tu emulador o flashcart (el juego no guarda partidas).

## Cambios por versión

### v1.1 — 18 de octubre de 2026

- Las pantallas que salen al acabar el juego, ahora en castellano: «AHORA PRUEBA EL MODO
  NORMAL/EXPERTO», el texto en japonés que explica el código del modo experto y el rango
  final («LUCHADOR LEGENDARIO»). Gracias a Medina por avisar.

### v1.0 — 17 de octubre de 2026

- Primera publicación: toda la historia (los 279 mensajes de radio y la
  introducción) en castellano de España, traducida del japonés.
- Menú CONFIG y aviso de mando traducidos, fuente española con el estilo
  original y ROM ampliada a 2 MB.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin
relación alguna con Human Entertainment ni con los actuales titulares de
*The Firemen*. Aquí no se distribuye el juego ni ninguna parte de él: solo un
parche que modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia
y lo hago.
