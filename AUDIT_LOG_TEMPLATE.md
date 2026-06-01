# AUDIT LOG TEMPLATE
## Sistema RUNTIME MASTER PROMPT v1.0

> **Regla fundamental: este log es append-only. No se edita. No se borra.**

---

## Formato de Entrada

```
AUDIT_ENTRY {
  session_id:      string (ej. "SESSION_20260531_001")
  timestamp:       ISO8601 (ej. "2026-05-31T15:30:00-06:00")
  corpus_version:  string (ej. "1.0.0")
  nodo:            "Generador" | "Curador" | "Custodio"
  tipo_mutacion:   "NEW_FACT" | "DEPRECATION" | "TYPE_CHANGE" | "MERGE" | "ROLLBACK"
  canon_type_pre:  CanonType | null
  canon_type_post: CanonType (ver Ontología)
  contenido:       string (descripción del hecho mutado)
  veredicto:       "CANON" | "CANON_CON_AJUSTE" | "RECHAZAR"
  firmado_por:     "Curador"
  aprobado_por:    "Custodio" | null
}
```

---

## Tipos Canónicos (referencia rápida)

| Tipo | Modificable | Autoridad |
|---|---|---|
| `HARD_CANON` | Solo en MAJOR | Custodio únicamente |
| `SOFT_CANON` | Sí, con veredicto AJUSTE | Curador + Custodio |
| `PROVISIONAL` | Sí, hasta cierre de sesión | Curador |
| `DEPRECATED` | No. Solo marcar. | Curador propone, Custodio aprueba |
| `COUNTERFACTUAL` | Solo dentro de su rama | Custodio |
| `SIMULATION_BRANCH` | Nunca persiste en corpus principal | Curador contiene |
| `PRIVATE_STATE` | Protegido del mapa compartido | Curador |
| `UNREVEALED` | Solo Curador y Custodio conocen | — |
| `PUBLIC_FACT` | Referenciable sin restricción | — |

---

## Versionado Semántico del Corpus

```
CORPUS_VERSION: MAJOR.MINOR.PATCH

MAJOR:  Reescribe HARD_CANON o redefine regla inviolable → solo Custodio
MINOR:  Bloque completo incorporado / conjunto HARD_CANON consolidado → Curador + Custodio  
PATCH:  PROVISIONAL → HARD_CANON / corrección SOFT_CANON → Curador veredicto
```

---

## Ejemplo de Entrada

```
AUDIT_ENTRY {
  session_id:      "SESSION_20260531_001"
  timestamp:       "2026-05-31T15:30:00-06:00"
  corpus_version:  "1.0.1"
  nodo:            "Curador"
  tipo_mutacion:   "NEW_FACT"
  canon_type_pre:  null
  canon_type_post: HARD_CANON
  contenido:       "El sistema opera en modo single-LLM por defecto cuando no se especifica arquitectura multi-nodo."
  veredicto:       "CANON"
  firmado_por:     "Curador"
  aprobado_por:    "Custodio"
}
```

---

## Registro de Sesiones

*(Append-only a partir de aquí)*

---

*AUDIT_LOG_TEMPLATE v1.0 · RUNTIME MASTER PROMPT · 2026*
