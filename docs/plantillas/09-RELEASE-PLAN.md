# 09 — Release Plan (plantilla completa con ejemplos)

---

## 1. Objetivo del release — EJEMPLO

Entregar el **MVP LibreriaRent** demostrable: login, catálogo, pago Yape, alquiler con UID, recojo/devolución, admin básico, Watson FAQ, API REST + app iOS con Core Data.

---

## 2. Releases — EJEMPLO

| Release | Contenido | Fecha |
|---------|-----------|-------|
| **R0 MVP** | US01–US10, US13; API + iOS; docs AT01/AT02 | `[RELLENAR]` antes EF |
| **R1** | Watson pulido (US11), mejoras UX, PageView onboarding | `[RELLENAR]` |
| **R2** | Pruebas automatizadas amplias (US12+), CI verde | `[RELLENAR]` |

---

## 3. Mapa de sprints — EJEMPLO COMPLETO

| Sprint | Sprint Goal | Historias | Incremento |
|--------|-------------|-----------|------------|
| **1** | API viva + Auth | US01, US09 base users, health, CRUD Book inicial | API login + books GET/POST |
| **2** | Catálogo iOS + Core Data | US03, US04, cache | App lista libros offline-ish |
| **3** | Yape + alquiler | US05, US06, US13 | Pago y reserva UID |
| **4** | Recojo/devolución + admin ejemplares + Facebook | US02, US07, US08, US10 | Flujo completo local |
| **5** | Watson + pruebas + pulido | US11, US12, DoD | Demo EF |

`[RELLENAR]` *Ajusta número de sprints a tu calendario real.*

---

## 4. Dependencias — EJEMPLO

1. Contrato API (endpoints) antes de pantallas de pago.  
2. Modelo Exemplar UID antes de Rentals.  
3. Keys Facebook/Firebase/Watson en paralelo sin bloquear email login.  

## 5. Criterio release listo — EJEMPLO

Checklist demo + plan de pruebas ejecutado en críticos + manuales borrador + Trello al día.
