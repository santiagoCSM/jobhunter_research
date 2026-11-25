# JobHunter Research

**English** · [Español ↓](#jobhunter-research-español)

> Research status: **planning / not yet experimentally validated**. This repository documents research, not a deployed autonomous application.

An open, reproducible engineering research project investigating whether **an old Android smartphone can function as an autonomous, resource-efficient, AI-assisted job-search agent** in the Mexican employment market.

The initial test device is an **LG X230H with Android 6 (API 23)** and approximately 1 GB RAM. The application itself is developed separately in [JobHunter MX](https://github.com/santiagoCSM/JobHunter-MX.). This repository is intended to publish research and experimental evidence through [Priors](https://github.com/santiagoCSM/priors).

## Research question

> Can a low-resource, unsupported Android phone autonomously discover relevant jobs from permitted sources, match them to a real candidate profile and produce accurate, tailored résumés—while achieving measurable improvements in time saved and job-search quality without compromising privacy or violating platform rules?

The answer is **not presumed to be yes**. Negative findings, limitations, and failed approaches must be documented.

## Research areas and hypotheses

| ID | Area | Testable question | Status |
| --- | --- | --- | --- |
| 001 | Legacy Android | Can Android 6 complete periodic ingestion and notifications with acceptable reliability, RAM, storage and battery use? | Planned |
| 002 | Job matching | Do structured filtering and semantic ranking improve relevant-job precision over keyword-only search? | Planned |
| 003 | Adaptive résumé | Does truthful job-specific résumé tailoring improve response rates compared with a consistent baseline CV? | Planned |
| 004 | Resource efficiency | Which architecture minimizes memory, energy, bandwidth and runtime on the LG X230H? | Planned |
| 005 | Workflow automation | How much manual effort can the system save without false submissions, incorrect answers or unauthorized automation? | Planned |

Hypotheses will be formally pre-registered with metrics, baselines, sample-size considerations, failure criteria and reproducible protocols **before running confirmatory experiments**.

## Research principles

1. **Measure, do not assume.** Distinguish measured findings from prototypes, assumptions and anecdotal observations.
2. **Establish a baseline.** Compare against a manual workflow or simpler alternative, not only against zero automation.
3. **Avoid leakage and confounding.** Evaluate job ranking on held-out opportunities; control job type, time, seniority and posting age when testing CV effects.
4. **Prioritize real-world constraints.** Assess Android 6 background execution, TLS compatibility, network interruptions, memory pressure and security risks.
5. **Preserve factual accuracy.** CV personalization may select and rephrase verified experience but must never invent employment, education, dates or skills.
6. **Respect consent and site restrictions.** Prefer official alerts, user-supplied links and permitted interfaces. No CAPTCHA bypass, unauthorized data harvesting or prohibited application bots.
7. **Protect personal data.** Use synthetic/anonymized fixtures in published experiments; never commit real CVs, applicant credentials, API keys or identifiable recruiter correspondence.
8. **Report negative results.** A rejected hypothesis is still an important research result.

## Candidate evaluation metrics

- **Autonomy:** successful scheduled runs, missed-run rate, recovery after reboot and connectivity loss.
- **Performance:** peak RAM, storage footprint, data usage, job processing time and battery consumption.
- **Relevance:** precision@k, recall on a labeled sample, ranking agreement and duplicate rate.
- **Résumé quality:** factual consistency, job requirement coverage, readability, ATS parseability and human review findings.
- **Outcome:** qualified applications reviewed, time saved, recruiter reply rates, interviews; confidence intervals and sample-size limitations.
- **Safety:** unauthorized actions (target: zero), false application-status claims, accidental duplicate applications and sensitive-data exposure.

A match score is a heuristic; it is **not** an estimated hiring probability. A personalized CV must not be described as superior until evidence supports that conclusion.

## Methodology and deliverables

Every study should include:

1. A falsifiable hypothesis and declared success/failure thresholds.
2. A benchmark and reproducible experimental protocol.
3. Data provenance, collection permissions and privacy handling.
4. Measured results, uncertainty and relevant negative cases.
5. Threats to validity and a decision: continue, revise, reject or collect more data.

Study status and decisions are tracked in [board.md](board.md), using a layout compatible with Priors.

### Proposed repository layout

```text
jobhunter_research/
├── README.md                 # Bilingual research overview
├── board.md                  # Research decision board (Priors source)
├── docs/                     # Study design, protocols and findings
├── research/                 # Individual studies and experiments
├── datasets/                 # Public/synthetic sample metadata only
├── scripts/                  # Reproducible analyses and benchmarks
└── results/                  # Aggregated, privacy-preserving reports
```

*The directories above are a proposal, not a claim that they are already implemented.*

## Initial research plan

- [ ] Define device baseline: firmware, RAM, storage, battery condition, network and TLS capabilities.
- [ ] Draft and preregister experiment 001: autonomous scheduling reliability on Android 6.
- [ ] Build a consented or synthetic set of Mexican software-job postings for matching evaluation.
- [ ] Specify a verified master-profile schema and factuality checks for tailored CVs.
- [ ] Define a fair CV comparison design before any outcome-based claims.
- [ ] Document reproducible findings and update [board.md](board.md).
- [ ] Publish this project through the Priors index after there is an initial study page and a valid research board.

## Connected projects

- **[JobHunter MX](https://github.com/santiagoCSM/JobHunter-MX.)** — Android application and implementation.
- **[Priors](https://github.com/santiagoCSM/priors)** — public index of independently maintained research projects.
- **[BTC Candles Research](https://github.com/santiagoCSM/btc_candles_research)** — methodological inspiration: explicit hypotheses, documented stages and a research decision board.

---

# JobHunter Research (Español)

[English ↑](#jobhunter-research)

> Estado: **planificación / sin validación experimental todavía**. Este repositorio documenta investigación, no una aplicación autónoma ya desplegada.

Proyecto abierto y reproducible de investigación de ingeniería para estudiar si **un teléfono Android antiguo puede operar como agente autónomo y eficiente de búsqueda de empleo asistida por IA** en el mercado mexicano.

El dispositivo inicial es un **LG X230H con Android 6 (API 23)** y aproximadamente 1 GB de RAM. La aplicación se desarrolla por separado en [JobHunter MX](https://github.com/santiagoCSM/JobHunter-MX.). Este repositorio busca publicar metodología, experimentos y resultados mediante [Priors](https://github.com/santiagoCSM/priors).

## Pregunta central

> ¿Puede un teléfono Android de recursos limitados descubrir ofertas relevantes de fuentes permitidas, compararlas con el perfil real de una persona y generar CV adaptados y veraces, con mejoras medibles en tiempo y calidad de búsqueda, sin poner en riesgo la privacidad ni incumplir las reglas de las plataformas?

No asumimos una respuesta afirmativa. Los resultados negativos y los intentos fallidos también se documentarán.

## Líneas de investigación

| ID | Área | Pregunta comprobable | Estado |
| --- | --- | --- | --- |
| 001 | Android antiguo | ¿Puede Android 6 ejecutar consultas y notificaciones periódicas con fiabilidad y consumo aceptables? | Planeada |
| 002 | Compatibilidad laboral | ¿Los filtros estructurados y el ranking semántico identifican mejor las vacantes relevantes que una búsqueda por palabras clave? | Planeada |
| 003 | CV adaptativo | ¿Un CV personalizado con información real aumenta las respuestas frente a un CV base constante? | Planeada |
| 004 | Eficiencia | ¿Qué arquitectura minimiza RAM, batería, datos y tiempos de ejecución en el LG X230H? | Planeada |
| 005 | Automatización | ¿Cuánto trabajo manual reduce el sistema sin solicitudes falsas ni acciones prohibidas? | Planeada |

Antes de cada experimento confirmatorio se definirán hipótesis falsables, métricas, grupos de comparación, tamaño de muestra cuando corresponda y criterios de abandono.

## Principios metodológicos

1. **Medir antes de afirmar.** Separar datos observados, prototipos, suposiciones y anécdotas.
2. **Comparar con un referente.** Usar el proceso manual o una alternativa sencilla como línea base.
3. **Controlar sesgos.** Usar ofertas reservadas para evaluación y controlar puesto, antigüedad, seniority y fecha de publicación en las pruebas del CV.
4. **Evaluar limitaciones reales.** Examinar segundo plano, HTTPS, cortes de red, uso de memoria y riesgos de Android 6.
5. **Mantener la veracidad.** Adaptar el CV significa reorganizar y describir mejor experiencia verificable; jamás inventar empleos, estudios, fechas o tecnologías.
6. **Respetar permisos y plataformas.** Priorizar alertas oficiales, enlaces del usuario y métodos autorizados. No evadir CAPTCHA, extraer datos sin permiso ni automatizar solicitudes prohibidas.
7. **Cuidar datos personales.** Publicar casos sintéticos o anonimizados; nunca subir CV reales, contraseñas, claves de API ni correspondencia identificable.
8. **Publicar hallazgos negativos.** Una hipótesis rechazada también aporta conocimiento.

## Métricas sugeridas

- **Autonomía:** ejecuciones exitosas, omisiones, recuperación tras reinicio o desconexión.
- **Rendimiento:** RAM máxima, almacenamiento, transferencia de datos, duración y batería.
- **Relevancia:** precision@k, recall en muestra etiquetada, acuerdos del ranking y duplicados.
- **Calidad del CV:** fidelidad factual, cobertura de requisitos, legibilidad, lectura ATS y revisión humana.
- **Resultados:** postulaciones cualificadas revisadas, tiempo ahorrado, respuestas y entrevistas, con incertidumbre y limitaciones muestrales.
- **Seguridad:** acciones no autorizadas (objetivo: cero), estados de envío incorrectos, duplicados involuntarios y filtraciones de datos.

Un puntaje de compatibilidad **no es** una probabilidad de contratación. No daremos por hecho que un CV adaptado funciona mejor sin resultados suficientes.

## Protocolo de investigación

Cada estudio debe incluir hipótesis falsable y umbrales, benchmark, protocolo reproducible, procedencia y permisos de datos, resultados e incertidumbre, limitaciones y decisión final: continuar, modificar, rechazar o reunir más información.

Las decisiones se registrarán en [board.md](board.md), siguiendo el formato de Priors.

### Estructura prevista

```text
jobhunter_research/
├── README.md                 # Presentación bilingüe
├── board.md                  # Tablero de decisiones para Priors
├── docs/                     # Diseños y protocolos
├── research/                 # Experimentos independientes
├── datasets/                 # Metadatos de muestras públicas/sintéticas
├── scripts/                  # Análisis reproducibles
└── results/                  # Informes agregados sin datos sensibles
```

*Por ahora es una propuesta de organización, no un listado de carpetas ya implementadas.*

## Próximas etapas

- [ ] Registrar características reales del LG: firmware, RAM, almacenamiento, batería, red y HTTPS.
- [ ] Diseñar y prerregistrar el experimento 001 sobre ejecución autónoma en Android 6.
- [ ] Construir un conjunto permitido o sintético de vacantes mexicanas para evaluar compatibilidad.
- [ ] Definir un perfil maestro verificable y comprobaciones contra información inventada.
- [ ] Diseñar una comparación justa entre CV base y CV adaptado.
- [ ] Publicar resultados reproducibles y mantener actualizado [board.md](board.md).
- [ ] Agregar el proyecto al índice de Priors cuando exista la primera publicación de investigación.

## Proyectos relacionados

- **[JobHunter MX](https://github.com/santiagoCSM/JobHunter-MX.)** — aplicación Android y código funcional.
- **[Priors](https://github.com/santiagoCSM/priors)** — índice público de investigaciones independientes.
- **[BTC Candles Research](https://github.com/santiagoCSM/btc_candles_research)** — referencia metodológica: hipótesis explícitas, fases documentadas y tablero de decisiones.
