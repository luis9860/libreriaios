# 14 — Negocio / dominio (plantilla)

## 1. Resumen

`[RELLENAR]`

*Ej: Alquiler de libros físicos con ejemplar UID, pago Yape (alquiler+garantía), recojo en local.*

## 2. Actores

| Actor | Puede |
|-------|-------|
| Admin | `[RELLENAR]` |
| Usuario | `[RELLENAR]` |

## 3. Entidades

| Entidad | Campos clave |
|---------|--------------|
| Book (título) | bookValue, rentalPrice, guaranteeAmount |
| Exemplar | uid, bookId, estado |
| Payment | montos, celular, código verificación, estado |
| Rental | userId, exemplarId, paymentId, startsAt, dueDate, estado |
| User | email/Facebook, rol |

## 4. Reglas

1. `guaranteeAmount >= bookValue`  
2. Sin pago Yape aprobado → no hay alquiler  
3. Plazo corre desde el pago  
4. Recojo/devolución solo en biblioteca  
5. `[RELLENAR]`

## 5. Estados

**Ejemplar:** available → reserved → onLoan → available / retired  

**Rental:** reserved → onLoan → returned / overdue  

## 6. Fuera de alcance negocio

`[RELLENAR]` *delivery, multas auto, venta*
