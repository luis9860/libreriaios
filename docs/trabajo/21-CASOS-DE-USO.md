# 21 — Casos de uso (plantilla completa con ejemplos)

> Formato breve corporativo. Prioriza los flujos del MVP.

---

## Actores

Usuario, Administrador, Sistema.

---

## CU-01 Iniciar sesión con email — EJEMPLO

| Campo | Contenido |
|-------|-----------|
| Actor | Usuario |
| Precondición | Usuario registrado |
| Flujo principal | 1. Abre app 2. Ingresa email/clave 3. Confirma 4. Sistema valida 5. Entra a catálogo |
| Alternativo | 4a. Credenciales inválidas → mensaje de error |
| Postcondición | Sesión activa rol member o admin |
| RF | RF-01 |

## CU-02 Iniciar sesión con Facebook — EJEMPLO

| Campo | Contenido |
|-------|-----------|
| Actor | Usuario |
| Flujo | 1. Botón Facebook 2. Autoriza 3. Sistema crea/vincula cuenta 4. Entra |
| RF | RF-02 |

## CU-03 Consultar catálogo — EJEMPLO

| Campo | Contenido |
|-------|-----------|
| Actor | Usuario |
| Flujo | 1. Home catálogo 2. Sistema obtiene REST (+ cache Core Data) 3. Muestra lista |
| RF | RF-03, RF-19, RF-20 |

## CU-04 Alquilar con Yape — EJEMPLO COMPLETO

| Campo | Contenido |
|-------|-----------|
| Actor | Usuario |
| Precondición | Sesión activa; título con ejemplar available |
| Flujo principal | 1. Detalle título 2. Ver montos 3. Pagar Yape (celular+código) 4. Sistema aprueba pago 5. Reserva UID 6. Muestra rental reserved y dueDate |
| Alternativo | 4a. Pago falla → no reserva |
| Postcondición | Payment approved; Exemplar reserved; Rental creado; plazo corriendo |
| RF | RF-06..09 |

## CU-05 Recoger ejemplar — EJEMPLO

| Campo | Contenido |
|-------|-----------|
| Actor | Admin (o Usuario según política) |
| Precondición | Rental reserved |
| Flujo | Confirmar recojo → onLoan |
| RF | RF-10 |

## CU-06 Devolver ejemplar — EJEMPLO

| Campo | Contenido |
|-------|-----------|
| Actor | Admin |
| Flujo | Registrar devolución + estado físico → available + garantía reembolsable o retenida |
| RF | RF-11..13 |

## CU-07 Administrar inventario — EJEMPLO

| Campo | Contenido |
|-------|-----------|
| Actor | Admin |
| Flujo | Crear título (validar garantía) → crear ejemplares UID |
| RF | RF-14, RF-15 |

## CU-08 Consultar Watson — EJEMPLO

| Campo | Contenido |
|-------|-----------|
| Actor | Usuario |
| Flujo | Abre asistente → pregunta FAQ → respuesta |
| RF | RF-18 |

## CU-09 `[RELLENAR]`

---

## Diagrama de casos de uso (texto)

```text
Usuario --- CU01, CU02, CU03, CU04, CU08
Admin   --- CU05, CU06, CU07 (+ CU03)
Sistema --- (incluye validaciones en CU04)
```
