# 26 — Modelo de datos y flujos — plantilla con ejemplos

> Cubre el video: **Modelado de datos y flujos de proceso**.

## 1. Entidades (lógico) — EJEMPLO

| Entidad | Atributos clave | PK |
|---------|-----------------|-----|
| User | email, passwordHash?, facebookId?, role | id |
| Book | title, author, isbn, bookValue, rentalPrice, guaranteeAmount, rentalDays | id |
| Exemplar | uid, status, bookId | id / uid |
| Payment | rentalAmount, guaranteeAmount, total, yapePhone, verificationCode, status | id |
| Rental | userId, exemplarId, paymentId, startsAt, dueDate, status, returnedAt | id |

## 2. Relaciones — EJEMPLO

```text
User 1──* Rental
Book 1──* Exemplar
Exemplar 1──* Rental (abierto máx. 1)
Rental 1──1 Payment
```

## 3. Diccionario (muestra)

| Tabla.Campo | Tipo | Descripción |
|-------------|------|-------------|
| Exemplar.uid | string/UUID | Identificador físico único |
| Book.guaranteeAmount | decimal | Debe ser >= bookValue |
| Rental.startsAt | datetime | Inicio al pagar |
| Payment.status | enum | pending/approved/failed |

## 4. Flujo de proceso alquiler — EJEMPLO

```text
Elegir título → Ver total → Yape → ¿approved?
   no → fin error
   sí → reservar UID → plazo corre → recojo → uso → devolución
         → buen estado: garantía reembolsable
         → daño: garantía retenida
```

## 5. Diagrama ER / BPMN

`[RELLENAR]` *Exporta desde Draw.io y pega aquí o adjunta PNG*

## 6. Core Data (app)

Entidades espejo de Book/Exemplar/Rental para cache — ver arquitectura.
