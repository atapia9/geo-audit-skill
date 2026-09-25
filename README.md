# GEO Audit Skill

**🇲🇽 Español** · [🇺🇸 English](#english)

Skill de Claude para realizar auditorías **GEO (Generative Engine Optimization)**: evalúa qué tan bien está posicionada una organización, marca o persona para ser encontrada, entendida y citada por asistentes de IA como ChatGPT, Claude, Gemini y Perplexity.

## ¿Qué es GEO?

Si el SEO optimiza para aparecer en los resultados de Google, el GEO busca que los sistemas de IA generativa:

- encuentren información sobre tu organización cuando les preguntan por tu tema;
- te citen como fuente confiable;
- te reconozcan en grafos de conocimiento (Wikipedia, Wikidata, Crunchbase, etc.);
- te recomienden en sus respuestas.

## Qué hace este skill

Ejecuta una auditoría en **6 fases**, cada una con puntaje de 0 a 100:

| # | Fase | Qué evalúa |
|---|---|---|
| 1 | Descubribilidad | Rastreo, indexación, arquitectura del sitio y organización del contenido |
| 2 | Autoridad | Señales EEAT: experiencia, pericia, autoridad y confianza |
| 3 | Citabilidad | Calidad y verificabilidad del contenido, Schema.org, estructura apta para citar |
| 4 | Comprensión semántica | Claridad de la entidad, relaciones y posibles confusiones |
| 5 | Grafos de conocimiento | Presencia en Wikipedia/Wikidata, Google/Bing KG, Crunchbase, LinkedIn, OpenAlex |
| 6 | Estrategia | Hallazgos principales, victorias rápidas y hoja de ruta |

Con esos puntajes calcula un **GEO Score** global (promedio ponderado; los pesos se ajustan por industria).

## Niveles de profundidad

| Nivel | Duración estimada | Resultado |
|---|---|---|
| `quick` | ~1 hora | 4 fases núcleo, 5 hallazgos, 10 victorias rápidas, hoja de ruta a 30 días |
| `standard` | 2–3 horas | 6 fases, benchmark con 3–4 competidores, 20–25 victorias rápidas, hoja de ruta a 6 meses |
| `deep` | 4+ horas | Análisis ampliado, 5+ competidores, auditoría de Schema.org, hoja de ruta a 12 meses, módulos por industria |

## Entregables

- Informe en Markdown con resumen ejecutivo, análisis por fase, hallazgos, matriz competitiva y evaluación de riesgos.
- Tablero interactivo en HTML con el GEO Score y los puntajes por fase.
- En auditorías `deep`: archivos de apoyo (hoja competitiva, auditoría de contenido, lista de verificación de Schema.org).

## Instalación

El skill es el archivo [`SKILL.md`](SKILL.md) (nombre: `geo-audit`).

- **Claude Code:** copia `SKILL.md` a una carpeta `geo-audit/` dentro de tu directorio de skills (por ejemplo, `~/.claude/skills/geo-audit/SKILL.md`).
- **Claude.ai / app de escritorio:** empaqueta la carpeta del skill y súbela desde la configuración de skills.

## Uso

Dile a Claude, por ejemplo:

- "Haz una auditoría GEO estándar de [organización]"
- "¿Está mi startup bien posicionada para el descubrimiento por IA?"
- "Compara nuestra visibilidad en IA contra [competidores]"

Datos que solicita: nombre de la organización, sitio web, industria, mercado geográfico y 2–3 competidores. Opcionales: nivel de profundidad, áreas de enfoque y formato de salida.

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `SKILL.md` | Definición del skill: proceso, criterios, entregables |
| `evals/evals.json` | Casos de prueba para evaluar el skill |
| `trigger_evals.json` | Frases de prueba para verificar cuándo debe activarse |
| `LICENSE` | Licencia MIT |

## Alcance y límites

La auditoría se apoya en investigación web y en inferencia; los puntajes son estimaciones fundamentadas en evidencia pública, no mediciones oficiales de ningún asistente de IA. Conviene revisar los hallazgos antes de tomar decisiones.

## Autoría y licencia

Creado por **Jesús Armando Tapia Gallegos** ([@atapia9](https://github.com/atapia9)), junio de 2026. Licencia [MIT](LICENSE).

---

<a id="english"></a>

# GEO Audit Skill (English)

A Claude skill that runs **GEO (Generative Engine Optimization)** audits: it assesses how well an organization, brand or person is positioned to be found, understood and cited by AI assistants such as ChatGPT, Claude, Gemini and Perplexity.

## What is GEO?

Where SEO optimizes for Google rankings, GEO aims to make generative AI systems:

- find information about your organization when asked about your domain;
- cite you as a credible source;
- recognize you in knowledge graphs (Wikipedia, Wikidata, Crunchbase, etc.);
- recommend you in their answers.

## What this skill does

It runs a **6-phase audit**, each phase scored 0–100:

| # | Phase | What it evaluates |
|---|---|---|
| 1 | Discoverability | Crawlability, indexation, site architecture, content organization |
| 2 | Authority | EEAT signals: experience, expertise, authoritativeness, trustworthiness |
| 3 | Citability | Content quality and verifiability, Schema.org, citation-friendly structure |
| 4 | Semantic understanding | Entity clarity, relationships, potential confusions |
| 5 | Knowledge graphs | Presence in Wikipedia/Wikidata, Google/Bing KG, Crunchbase, LinkedIn, OpenAlex |
| 6 | Strategy | Top findings, quick wins and roadmap |

From these it computes an overall **GEO Score** (weighted average; weights adjust by industry).

## Depth levels

| Level | Estimated time | Result |
|---|---|---|
| `quick` | ~1 hour | 4 core phases, 5 findings, 10 quick wins, 30-day roadmap |
| `standard` | 2–3 hours | 6 phases, benchmark vs. 3–4 competitors, 20–25 quick wins, 6-month roadmap |
| `deep` | 4+ hours | Expanded analysis, 5+ competitors, Schema.org audit, 12-month roadmap, industry modules |

## Deliverables

- Markdown report with executive summary, per-phase analysis, findings, competitive matrix and risk assessment.
- Interactive HTML dashboard with the GEO Score and phase scores.
- For `deep` audits: supporting files (competitor spreadsheet, content audit, Schema.org checklist).

## Installation

The skill is the [`SKILL.md`](SKILL.md) file (name: `geo-audit`).

- **Claude Code:** copy `SKILL.md` into a `geo-audit/` folder inside your skills directory (e.g. `~/.claude/skills/geo-audit/SKILL.md`).
- **Claude.ai / desktop app:** package the skill folder and upload it from the skills settings.

## Usage

Tell Claude, for example:

- "Run a standard GEO audit for [organization]"
- "Is my startup well positioned for AI discovery?"
- "Benchmark our AI visibility against [competitors]"

Inputs it asks for: organization name, website, industry, geographic market and 2–3 competitors. Optional: depth level, focus areas and output format.

## Repository contents

| File | Description |
|---|---|
| `SKILL.md` | Skill definition: process, criteria, deliverables |
| `evals/evals.json` | Test cases to evaluate the skill |
| `trigger_evals.json` | Test phrases to check when the skill should trigger |
| `LICENSE` | MIT license |

## Scope and limits

The audit relies on web research and inference; scores are evidence-based estimates from public information, not official measurements from any AI assistant. Review the findings before making decisions.

## Author and license

Created by **Jesús Armando Tapia Gallegos** ([@atapia9](https://github.com/atapia9)), June 2026. [MIT](LICENSE) license.

<sub>Este material fue elaborado con asistencia de Claude (Anthropic) y revisado por Armando Tapia, con colaboración de Claude Code. / This material was prepared with assistance from Claude (Anthropic) and reviewed by Armando Tapia, in collaboration with Claude Code.</sub>
