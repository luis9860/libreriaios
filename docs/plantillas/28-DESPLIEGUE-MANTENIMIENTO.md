# 28 — Despliegue y mantenimiento — plantilla con ejemplos

> Cubre el video: estrategias de despliegue, soporte, mejora continua.

## 1. Estrategia de despliegue — EJEMPLO (MVP académico)

| Componente | Estrategia |
|------------|------------|
| API | Ejecutar en laptop/lab o cloud free (Railway/Render/etc.) `[RELLENAR]` |
| App iOS | Build Debug en simulador/dispositivo para demo (TestFlight opcional) |
| BD | H2/dev o PostgreSQL managed |

## 2. Pasos de release demo

1. Seed datos  
2. Levantar API  
3. Apuntar app a Base URL  
4. Smoke CP01–CP08  
5. Ensayo demo 10 min  

Detalle instalación: ver `17-MANUAL-INSTALACION`.

## 3. Soporte y actualizaciones — EJEMPLO

- Canal: WhatsApp/email equipo `[RELLENAR]`  
- Bugs: card Trello etiqueta `Bloqueado`/`Bug`  
- Actualizaciones post-EF: backlog Could (delivery, multas, Yape real)

## 4. Feedback y mejora continua

- Retro de cada sprint (`15-INFORME-SPRINT`)  
- Feedback docente en avances Móviles  
- Futuro: ver `30-CONCLUSION-FUTURO`
