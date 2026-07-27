# 08 — Product Backlog (plantilla completa con ejemplos)

> Prioridad: Must / Should / Could. Est.: S=1, M=3, L=5 (o planning poker).

---

## Épicas

| ID | Épica | Descripción |
|----|--------|-------------|
| E1 | Autenticación | Email + Facebook + sesión |
| E2 | Catálogo / ejemplares | Títulos, UID, disponibilidad |
| E3 | Pagos Yape | UI + PaymentService |
| E4 | Alquileres | Reserva, recojo, devolución, plazos |
| E5 | Administración | CRUD libros/ejemplares |
| E6 | Watson | FAQ asistente |
| E7 | Calidad | Pruebas API / plan |

---

## Historias — EJEMPLO COMPLETO

| ID | Historia (Como… quiero… para…) | Pri | Est | Épica | Criterios de aceptación (ejemplo) |
|----|--------------------------------|-----|-----|-------|-----------------------------------|
| US01 | Como usuario quiero registrarme e iniciar sesión con email/contraseña para acceder | Must | M | E1 | Given datos válidos When login Then sesión activa; Given contraseña mala Then error |
| US02 | Como usuario quiero iniciar sesión con Facebook para entrar sin formulario largo | Must | M | E1 | Given Facebook OK When autorizo Then entro como member |
| US03 | Como usuario quiero ver el catálogo en lista/colección para elegir un título | Must | M | E2 | Given API con libros When abro catálogo Then veo título, autor, disponibles |
| US04 | Como usuario quiero ver detalle (precio alquiler, garantía, valor) y UIDs disponibles | Must | M | E2 | Given título con 2 available When abro detalle Then veo montos y cantidad disponible |
| US05 | Como usuario quiero pagar con Yape (celular + código verificación) el total alquiler+garantía | Must | L | E3 | Given formulario completo When pago OK Then payment approved; si falla Then no hay rental |
| US06 | Como usuario quiero que al pagar se reserve un ejemplar UID y empiece el plazo | Must | L | E4 | Given pago approved When confirma Then exemplar reserved y dueDate = now+N días |
| US07 | Como admin/usuario quiero registrar recojo para pasar a onLoan | Must | S | E4 | Given reserved When confirmo recojo Then onLoan |
| US08 | Como admin quiero registrar devolución en buen estado y marcar garantía reembolsable | Must | M | E4 | Given onLoan When devuelvo OK Then available + guarantee refundable |
| US09 | Como admin quiero crear título con bookValue, rentalPrice, guaranteeAmount (≥ valor) | Must | M | E5 | Given garantía < valor When guardo Then error validación |
| US10 | Como admin quiero crear ejemplares con UID para un título | Must | S | E5 | Given título When creo ejemplar Then uid único y available |
| US11 | Como usuario quiero preguntar a Watson por garantía/recojo/Yape | Should | M | E6 | Given pregunta FAQ When envío Then respuesta configurada |
| US12 | Como equipo quiero pruebas API de login y books | Should | M | E7 | Given API up When Rest Assured Then 200 y contrato OK |
| US13 | Como usuario quiero ver mis alquileres y si estoy atrasado | Must | M | E4 | Given tengo rental When abro Mis alquileres Then veo estado y dueDate |
| US14 | `[RELLENAR]` historia extra del equipo | Could | | | |

---

## Definition of Ready — EJEMPLO

Clara, con criterios de aceptación, estimada, prioridad Must/Should, sin dependencia bloqueante sin plan.

## Definition of Done — EJEMPLO

Código en `main` o PR merge, build OK, criterios OK, probada, card en Hecho, demoable.
