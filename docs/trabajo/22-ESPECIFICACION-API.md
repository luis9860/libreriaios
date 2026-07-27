# 22 — Especificación de interfaces / API (plantilla completa con ejemplos)

> Contrato REST que consumirá la app iOS. Ajusta paths cuando implementes.

---

## 1. General

| Campo | Valor |
|-------|--------|
| Base URL dev | `http://localhost:8080/api` |
| Formato | JSON |
| Auth | Bearer token / sesión `[RELLENAR mecanismo final]` |

## 2. Endpoints — EJEMPLO

### Auth

| Método | Path | Descripción | Body ejemplo |
|--------|------|-------------|--------------|
| POST | `/auth/register` | Registro email | `{ "email","password","name" }` |
| POST | `/auth/login` | Login email | `{ "email","password" }` |
| POST | `/auth/facebook` | Login Facebook | `{ "accessToken" }` |

### Books

| Método | Path | Descripción |
|--------|------|-------------|
| GET | `/books` | Listar títulos |
| GET | `/books/{id}` | Detalle + disponibilidad |
| POST | `/books` | Crear (admin) |
| PUT | `/books/{id}` | Actualizar (admin) |

**Ejemplo respuesta GET /books**

```json
[
  {
    "id": "uuid",
    "title": "El Principito",
    "author": "Antoine de Saint-Exupéry",
    "bookValue": 80.0,
    "rentalPrice": 10.0,
    "guaranteeAmount": 80.0,
    "rentalDays": 14,
    "availableCount": 2
  }
]
```

### Exemplars

| Método | Path | Descripción |
|--------|------|-------------|
| GET | `/books/{id}/exemplars` | Listar UIDs |
| POST | `/exemplars` | Crear UID (admin) |

### Payments / Rentals

| Método | Path | Descripción |
|--------|------|-------------|
| POST | `/payments/yape` | `{ phone, verificationCode, bookId, amount }` |
| POST | `/rentals` | Crear tras pago (o lo hace el payment) |
| GET | `/rentals/me` | Mis alquileres |
| GET | `/rentals` | Todos (admin) |
| POST | `/rentals/{id}/pickup` | Confirmar recojo |
| POST | `/rentals/{id}/return` | Devolución `{ condition: "good"|"damaged" }` |

## 3. Códigos HTTP — EJEMPLO

| Código | Uso |
|--------|-----|
| 200/201 | OK / creado |
| 400 | Validación (garantía &lt; valor, Yape incompleto) |
| 401 | No autenticado |
| 403 | No autorizado (no admin) |
| 404 | No encontrado |
| 409 | Conflicto (sin ejemplares) |

## 4. Errores — EJEMPLO

```json
{ "code": "GUARANTEE_TOO_LOW", "message": "La garantía debe ser >= valor del libro" }
```

## 5. Historial

| Versión | Fecha | Notas |
|---------|-------|-------|
| 0.1 | `[RELLENAR]` | Borrador contrato |
