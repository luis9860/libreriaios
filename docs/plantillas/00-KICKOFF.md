# 00 — Kickoff (plantilla completa con ejemplos)

> **Cómo usar:** deja los `[RELLENAR]` solo donde van TUS datos (nombre, fechas, equipo, link Trello).  
> El resto ya trae **ejemplo completo** del proyecto librería — adáptalo o cópialo a `trabajo/`.

---

## 1. Datos generales

| Campo | Valor |
|-------|--------|
| Nombre del sistema | `[RELLENAR]` — *Ejemplo sugerido: **LibreriaRent*** |
| Código | `[RELLENAR]` — *Ejemplo: **LR-2026*** |
| Fecha kickoff | `[RELLENAR]` — *Ejemplo: 26/07/2026* |
| Ciclo / aula | `[RELLENAR]` — *Ejemplo: Sexto ciclo — aula XXX — 2026-2* |
| Coordinador | `[RELLENAR]` |
| Integrantes | `[RELLENAR]` — *Ejemplo: Luis Pérez, Ana Ruiz* |

### Cursos que abarca

- [x] Desarrollo de Aplicaciones Móviles II (4696)
- [x] Proyecto Integrador (2423)
- [x] Pruebas de Software (2424)

---

## 2. Problema (1 frase) — EJEMPLO COMPLETO

Los negocios de alquiler de libros físicos pierden control de **ejemplares**, **garantías** y **plazos** porque el proceso se lleva en papel, Excel o de forma informal, sin una app que una pago, inventario y recojo.

`[RELLENAR si quieres otra redacción]`

---

## 3. Solución (1 frase) — EJEMPLO COMPLETO

**LibreriaRent**: app iOS + API Spring Boot para alquilar **ejemplares con UID**, pagar con **Yape** (alquiler + garantía), **recoger y devolver en local**, con login email/Facebook, Firebase, Core Data y asistente **Watson**.

`[RELLENAR si quieres otra redacción]`

---

## 4. Roles Scrum

| Rol | Responsable | Ejemplo |
|-----|-------------|---------|
| Product Owner | `[RELLENAR]` | *Define prioridad: Auth → Catálogo → Yape → Alquiler* |
| Scrum Master | `[RELLENAR]` | *Cuida Trello, daily, impedimentos* |
| Development Team | `[RELLENAR]` | *API Java, iOS Swift, docs, pruebas* |

*Si eres solo: pon tu nombre en los 3.*

---

## 5. Trello — EJEMPLO DE COLUMNAS

| Campo | Valor |
|-------|--------|
| URL | `[RELLENAR]` *https://trello.com/b/xxxx/libreriarent* |
| Columnas | **Backlog** \| **Sprint actual** \| **En progreso** \| **En prueba** \| **Hecho** |
| Etiquetas | `iOS` `API` `Docs` `Watson` `Pruebas` `Bloqueado` |

---

## 6. Alcance MVP — EJEMPLO COMPLETO

### Incluye
- Títulos + ejemplares con **UID** y estados (available / reserved / onLoan / retired)
- Login **email/contraseña** + **Facebook**
- Pago **Yape**: celular + código de verificación; total = alquiler + garantía (`garantía >= valor libro`)
- Recojo y devolución **solo en biblioteca**
- El **plazo del alquiler corre desde el pago** (aunque aún no recoja)
- **REST** (Spring Boot) + **Core Data** + **Firebase**
- **Watson** Assistant (FAQ: precios, recojo, Yape)
- Roles **admin** y **usuario**

### No incluye
- Delivery a domicilio
- Venta definitiva de libros
- Multas automáticas
- Varias sucursales
- Integración bancaria real de Yape (MVP: flujo + validación; API real después)

---

## 7. Stack — EJEMPLO COMPLETO

| Capa | Tecnología |
|------|------------|
| App móvil | iOS, UIKit, Storyboard, MVC modular + Coordinators |
| Persistencia local | Core Data (cache) |
| Backend | Java Spring Boot (REST) + BD |
| Nube / auth | Firebase + Facebook Login |
| Gestión | Scrum + Trello |
| IA | IBM Watson Assistant |
| Pruebas | JUnit, Rest Assured, Cucumber; Appium opcional |

---

## 8. Próximos hitos — EJEMPLO

| Hito | Entregable | Fecha |
|------|------------|-------|
| AT01 | Problemática → Product Backlog | `[RELLENAR]` *ej. semana 5* |
| AT02 | Release Plan, pruebas, CI | `[RELLENAR]` *ej. semana 9* |
| Sprint 1–2 | API + Auth + Catálogo iOS | `[RELLENAR]` |
| EF | Sistema + manuales + sustentación | `[RELLENAR]` *sesión 13* |

---

## 9. Definition of Done — EJEMPLO

Una historia está **Hecho** cuando:
1. Código en GitHub / build OK  
2. Cumple criterios de aceptación  
3. Probada (manual o automatizada)  
4. Card en **Hecho** en Trello  
5. Documentado lo mínimo si aplica  

---

## 10. Acuerdos — EJEMPLOS (cámbialos)

- `[RELLENAR]` *Daily asíncrono por WhatsApp a las 9:00*  
- `[RELLENAR]` *Nadie marca Hecho sin actualizar Trello*  
- `[RELLENAR]` *Cambios de alcance se anotan en AT01 / este Kickoff*  
