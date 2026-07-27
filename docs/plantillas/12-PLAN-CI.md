# 12 — Plan de CI (plantilla completa con ejemplos)

---

## 1. Objetivo — EJEMPLO

Cada push/PR a la API ejecuta build + tests unitarios automáticamente (GitHub Actions). La app iOS se valida al menos con build manual en Xcode cada sprint (CI macOS opcional).

## 2. Repos — EJEMPLO

| Repo | CI propuesto |
|------|----------------|
| `libreriaios` (docs + luego monorepo o subcarpeta api/) | Actions para API |
| App iOS | Build local Xcode; Actions si hay runner macOS |

## 3. Pipeline API — EJEMPLO

```yaml
# Idea (no es el archivo final todavía)
# on: [push, pull_request]
# jobs:
#   build:
#     runs-on: ubuntu-latest
#     steps: checkout → setup-java → mvn test → mvn package
```

Pasos: Checkout → JDK 17 → `mvn test` → artefacto jar.

## 4. Triggers — EJEMPLO

| Evento | Acción |
|--------|--------|
| Push `main` | Build + test |
| Pull Request | Build + test (bloquear merge si falla) |

## 5. Quality gates — EJEMPLO

- [ ] Compila  
- [ ] Unit tests OK  
- [ ] (Luego) smoke Rest Assured  

## 6. Responsables

| Actividad | Quién |
|-----------|-------|
| Mantener workflow | `[RELLENAR]` |
| Revisar fallos CI | Development Team |

## 7. Estado actual

- [ ] Carpeta API creada  
- [ ] Workflow añadido  
- [ ] Badge en README  

Notas: `[RELLENAR]` *CI se implementa cuando exista el código Spring Boot (Sprint 1).*
