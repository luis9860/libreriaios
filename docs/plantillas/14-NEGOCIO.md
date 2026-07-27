# 14 — Negocio / dominio (plantilla completa con ejemplos)

---

## 1. Resumen — EJEMPLO COMPLETO

Biblioteca de **alquiler de libros físicos**. El usuario paga en la app con Yape (**alquiler + garantía**), se le asigna un **ejemplar UID**, el plazo corre **desde el pago**, recoge y devuelve **en el local**. Si devuelve en buen estado, recupera la garantía. Sin delivery en el MVP.

## 2. Actores

| Actor | Puede |
|-------|-------|
| Admin | CRUD títulos/ejemplares, ver todos los alquileres, confirmar recojo/devolución |
| Usuario (member) | Login, catálogo, pagar, ver sus alquileres, Watson |

## 3. Entidades — EJEMPLO

| Entidad | Campos clave |
|---------|--------------|
| Book | id, title, author, isbn, bookValue, rentalPrice, guaranteeAmount, rentalDays |
| Exemplar | uid, bookId, status (available/reserved/onLoan/retired) |
| Payment | id, rentalAmount, guaranteeAmount, total, yapePhone, verificationCode, status |
| Rental | id, userId, exemplarId, paymentId, startsAt, dueDate, status, returnedAt? |
| User | id, email, role (admin/member), facebookId? |

## 4. Reglas — EJEMPLO COMPLETO

1. `guaranteeAmount >= bookValue` al guardar título.  
2. Total Yape = rentalPrice + guaranteeAmount.  
3. Sin `payment.status == approved` no se crea Rental.  
4. Al aprobar pago: ejemplar `reserved`, `startsAt=now`, `dueDate=now+rentalDays`.  
5. No recojo no cancela el plazo: el tiempo sigue.  
6. Recojo: `onLoan`. Devolución OK: ejemplar `available`, garantía reembolsable; alquiler no se devuelve.  
7. Daño/pérdida: se retiene garantía.  
8. Un ejemplar no tiene dos rentals abiertos.

## 5. Ejemplo numérico

El Principito: valor 80, garantía 80, alquiler 10 → paga **90**. 3 UIDs. Paga → reserva UID-B → 14 días corren. Devuelve bien → negocio gana 10; usuario recupera 80.

## 6. Fuera de alcance

Delivery, venta, multas auto, multi-sucursal, Yape bancario certificado.
