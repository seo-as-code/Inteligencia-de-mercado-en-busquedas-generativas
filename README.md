# Inteligencia de mercado en búsquedas generativas

Estudio y protocolo práctico para analizar cómo los buscadores con IA están cambiando la visibilidad de marcas, la competencia en respuestas generadas y las oportunidades de posicionamiento.

Conecta **SEO** (búsqueda clásica) y **GEO** (búsqueda generativa) en una sola estrategia medible.

---

## Contenido del repositorio

| Ruta | Qué es |
|------|--------|
| [`docs/ESTUDIO_INTELIGENCIA_MERCADO_BUSQUEDA_GENERATIVA.md`](docs/ESTUDIO_INTELIGENCIA_MERCADO_BUSQUEDA_GENERATIVA.md) | Estudio completo: qué observar, qué hacer, cómo hacerlo |
| [`docs/COMO_RELLENAR_REGISTRO.md`](docs/COMO_RELLENAR_REGISTRO.md) | Guía paso a paso para registrar cada ronda de medición |
| [`plantillas/`](plantillas/) | Archivos de ejemplo listos para copiar y rellenar |
| [`datos/`](datos/) | Carpeta local para tus registros (no se sube a Git) |

---

## Inicio rápido

```text
1. Lee el estudio          →  docs/ESTUDIO_INTELIGENCIA_MERCADO_BUSQUEDA_GENERATIVA.md
2. Copia las plantillas    →  plantillas/ → datos/
3. Configura tu mercado    →  datos/proyecto.yaml
4. Define tus consultas    →  datos/consultas.yaml
5. Mide y registra         →  datos/registro_medicion.csv
6. Repite con la misma cadencia para comparar rondas
```

### Copiar plantillas (Windows)

```powershell
Copy-Item plantillas\proyecto.ejemplo.yaml      datos\proyecto.yaml
Copy-Item plantillas\consultas.ejemplo.yaml     datos\consultas.yaml
Copy-Item plantillas\registro_medicion.csv      datos\registro_medicion.csv
```

---

## Estructura del estudio

El documento responde tres preguntas en orden:

1. **¿Qué observar?** — Tres capas: crawl, visibilidad, tráfico
2. **¿Qué hacer?** — Acciones técnicas, de contenido y de medición
3. **¿Cómo hacerlo?** — Protocolo en 7 pasos con métricas y cadencia

---

## Qué no incluye este repositorio

- Scripts de análisis automatizado (ver [SEO-as-Code Toolkit](https://github.com/seo-as-code/SEO-as-Code-Toolkit))
- Datos reales de clientes ni registros de medición completados
- Dependencia de herramientas comerciales de terceros

---

## Licencia

MIT — ver [LICENSE](LICENSE).

---

## Organización

Parte del ecosistema [seo-as-code](https://github.com/seo-as-code).
