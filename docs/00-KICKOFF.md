# Kickoff del Proyecto

> Plantilla corporativa — Proyecto Integrador (Cibertec)  
> Completa los campos `[RELLENAR]`. Los textos en *cursiva* son **ejemplos** (bórralos o déjalos de guía).

---

## 1. Datos generales

| Campo | Valor |
|-------|--------|
| Nombre del sistema | `[RELLENAR]` *Ej: LibreriaRent / BookLease Perú* |
| Nombre corto / código | `[RELLENAR]` *Ej: LR-2026* |
| Fecha de kickoff | `[RELLENAR]` *Ej: 2026-07-26* |
| Ciclo / aula | `[RELLENAR]` *Ej: Sexto ciclo — aula XXX* |
| Coordinador del grupo | `[RELLENAR]` |
| Integrantes | `[RELLENAR]` *Ej: Nombre1, Nombre2* |

### Cursos que abarca (proyecto integrador)

- [x] Desarrollo de Aplicaciones Móviles II (4696)
- [x] Proyecto Integrador (2423)
- [x] Pruebas de Software (2424)

---

## 2. Problema en una frase

`[RELLENAR]`

*Ejemplo: Las bibliotecas o negocios de alquiler de libros físicos pierden control de ejemplares, garantías y plazos porque el proceso se hace a mano o sin una app unificada.*

---

## 3. Solución en una frase

`[RELLENAR]`

*Ejemplo: App iOS + API Spring Boot para reservar/alquilar ejemplares con UID, pagar con Yape (alquiler + garantía), recoger y devolver en local, con login email/Facebook y asistente Watson.*

---

## 4. Roles Scrum

| Rol | Responsable | Notas |
|-----|-------------|--------|
| Product Owner | `[RELLENAR]` | *Define prioridad del backlog* |
| Scrum Master | `[RELLENAR]` | *Cuida el proceso Scrum / Trello* |
| Development Team | `[RELLENAR]` | *API, iOS, pruebas, docs* |

*Si trabajas solo: pon tu nombre en los 3 roles y anótalo.*

---

## 5. Tablero Trello

| Campo | Valor |
|-------|--------|
| URL del tablero | `[RELLENAR]` *Ej: https://trello.com/b/xxxx/libreriarent* |
| Columnas | Backlog \| Sprint actual \| En progreso \| En prueba \| Hecho |

### Convención de cards

- Una card = una historia de usuario o tarea técnica
- Etiquetas sugeridas: `iOS` `API` `Docs` `Watson` `Pruebas` `Bloqueado`

---

## 6. Alcance acordado (MVP)

### Incluye

- [x] Títulos + ejemplares con UID
- [x] Login email/contraseña + **Facebook** (Móviles U4)
- [x] Pago Yape (celular + código de verificación) = alquiler + garantía
- [x] Recojo y devolución **solo en biblioteca**
- [x] Plazo del alquiler corre **desde el pago**
- [x] REST (Spring Boot) + Core Data + Firebase
- [x] Watson Assistant
- [x] Roles admin y usuario

### No incluye (MVP)

- [ ] Delivery a domicilio
- [ ] Venta definitiva de libros
- [ ] Multas automáticas
- [ ] Varias sucursales

---

## 7. Stack técnico acordado

| Capa | Tecnología |
|------|------------|
| App móvil | iOS, UIKit, Storyboard, MVC modular |
| Persistencia local | Core Data |
| Backend | Java Spring Boot (REST) |
| Nube / auth extra | Firebase + Facebook Login |
| Gestión | Scrum + Trello |
| IA | IBM Watson |
| Pruebas | Java (JUnit, Rest Assured, etc.) sobre la API |

---

## 8. Próximo hito

| Hito | Entregable | Fecha objetivo |
|------|------------|----------------|
| AT01 | Problemática, justificación, SEPTE, alcance, riesgos, viabilidad, Product Backlog | `[RELLENAR]` |
| AT02 | Release Plan, Sprint Backlogs, Plan de pruebas, Plan CI | `[RELLENAR]` |
| Sprint 1–2 | Incremento funcional (API + iOS) | `[RELLENAR]` |

---

## 9. Definition of Done (DoD) básica

Una historia está **Hecho** cuando:

1. Código en el repo / build OK
2. Cumple criterio de aceptación
3. Probada (manual o automatizada según el plan)
4. Card movida a **Hecho** en Trello
5. Documentado lo mínimo (si aplica)

---

## 10. Acuerdos del equipo

- `[RELLENAR]` *Ej: Daily asíncrono por WhatsApp 9:00*
- `[RELLENAR]` *Ej: Nadie sube avance sin actualizar Trello*
- `[RELLENAR]` *Ej: Decisiones de alcance se anotan en este doc o en AT01*

---

## Firmas / conformidad

| Nombre | Rol | Fecha | Conformidad |
|--------|-----|-------|-------------|
| `[RELLENAR]` | | | [ ] OK |

---

*Fin del Kickoff — siguiente: `docs/01-AT01/`*
