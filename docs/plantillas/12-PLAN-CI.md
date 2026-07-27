# 12 — Plan de integración continua (plantilla)

## 1. Objetivo

`[RELLENAR]`

*Ej: Cada push valida build y pruebas básicas de API/app.*

## 2. Repositorios

| Repo | Tecnología | CI |
|------|------------|-----|
| API | Spring Boot | `[RELLENAR]` *GitHub Actions* |
| iOS | Xcode | `[RELLENAR]` *manual / Actions macOS si aplica* |
| Docs | Markdown | — |

## 3. Pipeline propuesto (API)

1. Checkout  
2. Build (`./mvnw package` o Gradle)  
3. Unit tests  
4. (Opcional) Rest Assured smoke  
5. Publicar artefacto / imagen  

## 4. Triggers

| Evento | Acción |
|--------|--------|
| Push a `main` | `[RELLENAR]` |
| Pull Request | `[RELLENAR]` |

## 5. Quality gates

- `[RELLENAR]` *Build OK*
- `[RELLENAR]` *Tests verdes*
- `[RELLENAR]`

## 6. Responsables

| Actividad | Quién |
|-----------|-------|
| Mantener CI | `[RELLENAR]` |
| Revisar fallos | `[RELLENAR]` |

## 7. Estado actual

- [ ] CI configurado  
- [ ] Badge en README  
- [ ] Documentado en este plan  

Notas: `[RELLENAR]`
