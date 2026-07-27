# 13 — Arquitectura (plantilla completa con ejemplos)

---

## 1. Contexto — EJEMPLO

```text
[Usuario iPhone]
      |
      v
[App iOS UIKit + Coordinators]
  - Core Data (cache)
  - Firebase / Facebook Auth
  - Watson SDK/Web
      |
      | HTTPS REST JSON
      v
[API Spring Boot]
  - Auth, Books, Exemplars, Payments, Rentals
      |
      v
[Base de datos]
```

Pruebas Java → golpean la API.  
Trello → gestión, no runtime.

## 2. Módulos iOS — EJEMPLO

| Feature | Storyboard | Contiene |
|---------|------------|----------|
| Auth | Auth.storyboard | Login email, Facebook |
| Catalog | Catalog.storyboard | Lista + detalle |
| Payments | Payments.storyboard | Yape teléfono + código |
| Rentals | Rentals.storyboard | Mis alquileres, recojo/devolución UI |
| Admin | Admin.storyboard | Alta libros/ejemplares |
| Watson | Watson.storyboard | Chat ayuda |
| Core | — | DI, Coordinators, Networking protocols |

## 3. API módulos — EJEMPLO

`/api/auth`, `/api/books`, `/api/exemplars`, `/api/payments/yape`, `/api/rentals`

## 4. Principios

1. Un storyboard por feature  
2. ViewControllers dependen de protocolos  
3. Agregar features sin reescribir Catalog  
4. Payment aprobado es prerrequisito de Rental  

## 5. Decisiones

| Decisión | Elegido | Motivo |
|----------|---------|--------|
| Backend | Spring Boot | Curso Pruebas + REST propio |
| Auth social | Facebook (U4) | Sílabo Móviles |
| Pago | Yape simulado UI real | MVP |
| IA | Watson Assistant | Integrador U2 |
