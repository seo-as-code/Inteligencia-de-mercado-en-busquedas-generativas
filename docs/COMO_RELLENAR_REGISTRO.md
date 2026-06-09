# Cómo rellenar el registro de medición

> Guía paso a paso para ejecutar una ronda de observación y registrar resultados en `datos/registro_medicion.csv`

---

## Antes de empezar

1. Copia las plantillas a `datos/` (ver [`datos/README.md`](../datos/README.md))
2. Rellena `datos/proyecto.yaml` con tu marca, competidores y mercado
3. Adapta `datos/consultas.yaml` con tus consultas por intención
4. Abre un buscador con IA y mantén el mismo motor durante toda la ronda

---

## Por cada consulta

### 1. Ejecutar la consulta

- Copia el `texto` de la consulta desde `datos/consultas.yaml`
- Pégalo en el buscador con IA tal cual, sin reformular
- Espera la respuesta completa antes de registrar

### 2. Observar tres señales

| Pregunta | Si sí → | Si no → |
|----------|---------|---------|
| ¿Aparece el nombre de tu marca (o un alias)? | `marca_mencionada` = **yes** | **no** |
| ¿Aparece tu dominio en las fuentes citadas? | `url_citada` = **yes** | **no** |
| ¿Qué otros dominios aparecen citados? | Escríbelos en `dominios_citados` | dejar vacío |

**Formato de `dominios_citados`:** separar con punto y coma, sin `https://`

```
competidor-a.com;competidor-b.com;marca-ejemplo.com
```

### 3. Elegir el `resultado`

| Resultado | Criterio |
|-----------|----------|
| **victory** | Mención + URL citada |
| **partial** | Mención sin URL, o URL sin mención explícita |
| **defeat** | Competidores citados; tu marca ausente |
| **ignored** | Sin mención ni cita |

### 4. Completar `dominio_ganador`

- Si tu URL fue la fuente principal → tu dominio
- Si ganó un competidor → dominio del rival más prominente
- Si no hay citas → dejar vacío

### 5. Anotar en `notas`

Registra lo relevante para la siguiente ronda:

- Posición de tu cita (`[1]`, `[2]`…)
- Tono con el que describen tu marca
- Alucinaciones (datos inventados sobre tu marca)
- Fragmento clave de la respuesta

---

## Ejemplo de fila completada

```csv
2026-06-09,com_01,"¿Cuál es el mejor software de gestión para pymes?",buscador-generativo,no,no,competidor-a.com;competidor-b.com,competidor-a.com,defeat,No aparecemos. Competidor A en [1].
```

Más ejemplos en [`plantillas/registro_medicion.ejemplo.csv`](../plantillas/registro_medicion.ejemplo.csv).

---

## Después de la ronda

### Calcular métricas básicas

| Métrica | Cálculo |
|---------|---------|
| Mention rate | Filas con `marca_mencionada=yes` / total consultas |
| Citation rate | Filas con `url_citada=yes` / total consultas |
| Victorias | Filas con `resultado=victory` |
| Brechas P1 | Consultas `comercial` o `comparativa` con `defeat` o `ignored` |

### Priorizar acciones

| Prioridad | Cuándo |
|-----------|--------|
| P0 | Crawl bloqueado o errores técnicos detectados en auditoría |
| P1 | `defeat` en consultas comerciales o comparativas |
| P2 | `ignored` en consultas informacionales |
| P3 | `partial` — hay mención pero falta cita |

### Repetir con la misma metodología

- Mismo set de consultas
- Mismo motor
- Mismo mercado e idioma
- Añadir consultas nuevas sin eliminar las existentes

---

## Columnas del CSV

| Columna | Descripción |
|---------|-------------|
| `fecha` | Fecha de la ronda (YYYY-MM-DD) |
| `consulta_id` | ID de `consultas.yaml` (ej. `com_01`) |
| `texto_consulta` | Texto exacto ejecutado |
| `motor` | Identificador del buscador usado |
| `marca_mencionada` | `yes` / `no` |
| `url_citada` | `yes` / `no` |
| `dominios_citados` | Dominios separados por `;` |
| `dominio_ganador` | Dominio principal de la respuesta |
| `resultado` | `victory` / `partial` / `defeat` / `ignored` |
| `notas` | Observaciones libres |

---

Marco completo: [`ESTUDIO_INTELIGENCIA_MERCADO_BUSQUEDA_GENERATIVA.md`](ESTUDIO_INTELIGENCIA_MERCADO_BUSQUEDA_GENERATIVA.md)
