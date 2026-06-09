# Inteligencia de mercado en búsquedas generativas

> Estudio informativo · Investigación en curso · v0.3 · Junio 2026
>
> Repositorio: **seo-as-code / Inteligencia de mercado en búsquedas generativas**

---

## Índice

**Introducción**
1. [Objeto de estudio](#1-objeto-de-estudio)
2. [Por qué conectar SEO y búsqueda generativa](#2-por-qué-conectar-seo-y-búsqueda-generativa)

**Qué observar**
3. [El entorno: dos sistemas de visibilidad](#3-el-entorno-dos-sistemas-de-visibilidad)
4. [Las tres capas de observación](#4-las-tres-capas-de-observación)
5. [Qué datos recoger](#5-qué-datos-recoger)
6. [Qué es observable y qué no](#6-qué-es-observable-y-qué-no)

**Qué hacer**
7. [Interpretar señales: matriz de diagnóstico](#7-interpretar-señales-matriz-de-diagnóstico)
8. [Acciones técnicas](#8-acciones-técnicas)
9. [Acciones de contenido y entidad](#9-acciones-de-contenido-y-entidad)
10. [Acciones de medición](#10-acciones-de-medición)

**Cómo hacerlo**
11. [Marco de trabajo paso a paso](#11-marco-de-trabajo-paso-a-paso)
12. [Métricas y criterios de evaluación](#12-métricas-y-criterios-de-evaluación)
13. [Cadencia y operación continua](#13-cadencia-y-operación-continua)

**Cierre**
14. [Limitaciones del estudio](#14-limitaciones-del-estudio)
15. [Implementación en este repositorio](#15-implementación-en-este-repositorio)
16. [Glosario](#16-glosario)

---

# Introducción

## 1. Objeto de estudio

Este documento estudia la **inteligencia de mercado en búsquedas generativas**: el análisis sistemático de cómo los buscadores con IA — motores que responden en lenguaje natural en lugar de devolver una lista de enlaces — están cambiando:

- Cómo los usuarios formulan preguntas y toman decisiones
- Qué marcas y URLs aparecen citadas en las respuestas
- Qué competidores ganan presencia en cada tipo de consulta
- Qué oportunidades y riesgos existen antes de que impacten en el tráfico medible

**No es un manual de herramientas.** Es un estudio que responde tres preguntas en orden:

| Pregunta | Sección |
|----------|---------|
| **¿Qué observar?** | Capas de datos, señales, fuentes |
| **¿Qué hacer?** | Acciones técnicas, editoriales y de medición |
| **¿Cómo hacerlo?** | Marco de trabajo, métricas, cadencia |

La inteligencia de mercado en este contexto no consiste en espiar conversaciones privadas. Consiste en **observar señales públicas y reproducibles**, cruzarlas con la base SEO existente y convertir los hallazgos en decisiones.

---

## 2. Por qué conectar SEO y búsqueda generativa

SEO y búsqueda generativa comparten el mismo activo — el contenido web — pero lo evalúan de forma distinta.

```
                    CONTENIDO WEB
                         │
         ┌───────────────┴───────────────┐
         ▼                               ▼
   BÚSQUEDA CLÁSICA              BÚSQUEDA GENERATIVA
   (índice de páginas)           (índice de respuestas)
         │                               │
         ▼                               ▼
   Posición, CTR                  Mención, cita,
   impresiones                    share of voice
         │                               │
         └───────────────┬───────────────┘
                         ▼
              TRÁFICO Y CONVERSIÓN
```

| Dimensión | Búsqueda clásica (SEO) | Búsqueda generativa |
|-----------|------------------------|---------------------|
| Formato de consulta | Keywords cortas (2–4 palabras) | Preguntas conversacionales (12–25 palabras) |
| Unidad de éxito | Página rankeada | Pasaje citado o marca mencionada |
| Métrica principal | Posición, CTR | Mention rate, citation rate |
| Competencia | Quién ocupa el SERP | Quién aparece en la respuesta sintetizada |
| Éxito sin clic | Secundario | Muy relevante |

**Conclusión del estudio:** tratar la búsqueda generativa como un canal independiente del SEO genera ceguera. La estrategia correcta es **una sola base técnica y de contenido** con **dos sistemas de medición**.

---

# Qué observar

## 3. El entorno: dos sistemas de visibilidad

Para observar con rigor, primero hay que entender qué agentes automatizados interactúan con tu sitio y con qué fin.

| Tipo de agente | Función | Qué observar |
|----------------|---------|--------------|
| Bot de búsqueda clásica | Indexar para resultados tradicionales | Frecuencia, URLs, errores — base SEO |
| Bot de índice generativo | Indexar para citar en respuestas de IA | Acceso, profundidad, páginas prioritarias |
| Bot de entrenamiento | Recoger datos para entrenar modelos | Política de acceso (opt-in / opt-out) |
| Fetcher de usuario | Leer URL cuando el usuario lo solicita | Páginas consultadas en tiempo real |

**Observación clave:** bloquear el bot de índice generativo equivale a ser invisible en ese buscador con IA, independientemente de lo bien que rankees en búsqueda clásica.

**Observación técnica:** muchos agentes generativos procesan HTML crudo con renderizado limitado de JavaScript. Un sitio legible para búsqueda clásica puede ser ilegible para buscadores con IA.

---

## 4. Las tres capas de observación

La inteligencia de mercado se construye observando **tres capas**. No deben mezclarse: cada una responde una pregunta distinta.

```
CAPA 1 — CRAWL          ¿Los agentes acceden a mi sitio?
CAPA 2 — VISIBILIDAD    ¿Aparezco en respuestas generadas?
CAPA 3 — TRÁFICO        ¿Llegan usuarios desde buscadores con IA?
```

| Capa | Pregunta | Tipo de indicador | Naturaleza |
|------|----------|-------------------|------------|
| **1. Crawl** | ¿Me indexan los agentes generativos? | Adelantado | Señal de acceso |
| **2. Visibilidad** | ¿Me mencionan o citan? | De resultado | Señal de presencia |
| **3. Tráfico** | ¿Me visitan? | Rezagado | Señal de conversión |

### Cómo leer las tres capas juntas

| Patrón | Qué indica |
|--------|------------|
| Crawl alto + visibilidad baja | Acceso correcto, contenido poco citables o poco relevante |
| Visibilidad alta + tráfico bajo | La respuesta basta sin clic; medir presencia como KPI |
| Tráfico sin visibilidad previa | Fetch en tiempo real; el usuario pidió una URL concreta |
| Crawl bloqueado | Problema técnico o de política; prioridad máxima |

---

## 5. Qué datos recoger

### 5.1 Datos técnicos — base compartida SEO + generativo

| Dato | Para qué observar |
|------|-------------------|
| Estado de indexación | Qué páginas existen para ambos sistemas |
| Errores de crawl (4xx, 5xx) | Barreras de acceso para agentes |
| Reglas de `robots.txt` | Qué agentes pueden entrar y cuáles no |
| Rendimiento (velocidad, CWV) | Capacidad de procesamiento eficiente |
| Schema y datos estructurados | Claridad de entidades para los agentes |
| Arquitectura de URLs | Qué secciones priorizan los crawlers |

### 5.2 Datos de visibilidad generativa

| Dato | Para qué observar |
|------|-------------------|
| Set de consultas por intención | Universo de medición del mercado |
| Mención de marca | Presencia en respuestas |
| Citación de URL | Fuentes que el buscador considera autoridad |
| Dominios competidores citados | Mapa competitivo por consulta |
| Tono y framing | Cómo describen tu marca |
| Alucinaciones | Datos inventados que distorsionan la percepción |

### 5.3 Datos de mercado y negocio

| Dato | Para qué observar |
|------|-------------------|
| Referrals desde buscadores con IA | Tráfico real derivado de respuestas |
| Conversiones por canal | Impacto en negocio |
| Consultas de ventas y soporte | Formulaciones reales del mercado |
| Keywords clásicas con volumen | Semilla para consultas conversacionales |
| Tendencias de adopción por sector | Evolución del canal generativo |

---

## 6. Qué es observable y qué no

### No es observable

- El prompt exacto que escribe cada usuario en un asistente conversacional
- El algoritmo interno de selección de fuentes de cada modelo
- El peso de cada señal dentro de una respuesta generada

### Sí es observable con método

| Qué observas | Cómo | Limitación |
|--------------|------|------------|
| Actividad de agentes en tu sitio | Logs del servidor | No predice citación |
| Respuestas a consultas definidas | Ejecución periódica de prompts | Es una muestra, no el universo |
| Patrones de consulta por sector | Bases agregadas de investigación | Estimaciones de mercado |
| Tráfico post-respuesta | Analytics de referrals | No revela la pregunta original |
| Barreras técnicas | Auditoría on-page y de acceso | No mide percepción de marca |

**Principio del estudio:** la inteligencia de mercado en búsquedas generativas se construye con **muestras controladas**, **patrones agregados** y **cruces entre capas**.

---

# Qué hacer

## 7. Interpretar señales: matriz de diagnóstico

Observar sin interpretar no produce inteligencia. Esta matriz conecta señales de distintas capas con acciones concretas.

| Lo que observas (SEO) | Lo que observas (generativo) | Diagnóstico | Qué hacer |
|-----------------------|------------------------------|-------------|-----------|
| Página indexada | No citada | Contenido poco citables | Reformular pasajes, añadir datos |
| No indexada | No citada | Problema de acceso | Priorizar técnico |
| Bien posicionada | Competidor citado | Brecha de formato o autoridad | Crear contenido comparativo |
| Crawl generativo alto | Citation rate bajo | Relevancia del pasaje insuficiente | Reestructurar bloques |
| Citation rate alto | Tráfico bajo | Respuesta autosuficiente | Reforzar marca y CTA |
| Alucinación detectada | Mención presente | Riesgo reputacional | Publicar datos oficiales |

---

## 8. Acciones técnicas

Acciones sobre la infraestructura web. Sin ellas, el resto no funciona.

| Acción | Qué resuelve | Capa afectada |
|--------|--------------|---------------|
| Auditar y configurar `robots.txt` | Acceso diferenciado por tipo de agente | Crawl |
| Garantizar HTML legible sin depender solo de JS | Legibilidad para agentes generativos | Crawl + SEO |
| Implementar Schema.org (Organization, FAQ, Article…) | Claridad de entidades | Visibilidad |
| Mantener sitemap actualizado | Descubrimiento de URLs prioritarias | Crawl |
| Resolver errores 4xx/5xx en peticiones de bots | Acceso continuo | Crawl |
| Optimizar velocidad de carga | Mejor procesamiento y UX | Crawl + tráfico |
| Definir canonical y eliminar duplicados | Una fuente de verdad por contenido | Ambas capas |
| Publicar `llms.txt` (opcional) | Guía de contenido relevante para agentes | Crawl |

---

## 9. Acciones de contenido y entidad

Acciones sobre lo que los buscadores con IA leen, interpretan y citan.

| Acción | Por qué | Intención que cubre |
|--------|---------|---------------------|
| Responder preguntas con la formulación conversacional exacta | Match con consultas reales | Todas |
| Añadir densidad factual: precios, fechas, cifras, tablas | Los agentes prefieren datos verificables | Comercial, comparativa |
| Crear bloques autocontenidos (pasajes citables) | Los agentes citan fragmentos, no páginas enteras | Todas |
| Publicar comparativas con criterios explícitos | Formato altamente citables | Comparativa |
| Mostrar autoría, credenciales y fecha de actualización | Señales E-E-A-T | Informacional |
| Incluir prueba social y casos propios | Diferenciación en respuestas | Comercial, branded |
| Cubrir el embudo completo: info, comercial, transaccional, branded | Presencia en todo el recorrido | Todas |
| Corregir alucinaciones con datos oficiales publicados | Control de narrativa | Branded |

---

## 10. Acciones de medición

Sin medición periódica no hay inteligencia de mercado: solo intuición.

| Acción | Frecuencia sugerida | Output |
|--------|---------------------|--------|
| Definir set de consultas por intención | Una vez; revisar trimestralmente | Inventario de observación |
| Ejecutar y registrar respuestas | Semanal o quincenal | Registro estructurado |
| Monitorizar crawl de agentes generativos | Continuo | Dashboard de acceso |
| Calcular mention rate y citation rate | Por cada ronda | Scoreboard |
| Identificar brechas de citación | Por cada ronda | Lista priorizada de gaps |
| Cruzar visibilidad con referrals | Mensual | Correlación presencia → tráfico |
| Registrar alucinaciones | Por cada ronda | Cola de correcciones |
| Comparar rondas en el tiempo | Mensual | Tendencia y efecto de cambios |

---

# Cómo hacerlo

## 11. Marco de trabajo paso a paso

Este es el protocolo operativo del estudio. Cada paso tiene un input, una acción y un output.

### Paso 1 — Definir el mercado observado

| Elemento | Qué definir |
|----------|-------------|
| Marca y variantes | Nombre, dominio, alias |
| Competidores | Lista cerrada de rivales directos |
| Mercado | Idioma, región, vertical |
| Intenciones | Informacional, comercial, comparativa, branded |

**Output:** `datos/proyecto.yaml`

---

### Paso 2 — Establecer línea base técnica (SEO)

| Acción | Cómo |
|--------|------|
| Auditar indexación | Consola de búsqueda + crawl propio |
| Revisar `robots.txt` | Comprobar acceso de agentes generativos |
| Evaluar legibilidad HTML | Contenido crítico sin dependencia exclusiva de JS |
| Verificar schema | Entidades principales marcadas |

**Output:** informe de acceso y salud técnica.

---

### Paso 3 — Inventariar consultas de observación

| Fuente de consultas | Cómo obtenerlas |
|---------------------|-----------------|
| Keywords clásicas con volumen | Reformular a lenguaje conversacional |
| Preguntas de ventas y soporte | Extraer formulaciones reales |
| Brechas competitivas | "¿Cuál es el mejor X?" donde no apareces |
| Consultas branded | "¿Qué es [marca]?", "¿[marca] vs [rival]?" |

**Output:** `datos/consultas.yaml`

---

### Paso 4 — Medir visibilidad generativa

| Acción | Cómo |
|--------|------|
| Ejecutar cada consulta en buscadores con IA | Misma formulación, mismo mercado |
| Registrar respuesta completa | Texto, fuentes citadas, competidores |
| Clasificar resultado | victory / partial / defeat / ignored |
| Anotar tono y alucinaciones | Framing + correcciones pendientes |

**Output:** `datos/registro_medicion.csv`

Guía detallada: [`COMO_RELLENAR_REGISTRO.md`](COMO_RELLENAR_REGISTRO.md)

---

### Paso 5 — Cruzar capas

| Cruce | Cómo |
|-------|------|
| Crawl + visibilidad | ¿Las páginas más visitadas por agentes son las citadas? |
| Visibilidad + tráfico | ¿Las consultas con cita generan referrals? |
| SEO clásico + generativo | ¿Las URLs bien posicionadas son las citadas? |

**Output:** matriz de diagnóstico (sección 7).

---

### Paso 6 — Priorizar y actuar

| Prioridad | Criterio |
|-----------|----------|
| P0 | Acceso bloqueado o errores críticos de crawl |
| P1 | Brechas de citación en intención comercial |
| P2 | Contenido informacional sin presencia |
| P3 | Optimización de formato y entidades |

**Output:** plan de acción con briefs de contenido y tareas técnicas.

---

### Paso 7 — Repetir con la misma metodología

| Regla | Por qué |
|-------|---------|
| Mismo set de consultas entre rondas | Comparabilidad |
| Misma cadencia (semanal / quincenal) | Detección de tendencias |
| Añadir consultas nuevas sin eliminar las existentes | Ampliar cobertura sin romper la serie |

**Output:** serie temporal comparable entre rondas.

---

## 12. Métricas y criterios de evaluación

### Métricas de visibilidad generativa

| Métrica | Definición | Cómo calcularla |
|---------|------------|-----------------|
| Mention rate | Presencia de marca en respuestas | Menciones / total consultas |
| Citation rate | Presencia de URL como fuente | Citas / total consultas |
| Share of voice | Peso relativo vs. competidores | Tu presencia / presencia total del sector |
| Framing | Tono de la descripción | Clasificación: positivo, neutral, negativo, mixto |
| Shortlist position | Posición en listas comparativas | 1, 2, 3… o ausente |

### Niveles de penetración

```
ignored  →  mentioned  →  recommended  →  cited
(ausente)   (nombrado)    (recomendado)    (URL citada)
```

### Resultados por consulta

| Resultado | Criterio |
|-----------|----------|
| victory | Mención + cita |
| partial | Mención sin cita, o cita sin mención explícita |
| defeat | Competidores presentes; marca ausente |
| ignored | Sin mención ni cita |

### Métricas SEO que siguen alimentando el estudio

| Métrica | Por qué sigue siendo relevante |
|---------|-------------------------------|
| Posición media | Proxy de autoridad temática |
| Páginas indexadas | Base de acceso para ambos sistemas |
| CTR orgánico | Salud del canal clásico |
| Impresiones | Demanda del tema en el mercado |

---

## 13. Cadencia y operación continua

```
SEMANAL / QUINCENAL          MENSUAL                    TRIMESTRAL
─────────────────────        ─────────────────          ─────────────────
Ejecutar consultas           Cruzar capas               Revisar set de
Registrar mediciones         Scoreboard comparativo      consultas
Detectar alucinaciones       Correlación tráfico        Ampliar competidores
                             Informe de brechas         Evaluar nuevas
                                                          intenciones
```

| Rol | Responsabilidad |
|-----|-----------------|
| Técnico | Acceso, crawl, schema, errores |
| Contenido | Briefs a partir de brechas de citación |
| Analista | Registros, scoreboards, cruces |
| Estrategia | Priorización P0–P3 e interpretación de mercado |

---

# Cierre

## 14. Limitaciones del estudio

1. No hay acceso a conversaciones privadas de usuarios en tiempo real
2. Los resultados varían por modelo, versión, región e idioma
3. Las muestras de consultas no representan el universo completo
4. Los modelos alucinan: los datos inventados deben detectarse y corregirse
5. Correlación no implica causalidad: crawl ≠ citación ≠ tráfico
6. El ecosistema evoluciona rápido: nuevos agentes y formatos de respuesta

Todo informe derivado de este estudio debe documentar: **fecha, buscadores evaluados, set de consultas, idioma y mercado**.

---

## 15. Implementación en este repositorio

Este repositorio materializa el protocolo del estudio con plantillas listas para usar.

| Ruta | Función en el protocolo |
|------|-------------------------|
| `plantillas/proyecto.ejemplo.yaml` | Paso 1 — definir mercado, marca y competidores |
| `plantillas/consultas.ejemplo.yaml` | Paso 3 — inventario de consultas por intención |
| `plantillas/registro_medicion.csv` | Paso 4 — plantilla vacía del registro |
| `plantillas/registro_medicion.ejemplo.csv` | Referencia con filas ficticias |
| `datos/` | Copia local de trabajo (no se sube a Git) |
| `docs/COMO_RELLENAR_REGISTRO.md` | Guía operativa del Paso 4 |

```
plantillas/  →  copiar a datos/  →  rellenar  →  medir  →  cruzar  →  actuar  →  repetir
```

Para análisis automatizado y scoreboards avanzados, el ecosistema **SEO-as-Code** ofrece herramientas complementarias de implementación técnica.

---

## 16. Glosario

| Término | Definición |
|---------|------------|
| **Inteligencia de mercado** | Análisis sistemático de señales competitivas y de demanda |
| **Búsqueda generativa** | Modalidad donde el motor responde en lenguaje natural |
| **Buscador con IA** | Motor que sintetiza respuestas a partir de fuentes web |
| **SEO** | Optimización para búsqueda clásica basada en índice de páginas |
| **GEO** | Optimización para presencia en respuestas generativas |
| **Share of voice** | Proporción de menciones o citas de tu marca frente al sector |
| **Citation gap** | Consulta donde un competidor es citado y tú no |
| **Prompt / consulta** | Pregunta en lenguaje natural enviada a un buscador con IA |
| **Framing** | Tono y contexto con el que un motor describe tu marca |
| **Registro de medición** | Archivo estructurado de una ronda de observación |
| **Penetration level** | Grado de presencia: ignorado → mencionado → recomendado → citado |
| **Fetcher** | Agente que lee una URL bajo demanda del usuario |

---

*Estudio de investigación · seo-as-code · v0.3 · Junio 2026*
