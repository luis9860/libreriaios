# 06 — Interesados y riesgos (plantilla completa con ejemplos)

---

## 1. Interesados — EJEMPLO COMPLETO

| Interesado | Rol / interés | Influencia | Estrategia |
|------------|---------------|------------|------------|
| Equipo de desarrollo | Entregar MVP y notas | Alta | Trello + sprints |
| Product Owner (equipo) | Priorizar backlog | Alta | Refinamiento semanal |
| Docente Proyecto Integrador | Evaluar AT01/AT02/EF | Alta | Cumplir rúbricas y fechas |
| Docente Móviles II | App iOS REST+Core Data | Alta | Avances semanales + video |
| Docente Pruebas | Artefactos de prueba API | Alta | Plan + automatización Java |
| Usuario lector | Alquilar fácil | Media | UX simple + Watson |
| Admin biblioteca | Control inventario | Media | Módulo admin claro |
| `[RELLENAR]` | | | *Añade sponsor u otros* |

---

## 2. Matriz de riesgos — EJEMPLO COMPLETO

| ID | Riesgo | Prob. | Impacto | Mitigación | Contingencia |
|----|--------|-------|---------|------------|--------------|
| R01 | API Spring Boot atrasa y bloquea iOS | M | A | Sprint 1 enfocado en API + contrato OpenAPI | Mock JSON local temporal |
| R02 | Facebook Login / App Review / keys | M | M | Configurar App Meta temprano | Priorizar email; Facebook en paralelo |
| R03 | Cuenta Watson / límites free | M | M | Configurar en Unidad 2; intents simples | FAQ estática en app |
| R04 | Alcance crece (delivery, multas) | A | A | MVP firmado en Kickoff/Alcance | Rechazar OUT o mover a R2 |
| R05 | Confusión Word vs Markdown en entregas | M | B | MD en repo; export Word al entregar | Plantillas Word puntuales |
| R06 | No hay Mac/Xcode estable | M | A | Definir entorno ya | Simulador + máquina lab Cibertec |
| R07 | Yape real no integrable a tiempo | A | M | Simular PaymentService con mismos campos UI | Documentar como futuro |
| R08 | `[RELLENAR]` | | | | |

Prob./Impacto: A=Alta, M=Media, B=Baja.
