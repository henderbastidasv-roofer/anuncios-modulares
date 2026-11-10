# Anuncios Modulares · La guía paso a paso

Así hicimos los anuncios de video de ConstruIA con Claude Code: **una grabación de unos 2 minutos y de ahí salieron 3 anuncios en 2 formatos**. Los hicimos con dos guiones, así que en total fueron **12 videos**, subidos a Meta en pausa.

Cada paso trae su **prompt para copiar y pegar** en Claude Code. Lo que va entre [corchetes] lo cambias por lo tuyo. Los mismos prompts están sueltos en la carpeta [`prompts/`](prompts/).

> **El método.** En vez de grabar un video por anuncio, grabas **piezas**: ganchos, cuerpos y cierres. Después Claude Code las mezcla como bloques de Lego, y cada combinación es un anuncio distinto. El método lo aprendí en el curso de Benja Cordero; aquí está cómo lo hago con Claude Code.

```
1 GANCHO (2-4 s) + 2 o 3 CUERPOS (4-8 s c/u) + 1 CIERRE (3-5 s) = un anuncio de 20 a 35 s
3 ganchos × 6 parejas de cuerpos × 2 cierres = 36 anuncios distintos de una sola grabación
```

| Pieza | Para qué sirve | Plano |
|---|---|---|
| **Gancho** | Que la persona se detenga a ver | Primer plano |
| **Cuerpo** | Una sola idea: qué ofreces o por qué tú | Plano medio |
| **Cierre** | Qué hacer ahora: el link | Primer plano |

---

## Paso 0 · Lo que necesitas

- **Claude Code** (plan Pro o Max). En la app de Claude es la pestaña **Code**.
- Una **carpeta nueva** para tus anuncios (por ejemplo, `Anuncios 2026-11`). Abre Claude Code en esa carpeta.
- Tu **celular o una cámara** y un **micrófono** (el de solapa sirve).
- Una **cuenta de anuncios de Meta** con tu página de Facebook y tu Instagram conectados.
- Unos **15 minutos para grabar**. Claude Code se encarga del resto.

Whisper (lo que convierte tu voz en texto) corre gratis en tu computadora. Si no lo tienes, Claude Code lo instala en el paso 4.

---

## Paso 1 · El guion de piezas

Claude Code escribe tus ganchos, cuerpos y cierres, cada uno con un **código**. El código es la clave de todo: después Claude lo busca en el audio para encontrar cada pieza.

**Prompt 1:**
```
Vamos a hacer anuncios de video con el método modular (Lego): 1 gancho + 2 o 3 cuerpos + 1 cierre, todo de una sola grabación mía. Trabaja paso a paso, deja todo guardado en esta carpeta y espera mi aprobación en cada paso.

Mi negocio: [qué hace tu compañía, en qué ciudad, para quién y cuál es tu oferta. Ej.: compañía de remodelación en Dallas; estimado gratis de cocinas y baños].
A dónde mando a la gente: [tu página, tu formulario o tu link].

Reglas del mensaje:

- [De qué sí quieres hablar y de qué no.]
- No prometer resultados ni inventar números, precios ni testimonios.

Hazme el guion de piezas:

- 3 ganchos, 4 cuerpos y 2 cierres, cada uno con su código (H-G01, H-C01, H-CTA1).
- Ganchos de 2 a 4 segundos, cuerpos de 4 a 8 y cierres de 3 a 5.
- Cada cuerpo se tiene que entender solo: nada de "y además" ni "como te dije".
- Nada de "esto" o "aquí": no voy a señalar nada en cámara.
- Al lado de cada pieza, el texto en pantalla o la imagen que sugieres.
- Después, 3 recetas de anuncios con las piezas, cada una con un título corto.
Guárdalo en guion-piezas.md y enséñamelo para aprobarlo.
```

**Antes de aprobarlo, revísalo:**

1. Cada cuerpo se entiende solo.
2. No dice nada que no ofreces.
3. No promete resultados.
4. Suena a como tú hablas. Si una línea no suena a ti, pídele que la cambie.

**¿Quieres otro ángulo?** Nosotros hicimos dos guiones: "La compañía de construcción del futuro" y "IA desde cero". Para el segundo:
```
Hazme un segundo guion de piezas con otro ángulo: [de qué trata]. Usa códigos del 21 en adelante (H-G21, H-C21, H-CTA21) para que no se mezclen con el primero. Guárdalo en guion-piezas-2.md.
```

Mira los guiones reales de ConstruIA en [`ejemplo-construia/`](ejemplo-construia/).

---

## Paso 2 · El teleprompter y el plan de grabación

Se graba **por bloques**, no por anuncio: primero todos los ganchos, luego los cuerpos y luego los cierres.

**Prompt 2:**
```
Aprobado. Ahora dame el plan de grabación por bloques: los ganchos en primer plano, los cuerpos en plano medio, los cierres en primer plano y un bloque final repitiendo los ganchos con otra camisa (con los códigos H-G11, H-G12 y H-G13). Y el texto para el teleprompter: solo las líneas con su código, en el orden en que las voy a grabar. Guárdalo en teleprompter.txt.
```

El bloque con otra camisa es opcional, pero te da el doble de ganchos sin escribir nada nuevo.

---

## Paso 3 · Grabar

**Antes de empezar:**

- Micrófono en **mono** y el medidor en amarillo (entre −12 y −6 dB).
- Graba **10 segundos de prueba** y escúchalos: que se oiga de los dos lados y que no truene.

**Por cada pieza, siempre igual:**

1. Di el **código** en voz alta ("H-G01").
2. Da una **palmada suave**, lejos del micrófono.
3. Espera **2 segundos**.
4. Di la línea **dos veces**.

El código y la palmada son para la máquina: Claude busca el código y la palmada marca dónde empieza. La línea dos veces es para quedarte con la mejor.

**Cuando termines:** pasa el video **original** a la carpeta de tus anuncios, por cable, Drive o USB. **Nunca por WhatsApp**, porque lo comprime.

**Lo que nos pasó a nosotros (y no pasó nada):**

- El micrófono quedó grabando en un solo canal. Claude usó ese canal en mono.
- Dije "H-C01" cuando era "H-C21". Claude encontró la pieza por la frase.
- No grabé los ganchos con otra camisa. Igual salieron los 3 anuncios de cada guion.

| Error | Cómo se evita |
|---|---|
| Audio en estéreo o saturado | Mono, medidor en amarillo y 10 s de prueba |
| Improvisar y saltarse piezas | Seguir el teleprompter, pieza por pieza |
| Hablar justo después de la palmada | Esperar los 2 segundos |
| Señalar cosas ("mira esto") | Decirlo completo; lo visual entra después |
| Pasar el video por WhatsApp | Pasarlo por cable, Drive o USB |

---

## Paso 4 · Encontrar las tomas

Claude Code transcribe tu grabación con **Whisper**, en tu computadora y gratis: convierte la voz en texto con el segundo exacto de cada palabra. Después busca cada código y se queda con la mejor toma.

**Prompt 3:**
```
Ya grabé. El video está en [la ruta del archivo, o "en esta carpeta"].

1. Instala lo que haga falta para transcribir con Whisper en mi computadora (gratis, sin mandar el audio a ningún lado). Revisa en qué canal de audio está mi voz.
2. Parte el audio en los silencios y transcribe cada tramo por separado, para que no se pierdan las repeticiones.
3. Encuentra cada código del guion. Si dije un código mal, búscalo por la frase.
4. De cada pieza, quédate con la última toma completa y sin trabarme.
5. Córtala pegada a la voz: sin la palmada, sin respiraciones y sin pausas largas.
6. Vuelve a transcribir cada pieza cortada para confirmar que dice la frase completa.
Guárdame una "Lista de tomas.md" con el segundo de cada toma, lo que dice y cualquier cosa rara que encuentres.
```

**Por qué por tramos:** si transcribes todo de un jalón, Whisper "se come" las repeticiones y parece que solo dijiste cada línea una vez.

---

## Paso 5 · Armar los anuncios

**Prompt 4:**
```
Arma los 3 anuncios de las recetas del guion-piezas.md, cada uno en 9:16 (Reels y Stories) y en 4:5 (Feed):

- Cortes pegados a la voz: mi cara solo sale mientras hablo.
- Voz limpia y pareja: que todos los anuncios suenen al mismo volumen.
- Subtítulos de 2 o 3 palabras, con la palabra clave resaltada.
- El título fijo de cada receta arriba, para quien lo ve sin sonido.
- Gráficos o texto en pantalla que muestren lo que digo, mientras lo digo.
- Música de fondo [original o libre de derechos], bajita debajo de la voz.
- Una tarjeta final con [mi link].
- Letra: [la tipografía de tu marca].
Guárdalos en una carpeta "Anuncios finales" y dime cuánto dura cada uno.
```

La primera vez, Claude Code arma todo el proceso. **Desde la segunda**, le pasas la grabación nueva y repite los mismos pasos. Pídele al final:
```
Guarda en "LEEME - como se edito.md" todos los pasos y los archivos que usaste, para repetirlo con mi próxima grabación.
```

---

## Paso 6 · Revisar antes de subir

**Prompt 5:**
```
Antes de mandármelos, hazme una hoja de cuadros de cada anuncio: el primer y el último cuadro de cada corte, en los dos formatos. Revisa que no quede la palmada, una cara a medio parpadeo ni un subtítulo de la frase anterior. Después hazme copias livianas para verlas en el celular.
```

**Tú revisas:**

- Míralos en el teléfono, **con y sin sonido**.
- Compara lo que dicen con tu oferta real.
- **Nada se publica sin tu OK.**

A nosotros la hoja de cuadros nos encontró dos cosas: un gancho que empezaba saliendo de un parpadeo y un subtítulo que se quedaba unos cuadros de más.

---

## Paso 7 · Subir a Meta en pausa

**Conecta Meta Ads a Claude Code** (una sola vez). En la Terminal:
```
claude mcp add --transport http meta-ads https://mcp.facebook.com/ads
```
Después, en Claude Code, escribe `/mcp`, escoge *meta-ads* → *Authenticate* e inicia sesión con Facebook. En la pantalla de permisos, **marca todas tus cuentas de anuncios y páginas**: Claude solo ve lo que le autorizas.

**Prompt 6:**
```
Sube los anuncios aprobados a mi cuenta de Meta [nombre de la cuenta], TODO EN PAUSA:

- Una campaña de [tráfico a mi página / clientes potenciales] con un conjunto de anuncios por guion.
- Un anuncio por formato: el 9:16 para Reels y Stories, y el 4:5 para el Feed.
- Escribe el texto y un titular por anuncio, con el botón [Más información] a [mi link]. Enséñamelos antes de subirlos.
- Presupuesto: [cantidad] al día para la campaña.
- No actives nada: yo lo reviso en el Administrador de anuncios y lo activo.
Al final dame una tabla con cada anuncio y dónde quedó.
```

**Ojo:** si tu compañía repara o remodela casas, Meta puede pedir la **categoría especial de Vivienda**. Pregúntale a Claude si aplica a tu oferta.

---

## Paso 8 · Medir y mezclar sin volver a grabar

Deja correr los anuncios unos días y pregunta:

**Prompt 7:**
```
Dime cómo van los anuncios de [nombre de la campaña] en los últimos [7] días: cuánta gente vio los primeros 3 segundos de cada uno (eso mide el gancho), los clics y el costo por clic. No cambies nada: dime qué anuncio va mejor y por qué.
```

**Qué cambias según lo que veas:**

- **Se detienen pero no dan clic:** cambia los cuerpos o el cierre.
- **Nadie se detiene:** prueba otro gancho con los mismos cuerpos.
- **Uno gana:** haz 3 versiones nuevas cambiando solo el gancho.

**Prompt 8:**
```
El anuncio que ganó fue el de las piezas [códigos, ej.: H-G01 + H-C01 + H-C04 + H-CTA1]. Arma 3 versiones nuevas cambiando solo el gancho, con las piezas que ya tengo grabadas.
```

Como ya tienes todas las piezas, no vuelves a grabar.

---

## Tu tarea

1. Copia el prompt 1 y cambia el párrafo de tu negocio.
2. Aprueba tu guion y grábalo con el protocolo.
3. Pídele a Claude Code tus primeros 3 anuncios.
4. Comparte en la comunidad de ConstruIA tu guion y uno de tus anuncios.
5. Si te trabas, pregunta en la comunidad contando qué querías lograr, qué hiciste y dónde te trabaste.

**Grabas una vez y tienes anuncios para todo el mes.**
