# Radar inicial · método y fuentes por nicho

Leé este archivo en la Fase 3b de la skill. Sirve para armar el primer radar de tendencias y cuentas de referencia de una marca, antes de que corra el analista de los sábados.

## Método

1. **Leé primero el radar de la marca**, si existe: `claude/radar-<marca>.md` (o `claude/recursos-*-tendencias.md`). Si tiene menos de 30 días, partí de él y actualizá solo lo que cambió.
2. **Buscá en tandas paralelas** (6 a 10 búsquedas en el mismo turno), en inglés y en el idioma de la marca:
   - reportes de tendencias del nicho del año en curso;
   - tendencias en TikTok e Instagram del nicho (hashtags, formatos);
   - cuentas más seguidas del nicho, a nivel global y en los países de la marca;
   - podcasts y newsletters más escuchados del nicho;
   - medios del idioma de la marca que cubran el tema.
3. **Filtrá con la marca, no con la viralidad:**
   - cada tendencia lleva una línea de por qué encaja (o no) con la marca, su pilar o serie y una fuerza (alta, media o baja);
   - descartá lo que choque con `config/reglas` (promesas, pseudociencia, ofertas que la marca no tiene) y anotalo en "evitar";
   - priorizá lo que responda a los dolores reales del público (comentarios, DMs, análisis de marca).
4. **Cuentas de referencia:** de 8 a 12, mezcla de idioma propio y globales. Solo cargá en el panel los usuarios de Instagram confirmados; los dudosos van al doc con "(verificar)".
5. **Cifras:** citá siempre la fuente y la fecha. Los rankings de terceros (Heepsy, HypeAuditor, listas de medios) son orientativos: decilo. Nunca inventes seguidores, escuchas ni porcentajes.
6. **Guardá en dos lugares:**
   - **Doc de la marca** `claude/radar-<marca>.md`: tendencias con encaje, qué evitar, cuentas (idioma propio y globales), recursos para seguir el radar e ideas listas para el banco. Fuentes como links al final.
   - **Panel**: `set` de `config/radar` con `{semana (lunes AAAA-MM-DD), creado, por, resumen, tendencias: [{titulo, formato, pilar_nombre, fuerza, detalle, fuente}], cuentas: [{usuario sin @, por_que, estado: "propuesta"}]}`. Si ya existe, leelo primero y conservá el `estado` de las cuentas que el dueño ya aprobó o descartó.
7. **Ideas:** las 3 a 5 mejores ideas del radar pueden ir a `ideas` con `origen: "tendencia"` y guion, si el dueño lo pide o si la tarea del analista ya está activa.

## Fuentes por nicho

Sumá un nicho nuevo cada vez que armes un radar para una marca de otro rubro.

### Bienestar, salud mental y crecimiento personal

_Usado para Weholos (08/11/2026). Radar completo: `claude/recursos-bienestar-tendencias.md` en el proyecto de la marca._

- **Reportes:** [Global Wellness Summit · Future of Wellness](https://www.globalwellnesssummit.com/press/global-wellness-summit-releases-10-wellness-trends-for-2026/) (sale cada enero) · [Pew Research · wellness influencers](https://www.pewresearch.org/wp-content/uploads/sites/20/2026/10/pl_2026.10.07_wellness-influencers-report.pdf)
- **Podcasts:** [Podscribe · rankings mensuales](https://podscribe.com/podcast-rankings/july-2026) · [CastFox · self-improvement](https://www.castfox.net/blog/best-self-improvement-podcasts-2026) · ranking Forbes España de podcasts
- **Cuentas:** [Heepsy · wellness por país](https://www.heepsy.com/es/top-instagram/wellness) · [Forbes España · Top 50 divulgadores en salud](https://forbes.es/forbes-women/937129/los-top-50-divulgadores-expertos-en-salud-2026/) · [Psicología y Mente · rankings](https://psicologiaymente.com/directorio/rankings/mejores-cuentas-instagram-psicologia)
- **Newsletters:** [Reletter · Substack salud y bienestar](https://reletter.com/charts/substack/health-and-wellness) · [InboxReads](https://inboxreads.co/best-emotional-wellbeing-newsletters)
- **Cuentas de referencia que funcionaron:**
  - español: Marian Rojas Estapé (@marianrojasestape), Entiende Tu Mente, Patricia Ramírez, Walter Riso, Mario Alonso Puig;
  - globales: The Diary of a CEO (clips de invitados), @melrobbins, @jayshetty, @nedratawwab (carruseles de texto), @drjuliesmith, @the.holistic.psychologist, @headspace, @calm, The School of Life.
- **Tendencias 2026 de base:** regulación del sistema nervioso, slow living y descanso sin culpa, JOMO y desconexión digital, bienestar en comunidad frente a la soledad, trabajo interior, desconfianza en influencers sin respaldo.
- **Evitar en este nicho:** dietas virales, biohacking, detox, aparatos sin regulación y cualquier promesa de salud.

### Automatización e IA para negocios

_Pendiente: completar la próxima vez que se arme un radar para Baires IA Lab._
