# Reciclaje de contenido largo

Leé este archivo cuando la marca tenga contenido largo (podcast, YouTube, clases, webinars) y armes la sección **Reciclar** del panel o reciclés un episodio a mano. Está adaptado de las "Custom AI Instructions" (PDF en esta carpeta).

## Cómo se usa en el panel

- **Sección:** Crear → "Reciclar episodio" (`#reciclar`). Campos: título, invitado o invitada, link y transcripción (pegada o subida en .txt, .srt o .vtt; los .srt y .vtt se limpian dejando marcas `[hh:mm:ss]`). Se usan hasta 90.000 caracteres.
- **Formatos:** casillas por formato. Por defecto quedan marcados los canales que la marca usa; el resto queda opcional.
- **Generación:** un `sample` por formato, en secuencia, con `reglasActuales()` + pilares + reglas de reciclaje + instrucción del formato + transcripción. Cada resultado se guarda apenas termina, así que si se corta no se pierde lo hecho.
- **Datos:** colección `reciclajes` {titulo, invitado, link, transcripcion, formatos: {clave: texto}, ideas_enviadas, creado, actualizado}.
- **Pasar ideas al banco:** a partir de clips, Instagram y TikTok elige 6 piezas (2 reels, 3 carruseles, 1 historia) con guion completo y las guarda en `ideas` con `origen: "podcast"`, `episodio` y la serie o pilar. El CM las toma como candidatas del mes.
- **Reglas editables:** `config/reglas.reciclaje` = {clips, instagram, tiktok, youtube, podcast, blog, newsletter, linkedin, threads, pinterest}. Si un formato no está, el panel usa su texto por defecto. Al guardar las reglas desde el panel se conservan los campos que el formulario no muestra (`videos`, `reciclaje`).

## Reglas comunes (van en todos los prompts)

- Todo sale de la transcripción: frases, historias y ejemplos. Nada de ideas genéricas.
- No inventar datos, cifras, estudios ni frases. Atribuir cada cita a quien la dijo y dejarla textual.
- Respetar la voz y la variante de la marca (`config/reglas.base`), salvo en las citas textuales.
- Texto plano, títulos de sección en MAYÚSCULAS.

## Formatos

| Clave | Qué entrega |
|---|---|
| `clips` | De 5 a 8 momentos de menos de 60 s que se entiendan solos: título-gancho, inicio aproximado, duración, cita exacta, texto en pantalla para los 3 primeros segundos (máximo 8 palabras) y por qué funciona. Prioriza ganchos fuertes, historias, consejos concretos y frases citables |
| `instagram` | 20 ideas específicas (5 posts, 5 carruseles, 5 reels, 5 historias) con la frase de origen y el pilar o serie. Las 3 mejores, completas: formato, concepto visual, guion o copy y caption (hashtags según las reglas de la marca) |
| `tiktok` | 20 ideas (10 b-roll + texto en pantalla de 10 a 15 palabras con tipo de b-roll y de audio, y 10 a cámara o voz en off con gancho, mensaje y CTA). Las 3 mejores, completas; caption sin hashtags |
| `youtube` | Al menos 10 palabras clave cortas y long tail en una oración, 5 títulos con formatos variados y una descripción de 3 a 5 oraciones con las palabras clave y 3 hashtags al final |
| `podcast` | En orden: 5 títulos de menos de 70 caracteres, una descripción de menos de 200 palabras con recursos mencionados ("No hay links ni recursos mencionados en este episodio" si no hay) y notas del episodio de 500 a 700 palabras |
| `blog` | 5 títulos SEO, meta descripción de hasta 160 caracteres y artículo de al menos 1.500 palabras con H2 y H3 buscables, sin encabezados vacíos y con viñetas solo si son lo natural |
| `newsletter` | 3 asuntos, 3 textos de vista previa (40 a 140 caracteres) y un cuerpo de 800 a 1.000 palabras: gancho → historia → aprendizaje → un CTA suave. Con marcas para imágenes |
| `linkedin` | 15 posts (5 cortos, 5 medios de 150 a 250 palabras, 5 largos de hasta 500), al menos 2 con historia; sin emojis ni hashtags ni muletillas |
| `threads` | 30 posts (10 citas de menos de 150 caracteres, 10 medios, 10 consejos o reflexiones), sin hashtags y sin resumir el episodio |
| `pinterest` | 10 pines con texto del pin, título de 60 a 100 caracteres y descripción de 100 a 500 caracteres, sin hashtags, emojis ni CTA |

## Adaptación por marca

- Marcá por defecto solo los canales que la marca usa de verdad (para Weholos: clips, Instagram, TikTok, YouTube, Spotify y blog; newsletter, LinkedIn, Threads y Pinterest quedan opcionales).
- Si la marca escribe en primera persona del plural (Weholos: "nosotros, en Weholos"), cambiá "primera persona" por esa voz en blog y newsletter.
- Si la marca usa hashtags en Instagram, el caption lleva los de sus reglas. Si no, ninguno.
- Mencioná el destino real de cada pieza (blog: dominio y categorías; podcast: plataformas).
