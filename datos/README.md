# Datos locales

Copia aquí las plantillas desde `plantillas/` y rellénalas con tu proyecto.

```powershell
Copy-Item ..\plantillas\proyecto.ejemplo.yaml      proyecto.yaml
Copy-Item ..\plantillas\consultas.ejemplo.yaml     consultas.yaml
Copy-Item ..\plantillas\registro_medicion.csv      registro_medicion.csv
```

Los archivos de esta carpeta **no se suben a Git** (están en `.gitignore`).

Guía de rellenado: [`docs/COMO_RELLENAR_REGISTRO.md`](../docs/COMO_RELLENAR_REGISTRO.md)
