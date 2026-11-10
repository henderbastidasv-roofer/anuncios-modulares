# Modelo de edición · Anuncios Modulares

Instrucciones para Claude Code. Es el modelo con el que se editaron los anuncios de ConstruIA. Úsalo como la línea de edición; adapta los colores, la letra y el link a la marca de quien lo usa.

## 1. Encontrar y cortar las tomas
- Transcribe con **Whisper local** (faster-whisper, modelo `medium` o mejor, idioma español). Nada sale de la computadora.
- Revisa los **canales del audio**. Si la voz está en un solo canal, usa ese canal en mono.
- **Por tramos:** parte el audio en los silencios y transcribe cada tramo por su cuenta. La transcripción de corrido se come las repeticiones.
- Busca cada **código** (H-G01, H-C01, H-CTA1…). Si el código se dijo mal o no se dijo, encuentra la pieza por la frase del guion.
- De cada pieza, quédate con la **última toma completa y sin trabarse**.
- **Corte pegado a la voz:** 0.06 s antes de la primera sílaba y 0.10 s después de la última. Fuera el código, la palmada si la hay y las respiraciones. Las pausas de 0.30 s o más dentro de la frase se quitan.
- **Vuelve a transcribir cada pieza cortada** para confirmar que dice la frase completa.
- Si una toma dice algo de más o promete algo que no se ofrece, **pregúntale al usuario** antes de recortarla.
- Escribe `Lista de tomas.md`: código, segundo de la toma, duración, lo que dice y lo raro que encontraste.

## 2. Armar cada receta
- Pega las piezas de la receta en orden (gancho + cuerpos + cierre).
- **Voz:** highpass a 75 Hz, de-esser, compresión suave 2:1 y −16 LUFS con limitador. Todos los anuncios al mismo volumen.
- **Encuadre:** detecta la cara en cada toma y recorta a **9:16** (1080×1920) y a **4:5** (1080×1350) con la cara centrada. La cara solo sale mientras habla.
- Un poco de color: contraste y saturación suaves, sin exagerar.

## 3. Lo que se ve encima
Estilo: **"lo muestras mientras lo dices"**. Algo nuevo en pantalla cada 1.5 a 3 segundos.
- **Título fijo arriba** con el título de la receta, para quien ve sin sonido.
- **Subtítulos** de 2 o 3 palabras, palabra por palabra, en blanco y sin caja. Una palabra clave resaltada (otro color o una itálica serif).
- **Una tarjeta animada por idea**, que se arma mientras se dice: barras que crecen, una lista que se palomea, un antes y después, el logo real de lo que se nombra (búscalo; nunca dibujes uno parecido).
- **Reencuadres secos** entre piezas y a mitad de una pieza larga (un poco más cerca y luego normal).
- **Tarjeta final** de 1.5 a 2 s con el link y un botón que late.
- Los gráficos se pueden hacer con HTML + GSAP renderizado a video (por ejemplo con HyperFrames) o con ffmpeg. Que no tiemblen: nada de zoompan de ffmpeg.
- **Letra:** la de la marca del usuario. Si no tiene, propón una con carácter y pregúntale antes de usarla.

## 4. Música y sonido
- **Música original o libre de derechos**, nunca una canción comercial. Puede ser generada con IA (por ejemplo ElevenLabs Music, instrumental) o de una biblioteca libre. Deja un `LEEME.txt` con de dónde salió.
- La música va bajita debajo de la voz y el golpe final cae en la tarjeta final.
- Efectos suaves atados a cada animación (whoosh, pop, click).
- Mezcla final a −14 LUFS, con un pico máximo de −1 dBTP.

## 5. Revisar antes de entregar
- **Hoja de cuadros:** el primer y el último cuadro de cada corte, en los dos formatos. Busca:
  - el código o la palmada que se quedó;
  - una cara a medio parpadeo (si pasa, congela los primeros cuadros en uno con los ojos abiertos);
  - un subtítulo de la frase anterior que se quedó encima de la toma nueva.
- Vuelve a escuchar cada anuncio completo.
- Haz **copias livianas** para verlas en el celular (de 4 a 8 MB).
- Entrega en `Anuncios finales/` con nombres claros: `Marca - A1 Nombre - 9x16.mp4`.

## 6. Reglas del mensaje
- No prometer resultados ni inventar números, precios ni testimonios.
- Nada se publica sin el OK del usuario. A Meta se sube **en pausa**.

## 7. Para la próxima grabación
Al terminar, guarda en `LEEME - como se edito.md` los pasos y los scripts que usaste, para repetirlo igual con la grabación nueva cambiando solo las tomas y las recetas.
