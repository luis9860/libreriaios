# 18 — Requisitos funcionales (RF) — plantilla completa con ejemplos

> Cada RF debe ser: identificable, claro, verificable. Prioridad: Must / Should / Could / Won’t (MoSCoW).

---

## 1. Introducción — EJEMPLO

Este documento describe **qué debe hacer** el sistema LibreriaRent (comportamiento observable), sin detallar aún la tecnología interna.

## 2. Actores

| Actor | Descripción |
|-------|-------------|
| Usuario | Persona registrada (rol member) que alquila libros |
| Administrador | Personal de la biblioteca (rol admin) |
| Sistema | Automatismos (plazos, validaciones, asignación UID) |
| Watson | Asistente virtual de ayuda (integración) |
| Pasarela Yape (simulada) | Proceso de pago móvil en MVP |

---

## 3. Lista de requisitos funcionales — EJEMPLO COMPLETO

| ID | Requisito | Actor | Prioridad | Criterio de aceptación (resumen) | Huella (US) |
|----|-----------|-------|-----------|----------------------------------|-------------|
| RF-01 | El sistema debe permitir registro e inicio de sesión con email y contraseña | Usuario | Must | Credenciales válidas → sesión; inválidas → error | US01 |
| RF-02 | El sistema debe permitir inicio de sesión con Facebook | Usuario | Must | Autorización OK → sesión member | US02 |
| RF-03 | El sistema debe mostrar el catálogo de títulos disponibles | Usuario | Must | Lista con título, autor, cantidad disponible | US03 |
| RF-04 | El sistema debe mostrar detalle de un título (valor, alquiler, garantía, plazo) | Usuario | Must | Montos visibles; garantía ≥ valor en datos válidos | US04 |
| RF-05 | El sistema debe listar ejemplares disponibles de un título (por UID) | Usuario/Admin | Must | Solo status available; UID visible para admin | US04 |
| RF-06 | El sistema debe calcular total = alquiler + garantía | Sistema | Must | Total correcto en pantalla de pago | US06 |
| RF-07 | El sistema debe permitir pagar con Yape ingresando celular y código de verificación | Usuario | Must | Campos obligatorios; formato celular 9 dígitos | US05 |
| RF-08 | Solo si el pago está approved, el sistema debe crear el alquiler y reservar un ejemplar UID | Sistema | Must | Sin approved → no rental; con approved → reserved + startsAt/dueDate | US05-06 |
| RF-09 | El sistema debe iniciar el plazo de alquiler en el momento del pago aprobado | Sistema | Must | dueDate = startsAt + rentalDays aunque no haya recojo | US06 |
| RF-10 | El sistema debe permitir confirmar recojo (reserved → onLoan) | Admin/Usuario | Must | Solo desde reserved | US07 |
| RF-11 | El sistema debe permitir registrar devolución | Admin | Must | onLoan → returned; ejemplar available si buen estado | US08 |
| RF-12 | Si devolución en buen estado, el sistema debe marcar garantía como reembolsable | Sistema | Must | Alquiler no se reembolsa | US08 |
| RF-13 | Si pérdida/daño, el sistema debe retener la garantía | Admin/Sistema | Must | Estado de payment/guarantee = retained | US08 |
| RF-14 | El admin debe poder crear/editar títulos validando guaranteeAmount ≥ bookValue | Admin | Must | Si no cumple → rechazo | US09 |
| RF-15 | El admin debe poder crear ejemplares con UID único | Admin | Must | UID no duplicado; status available | US10 |
| RF-16 | El usuario debe poder ver solo sus alquileres | Usuario | Must | No ve rentals de otros | US13 |
| RF-17 | El admin debe poder ver todos los alquileres | Admin | Must | Listado global | — |
| RF-18 | El sistema debe exponer un asistente Watson para FAQs del negocio | Usuario | Should | Responde garantía, recojo, Yape, plazos | US11 |
| RF-19 | El sistema debe persistir catálogo en Core Data como cache local | App | Must | Tras sync REST, datos locales disponibles | — |
| RF-20 | El sistema debe consumir la API REST propia (no APIs de examen/iTunes) | App | Must | Base URL configurable a Spring Boot | — |
| RF-21 | `[RELLENAR]` requisito extra del equipo | | Could | | |

---

## 4. Reglas de negocio asociadas (trazabilidad)

| Regla | RFs |
|-------|-----|
| guarantee ≥ bookValue | RF-14, RF-04 |
| Pago previo a alquiler | RF-08 |
| Plazo desde pago | RF-09 |
| Solo recojo local | RF-10, RF-11 |
| UID por ejemplar | RF-05, RF-08, RF-15 |

## 5. Fuera de requisitos funcionales (MVP)

Delivery, multas automáticas, venta de libros, multi-sucursal, Yape bancario certificado.

## 6. Historial

| Versión | Fecha | Autor | Cambio |
|---------|-------|-------|--------|
| 0.1 | `[RELLENAR]` | `[RELLENAR]` | Borrador inicial |
