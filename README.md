# Inteligencia de mercado en búsquedas generativas

[![Licencia: MIT](https://img.shields.io/badge/Licencia-MIT-blue.svg)](LICENSE)
[![Organización: seo-as-code](https://img.shields.io/badge/org-seo--as--code-green.svg)](https://github.com/seo-as-code)

Estudio y protocolo práctico para analizar cómo los buscadores con IA están transformando la visibilidad de marcas, la competencia en respuestas generadas y las oportunidades de posicionamiento.

Conecta **SEO** (búsqueda clásica) y **GEO** (búsqueda generativa) en una estrategia medible, reproducible y sin dependencia de herramientas comerciales.

---

## Para quién es

| Perfil | Uso |
|--------|-----|
| **SEO / Marketing** | Entender el nuevo canal de visibilidad generativa |
| **Estrategia** | Detectar oportunidades y riesgos competitivos antes del impacto en tráfico |
| **Analistas** | Aplicar un protocolo de medición con plantillas listas para usar |
| **Equipos técnicos** | Alinear acceso de crawlers, contenido y datos estructurados |

---

## Qué encontrarás aquí

| Documento | Contenido |
|-----------|-----------|
| [Estudio completo](docs/ESTUDIO_INTELIGENCIA_MERCADO_BUSQUEDA_GENERATIVA.md) | Marco conceptual: qué observar, qué hacer, cómo hacerlo |
| [Guía de registro](docs/COMO_RELLENAR_REGISTRO.md) | Protocolo paso a paso para cada ronda de medición |
| [Plantillas](plantillas/) | YAML y CSV de ejemplo, listos para copiar |
| [Datos locales](datos/) | Carpeta de trabajo personal (excluida de Git) |
| [Guia de contribucion](CONTRIBUTING.md) | Como proponer mejoras al estudio y plantillas |
| [Seguridad y datos](SECURITY.md) | Politica sobre datos sensibles y que no subir a Git |

---

## Inicio rápido

### 1. Leer el marco

Empieza por el [estudio](docs/ESTUDIO_INTELIGENCIA_MERCADO_BUSQUEDA_GENERATIVA.md). Responde tres preguntas en orden:

1. **¿Qué observar?** — Crawl, visibilidad y tráfico
2. **¿Qué hacer?** — Acciones técnicas, de contenido y de medición
3. **¿Cómo hacerlo?** — Protocolo en 7 pasos con métricas y cadencia

### 2. Preparar tu entorno local

```powershell
# Desde la raíz del repositorio
Copy-Item plantillas\proyecto.ejemplo.yaml      datos\proyecto.yaml
Copy-Item plantillas\consultas.ejemplo.yaml     datos\consultas.yaml
Copy-Item plantillas\registro_medicion.csv      datos\registro_medicion.csv
```

Equivalente en Linux / macOS:

```bash
cp plantillas/proyecto.ejemplo.yaml   datos/proyecto.yaml
cp plantillas/consultas.ejemplo.yaml  datos/consultas.yaml
cp plantillas/registro_medicion.csv   datos/registro_medicion.csv
```

### 3. Configurar y medir

1. Edita `datos/proyecto.yaml` — marca, competidores, mercado
2. Adapta `datos/consultas.yaml` — consultas por intención
3. Ejecuta cada consulta en un buscador con IA
4. Registra resultados en `datos/registro_medicion.csv`
5. Repite con la misma cadencia para comparar rondas

Guía detallada: [Cómo rellenar el registro](docs/COMO_RELLENAR_REGISTRO.md)

---

## Estructura del repositorio

```text
.
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── SECURITY.md
├── docs/
│   ├── ESTUDIO_INTELIGENCIA_MERCADO_BUSQUEDA_GENERATIVA.md
│   └── COMO_RELLENAR_REGISTRO.md
├── plantillas/
│   ├── proyecto.ejemplo.yaml
│   ├── consultas.ejemplo.yaml
│   ├── registro_medicion.csv
│   └── registro_medicion.ejemplo.csv
└── datos/                  ← trabajo local (no se sube a Git)
    └── README.md
```

---

## Las tres capas de observación

```text
CAPA 1 — CRAWL        →  ¿Los agentes acceden a mi sitio?
CAPA 2 — VISIBILIDAD  →  ¿Aparezco en respuestas generadas?
CAPA 3 — TRÁFICO       →  ¿Llegan usuarios desde buscadores con IA?
```

La inteligencia de mercado surge al **cruzar las tres capas**, no al mirar una sola.

---

## Privacidad y datos

- Las plantillas usan **datos ficticios** (`marca-ejemplo.com`, competidores genéricos).
- La carpeta `datos/` está en `.gitignore` — tus registros reales **no se suben** a Git.
- No incluyas credenciales, URLs internas ni información de clientes en commits.
- Consulta [SECURITY.md](SECURITY.md) para la política completa.

---

## Qué no incluye este repositorio

- Scripts de análisis automatizado
- Datos reales de proyectos ni registros completados
- Integraciones con plataformas comerciales de terceros

Para implementación técnica avanzada, consulta el ecosistema [SEO-as-Code Toolkit](https://github.com/seo-as-code/SEO-as-Code-Toolkit).

---

## Contribuir

Consulta [CONTRIBUTING.md](CONTRIBUTING.md). Las mejoras al estudio, las plantillas y la documentación son bienvenidas mediante issues o pull requests.

---

## Licencia

[MIT](LICENSE) — uso, modificación y distribución libres con atribución.

---

## Organización

Desarrollado por [seo-as-code](https://github.com/seo-as-code) — procesos de SEO medibles, versionados y reproducibles.
