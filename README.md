# RUNTIME MASTER PROMPT v1.0
### Sistema de Governance para Producción de Conocimiento Complejo con LLMs

> *"El problema no es generar contenido con IA. El problema es mantenerlo coherente a escala."*

---

## El Problema

Cuando múltiples instancias de LLM generan contenido sobre un mismo corpus — narrativa, investigación, producto, legal — el sistema se contradice solo. No hay custodio formal. No hay audit log. No hay governance.

El resultado: contenido abundante, corpus corrupto.

---

## La Solución

Un sistema operativo de tres nodos para producción de conocimiento con integridad garantizada:

```
Generador → produce volumen
Curador   → valida contra corpus (única autoridad canónica)
Runtime   → gestiona sesión y enruta al custodio humano
```

**Compatible con modo single-LLM** (Claude asume los tres roles en secuencia) **y modo multi-LLM** (cada nodo recibe su sección).

---

## Qué Incluye

| Archivo | Contenido |
|---|---|
| `RUNTIME_MASTER_PROMPT_v1.md` | Sistema completo: 10 bloques, 47 tests de validación, governance de corpus, protocolo de sesión |
| `ONTOLOGIA.md` | Tipos canónicos: HARD_CANON, SOFT_CANON, PROVISIONAL, DEPRECATED, COUNTERFACTUAL, SIMULATION_BRANCH |
| `AUDIT_LOG_TEMPLATE.md` | Formato append-only para trazabilidad de mutaciones del corpus |
| `EJEMPLO_SESION.md` | Caso de uso completo: inicio → generación → validación → cierre |

---

## Suite de Validación — 47 Tests

Organizados en 5 bloques:

- **A — Integridad Estructural**: consistencia temporal, conocimiento por agente, asimetría de información
- **B — Plausibilidad del Dominio**: institucional, infraestructura, economía interna
- **C — Gestión de Corpus**: mutaciones, versionado, branching
- **D — Tono y Exposición**: registro, densidad, coherencia narrativa
- **E — Autorización**: anti-autovalidación, escalación al custodio

---

## Casos de Uso

| Dominio | Corpus | Valor |
|---|---|---|
| Narrativa / worldbuilding | Canon de universo | Coherencia entre episodios, personajes, timelines |
| Investigación académica | Hipótesis y hallazgos | Trazabilidad de fuentes, no-contradicción retroactiva |
| Diseño de producto | Specs y decisiones | Governance de requerimientos entre iteraciones |
| Legal / compliance | Doctrina y precedentes | Jurisdicción coherente, no-contradicción entre documentos |
| Inteligencia competitiva | Modelo de mercado | Datos primarios protegidos de interpretación sin verificación |

---

## Transferencia a Dominio Nuevo — 7 Pasos

```
PASO 1: Rellenar BLOQUE 0 (definición de dominio)
PASO 2: Definir BLOQUE 5 (reglas inviolables)
PASO 3: Adaptar BLOQUE B (plausibilidad institucional)
PASO 4: Ajustar BLOQUE D (tono del dominio)
PASO 5: Construir snapshot inicial del corpus
PASO 6: Ejecutar caso de prueba
PASO 7: Documentar en /rules/domain_transfer_log.md

NO MODIFICAR: Bloques A, C, E2/E3 (universales)
```

---

## Origen

Extraído por ingeniería inversa del sistema **COMPUTE / El Licenciatario** — serie de ficción y guía operativa sobre la geopolítica del cómputo y los vacíos regulatorios de la IA.

**Autor:** Daniel Gómez Gamiño · [dggamino@gmail.com](mailto:dggamino@gmail.com)  
**Metodología:** Blueprint 2001 — arbitraje institucional verificable desde 2001  
**Credenciales:** Selladas criptográficamente en blockchain Bitcoin · OpenTimestamps · 19 marzo 2026  
**Verificación:** SHA-256 + [opentimestamps.org](https://opentimestamps.org)

---

## Licencia

MIT — Usa, modifica, distribuye. Atribuye al autor.

---

## Contexto Externo

La escasez de cómputo documentada por *The Economist* (2 mayo 2026, "Compute says no") confirma que el governance de producción con LLMs deja de ser opcional. Los cinco grandes hiperescaladores invertirán más de $750B USD este año en infraestructura. El problema no es el acceso al cómputo. Es la coherencia de lo que se produce con él.

Este sistema es una respuesta operativa a ese problema.

---

*RUNTIME MASTER PROMPT v1.0 · México · 2026*
