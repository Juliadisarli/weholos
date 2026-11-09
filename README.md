---
title: Weholos · Contexto de marca y Centro de Marketing
description: Qué hay en este repositorio, cómo funciona el Centro de Marketing paso a paso y de dónde saca los datos cada sección del panel.
tags:
  - weholos
  - centro-de-marketing
  - readme
---
# Weholos · Contexto de marca y Centro de Marketing

Este repositorio guarda el contexto de marca de Weholos y el **Centro de Marketing**: un panel privado donde se planifica, crea y mide el contenido de Instagram, con Claude haciendo el trabajo pesado y las socias aprobando.

- **Panel:** https://claude.ai/artifact/EfqazcMETNY7SyaHwCi2bd (privado; se comparte desde el menú Compartir del panel).
- **Estado al 09/11/2026:** panel publicado, base cargada, métricas de Meta Ads conectadas. Las tareas programadas todavía no están creadas (ver [Qué falta](#qué-falta)).

## Qué hay en el repositorio

| Carpeta o archivo | Qué contiene |
|---|---|
| `01 Podcast Tu Mejor Version Contexto/` | Portadas y piezas del podcast *Tu Mejor Versión*. Los videos .mp4 no se suben (pesan más de lo que GitHub acepta) |
| `02 Reels Capsulas/` | Portadas de reels cápsula (Ikigai, ¿Quieres o no quieres?) |
| `03 Weholos Carrusel/` | Carrusel "Los cuatro acuerdos": referencia del estilo visual |
| `04 Webblog In progress/` | Links del blog weholos.com |
| `05 Reel Dosis In progress/`, `06 Descargable Camino del Bienestar/` | Proyectos en preparación (vacías) |
| `07 Manual de marca weholos/` | Manual de marca en PDF |
| `Links Sitio Web y Redes Sociales weholos.txt` | Web, Instagram, Linktree, Spotify, YouTube y TikTok |
| `claude/` | Todo lo que generó Claude para Weholos (ver abajo) |
| `centro-marketing-marca/` | La skill que arma un Centro de Marketing para cualquier marca |
| [centro-marketing-blueprint.md](./centro-marketing-blueprint.md) | Blueprint original del sistema (hecho para Baires IA Lab) |

**Carpeta `claude/`:**

| Archivo | Para qué sirve |
|---|---|
| [analisis-weholos.md](./claude/analisis-weholos.md) | Análisis de marca: posicionamiento, público, series, voz, formatos de video y calendario base |
| [centro-marketing-weholos.md](./claude/centro-marketing-weholos.md) | Resumen técnico del sistema: URL, base de datos, conectores |
| [recursos-bienestar-tendencias.md](./claude/recursos-bienestar-tendencias.md) | Radar de tendencias y cuentas de referencia de bienestar |
| `centro-marketing-weholos.html` | El código del panel. Se publica con la herramienta Artifact de Claude |
| `reglas-weholos.json` | Copia de las reglas de marca que viven en la base del panel |

## Cómo funciona, paso a paso

### Una sola vez (armado, ya hecho)

1. **Contexto.** Claude leyó estas carpetas, `E:\WEHOLOS` (estrategia, ecosistema y manual de marca), la web y el Linktree, y pidió lo que faltaba: objetivo (crecer audiencia, sin venta por ahora), voz (tuteo neutro), países y mails.
2. **Análisis de marca.** Propósito "crear momentos de bienestar", pilares Amor, Salud y Dinero, y cinco series editoriales. Queda en [analisis-weholos.md](./claude/analisis-weholos.md).
3. **Panel.** Se adaptó la plantilla del Centro de Marketing con los colores, la tipografía (Poppins) y el logo del manual, y se publicó como artifact con base de datos propia.
4. **Base inicial.** Se cargaron las series como pilares, las reglas de marca, la meta semanal, el radar de tendencias, las reglas de reciclaje y los datos de Meta Ads.

### Cada mes (con tareas programadas, cuando se activen)

1. **Durante el mes entran ideas:** reels virales guardados, tendencias del sábado, episodios reciclados e ideas propias.
2. **Día 20:** el CM arma el mes siguiente: 4 reels, 8 carruseles, sus diseños y 12 secuencias de historias.
3. **Día 21:** llega un mail a julidisarli@gmail.com y j.obejeropaz@gmail.com con lo que hay que aprobar y lo que hay que grabar a mano.
4. **Las socias aprueban** en "Para aprobar" y las piezas pasan al calendario.
5. **Cada semana:** se cargan las métricas, se actualizan los anuncios de Meta y el radar de tendencias.

### Cada vez que sale un episodio del podcast

1. Pegar o subir la transcripción en **Reciclar episodio**.
2. Claude genera clips, ideas para Instagram y TikTok, textos para YouTube y Spotify y un artículo para el blog.
3. Con **Pasar ideas al banco**, las mejores piezas quedan con guion y el CM las usa al armar el mes.

## Secciones del panel y de dónde salen los datos

| Sección | Qué hace | De dónde salen los datos | Quién los carga |
|---|---|---|---|
| **Inicio** | Resumen: KPIs, flujo de contenido, próximos, tendencias y banco | Todo lo de abajo | Se calcula solo |
| **Para aprobar** | Propuesta mensual del CM: aprobar, descartar, cambiar o pasar a video a cámara | `meses/<AAAA-MM>` (lugares del mes) e `historias` | El CM (día 20 o botón "Completar con el CM") |
| **Contenido Mes** | Brief del mes y los 12 lugares | `meses/<AAAA-MM>` | Las socias (brief) y el CM (lugares) |
| **Calendario** | Mes, agenda, meta semanal y "Para producir" | `posts` y `config/meta` | Se crean al aprobar; también a mano |
| **Carruseles** | Diseñador 1080 × 1350 con descarga de PNG o ZIP | `disenos` | El CM, el generador del panel o a mano |
| **Historias** | Secuencias 1080 × 1920 con stickers de guía | `historias` | El CM o el generador del panel |
| **Reels virales** | Cola de reels de referencia con análisis y guion nuevo | `reels` | Se suman links a mano; Claude los procesa (necesita el navegador con sesión de Instagram) |
| **Reciclar episodio** | De una transcripción del podcast salen 10 formatos e ideas para el banco | `reciclajes` e `ideas` (origen `podcast`); reglas en `config/reglas.reciclaje` | Las socias pegan la transcripción; Claude genera desde el panel |
| **Ideas** | Banco de ideas con guion, puntaje y serie | `ideas` y `pilares` | Todas las fuentes de arriba más ideas propias |
| **Tendencias** | Radar semanal, cuentas de referencia (aprobar o descartar) e ideas | `config/radar` e `ideas` (origen `tendencia`) | Claude: radar inicial del 08/11/2026; después, el analista de los sábados |
| **Métricas · Publicidad en Meta** | Inversión, seguidores de Instagram atribuidos, impresiones, clics e interacciones por período; gráfico mensual; ranking de anuncios | `config/ads` (totales, `mensual`, `anuncios`) | Claude con el conector oficial de Meta Ads, solo lectura. Última carga: 09/11/2026 |
| **Métricas · Orgánico** | Semanas de Instagram (vistas, alcance, seguidores, interacciones) y resultados por publicación | `metrics/<lunes>` y `posts.res` | A mano o por CSV. La carga automática necesita el conector local de Meta (pendiente) |
| **Campañas** | Anuncios propios con "Ver en Meta", referencias de la Biblioteca de anuncios y propuestas | `config/ads`, `config/ads_refs` y `campanas` | Claude (solo lectura en Meta); las campañas las carga a mano quien administra la cuenta |

**Reglas que usan todas las generaciones:** `config/reglas` (voz, público, oferta, carruseles, historias, videos y reciclaje) y la colección `pilares`. Se editan desde Ideas → reglas, o pidiéndoselo a Claude.

### Cómo se filtran los anuncios de Weholos

La cuenta publicitaria `260302546` (en pesos) es compartida con Baires IA lab y L&J Contenidos. Solo se cuentan los anuncios cuyo creativo pertenece a la página Weholos (`307950359058266`). En la carga del 09/11/2026 eso dio 60 de 65 anuncios, desde abril de 2024.

## Conectores

| Conector | Para qué | Estado |
|---|---|---|
| Meta Ads (oficial, claude.ai) | Anuncios, métricas pagas y Biblioteca de anuncios | Conectado, uso solo lectura |
| Gmail (j.obejeropaz@gmail.com) | Mail mensual | Conectado |
| Conector local de Meta (en la compu) | Métricas orgánicas de Instagram y transcripción de reels | Falta instalar |
| Navegador de la app de Claude con sesión de Instagram | Leer reels guardados y cuentas de referencia | Falta iniciar sesión |

Los tokens y claves nunca van en el chat ni en este repo: solo en la configuración local de Claude.

## Cómo actualizar cosas a mano

Escribirle a Claude en el chat, por ejemplo:

- "Actualizá las métricas de Meta Ads del centro de marketing"
- "Actualizá el radar de tendencias de Weholos"
- "Procesá la cola de reels del centro de marketing"
- "Completá el mes de diciembre con el CM"

Para cambiar el panel: se edita `claude/centro-marketing-weholos.html` y Claude lo vuelve a publicar en el mismo link. Los datos viven en la base del panel, así que republicar no los borra.

## Qué falta

1. **Tareas programadas:** CM mensual (día 20), mail mensual (día 21), alerta de constancia (jueves), analista de tendencias (sábados), experto en campañas y métricas de Meta Ads (miércoles), reels virales y métricas orgánicas. Horario previsto: 10 h, UTC−3, lunes a sábado.
2. **Conector local de Meta y sesión de Instagram** para las tareas que necesitan la compu.
3. **Primera prueba real** de Reciclar episodio con la transcripción de *#1 Inteligencia Emocional*.

## La skill

`centro-marketing-marca/` es la versión genérica: arma este mismo sistema para cualquier marca a partir de su carpeta de contexto. Incluye el método del radar inicial (`references/radar-inicial.md`) y el de reciclaje de contenido largo (`references/reciclaje-contenido.md`). Está instalada también en `C:\Users\PC\.claude\skills\` para usarla como `/centro-marketing-marca`; si se cambia acá, hay que volver a copiarla allá.
