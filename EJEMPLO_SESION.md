# EJEMPLO DE SESIÓN COMPLETA
## RUNTIME MASTER PROMPT v1.0 — Caso de Uso: Inteligencia Competitiva

---

## Contexto del Ejemplo

**Dominio:** Inteligencia competitiva sobre mercado de cómputo para IA  
**Corpus:** "COMPUTE_INTEL_2026"  
**Custodio:** Daniel Gómez Gamiño  
**Verdad central:** "Los vacíos regulatorios entre jurisdicciones son estructurales, no accidentales"  
**Modo:** Single-LLM (Claude asume Generador + Curador + Runtime)

---

## BLOQUE 0 — Definición de Dominio (rellenado)

```
DOMINIO:           inteligencia competitiva
NOMBRE DEL CORPUS: COMPUTE_INTEL_2026
CUSTODIO:          Daniel Gómez Gamiño
VERDAD CENTRAL:    "El cómputo es el recurso más escaso del ciclo 2025-2027. 
                    Quien controla el acceso legal al flujo de datos controla el input 
                    de la infraestructura cognitiva global."
LINGUA:            español
MODO:              single-LLM
```

---

## INICIO DE SESIÓN

```
SESSION_INIT {
  session_id:    "SESSION_20260531_001"
  objetivo:      análisis — identificar vectores de intermediación en mercado de cómputo LATAM
  foco:          gap entre demanda de inferencia en México y oferta estructurada en español
  modo:          Generador → Curador → Runtime
  pendientes:    ninguno (primera sesión)
  restricciones_activas:
    R1: Los datos de fuente primaria no se interpretan sin verificación externa
    R2: Una jurisdicción no puede anular a otra sin proceso explícito
    R4: Todo componente tiene historia previa trazable
    R5: Los vacíos son estructurales, no accidentes
}
```

---

## MODO GENERADOR

*[Claude declara: operando en Modo Generador]*

**Output generado:**

El mercado mexicano de acceso a LLMs presenta cinco fricciones estructurales identificables:

1. **Facturación**: los proveedores globales (OpenAI, Anthropic, Google) facturan en USD con tarjeta de crédito internacional. Las PYMEs mexicanas sin acceso a divisas quedan excluidas estructuralmente, no por precio sino por mecanismo de pago.

2. **Idioma técnico**: la documentación de APIs está en inglés. El equipo promedio de producto en empresa mexicana mediana no tiene capacidad técnica para integrar sin soporte en español.

3. **Soporte**: los proveedores globales no ofrecen soporte técnico en español con SLA definido para cuentas menores a $10K USD/mes.

4. **Compliance local**: las empresas mexicanas en sectores regulados (fintech, salud, legal) necesitan garantías de residencia de datos que los proveedores globales no documentan en español ni bajo jurisdicción mexicana.

5. **Escala de entrada**: los modelos de precios están optimizados para consumo en inglés a gran escala. El costo por token en español es hasta 40% mayor por la longitud promedio de tokens en castellano vs inglés.

**Oportunidad identificada**: intermediario que resuelve las cinco fricciones simultáneamente, comprando wholesale y revendiendo con capa de valor en español.

---

## MODO CURADOR

*[Claude declara: cambiando a Modo Curador — pausa explícita de rol]*

**Evaluando output del Generador contra corpus y suite de validación:**

| Bloque | Tests aplicados | Pass | Fail | BLOCKERs |
|---|---|---|---|---|
| A — Integridad estructural | 4 | 4 | 0 | 0 |
| B — Plausibilidad | 4 | 3 | 1 | 0 |
| C — Corpus | 3 | 3 | 0 | 0 |
| D — Tono | 2 | 2 | 0 | 0 |
| E — Autorización | 2 | 2 | 0 | 0 |

**Fallo identificado:**

| ID | Test | Severidad | Descripción | Acción |
|---|---|---|---|---|
| B2.1 | Historia previa trazable | 🟡 WARNING | El dato "40% mayor costo por token en español" no tiene fuente primaria citada | Marcar como PROVISIONAL hasta verificación |

**Veredicto:** `CANON_CON_AJUSTE`

**Ajuste aplicado:** El punto 5 sobre costo por token se reclasifica de afirmación a hipótesis operativa pendiente de verificación. Resto del output: CANON.

---

## MODO RUNTIME

*[Claude declara: operando en Modo Runtime — síntesis para el Custodio]*

**Resumen ejecutivo de sesión:**

El Generador identificó 5 fricciones estructurales en el mercado mexicano de acceso a LLMs. El Curador validó 4 de 5 como CANON. El punto 5 (diferencial de costo por token en español) requiere verificación de fuente primaria antes de usarse en propuesta comercial.

**Acción recomendada para el Custodio:** verificar el dato de costo por token en español consultando documentación de precios de OpenAI/Anthropic para tokens en castellano vs inglés.

---

## CIERRE DE SESIÓN

```markdown
## CIERRE DE SESIÓN — COMPUTE_INTEL_2026 / 2026-05-31

**Modo operado:** Generador → Curador → Runtime (single-LLM)
**Objetivo de sesión:** Identificar vectores de intermediación en mercado de cómputo LATAM

### Output generado
- Análisis de 5 fricciones estructurales en mercado mexicano de LLMs

### Veredictos emitidos
- Fricciones 1-4: CANON
- Fricción 5 (diferencial de costo por token): CANON_CON_AJUSTE (marcado PROVISIONAL)

### Nuevos hechos incorporados al corpus
- HARD_CANON: El mercado mexicano de LLMs tiene 4 fricciones estructurales verificables
- PROVISIONAL: Diferencial de costo por token en español vs inglés (~40%) — pendiente verificación

### Riesgos de continuidad identificados
- El dato de fricción 5 no debe usarse en propuesta comercial hasta verificación

### Próxima sesión recomendada
- Objetivo: verificar dato de costo por token + identificar compradores concretos por fricción
- Foco: segmento fintech/legal (fricción 4 — compliance local)
- Modo: Diagnóstico

### Estado del sistema
- Corpus versión: 1.0.1
- Tensión acumulada: baja
- Decisión abierta: verificación de fricción 5
```

---

## AUDIT LOG — Esta Sesión

```
AUDIT_ENTRY {
  session_id:      "SESSION_20260531_001"
  timestamp:       "2026-05-31T15:30:00-06:00"
  corpus_version:  "1.0.1"
  nodo:            "Curador"
  tipo_mutacion:   "NEW_FACT"
  canon_type_pre:  null
  canon_type_post: HARD_CANON
  contenido:       "El mercado mexicano de LLMs tiene 4 fricciones estructurales verificables: facturación en USD, documentación en inglés, soporte sin SLA en español, compliance local sin documentación jurisdiccional."
  veredicto:       "CANON"
  firmado_por:     "Curador"
  aprobado_por:    "Custodio"
}

AUDIT_ENTRY {
  session_id:      "SESSION_20260531_001"
  timestamp:       "2026-05-31T15:31:00-06:00"
  corpus_version:  "1.0.1"
  nodo:            "Curador"
  tipo_mutacion:   "NEW_FACT"
  canon_type_pre:  null
  canon_type_post: PROVISIONAL
  contenido:       "Diferencial de costo por token en español vs inglés estimado en ~40% por longitud promedio de tokens. Pendiente verificación en documentación oficial de proveedores."
  veredicto:       "CANON_CON_AJUSTE"
  firmado_por:     "Curador"
  aprobado_por:    null
}
```

---

*EJEMPLO_SESION.md · RUNTIME MASTER PROMPT v1.0 · 2026*
