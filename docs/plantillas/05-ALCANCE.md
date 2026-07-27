# 05 — Alcance (plantilla completa con ejemplos)

---

## 1. Descripción del producto — EJEMPLO COMPLETO

**LibreriaRent** es un sistema de alquiler de libros físicos compuesto por:

- App **iOS** (UIKit + Storyboard, MVC modular)  
- API **Java Spring Boot** (REST)  
- Persistencia local **Core Data** (cache)  
- **Firebase** + login **Facebook**  
- Asistente **Watson**  
- Gestión con **Scrum / Trello**  

El usuario reserva un **ejemplar (UID)**, paga **alquiler + garantía** con Yape (celular + código de verificación), recoge y devuelve **en la biblioteca**. El plazo corre **desde el pago**.

---

## 2. Incluido en el MVP (IN) — EJEMPLO COMPLETO

| ID | Funcionalidad | Actor |
|----|---------------|-------|
| IN-01 | Registro / login email-contraseña | Usuario |
| IN-02 | Login Facebook | Usuario |
| IN-03 | Catálogo de títulos (lista/collection) | Usuario |
| IN-04 | Detalle de título: precios, ejemplares disponibles | Usuario |
| IN-05 | Pago Yape (teléfono + código verificación); total = alquiler + garantía | Usuario |
| IN-06 | Crear alquiler solo si pago approved; ejemplar → reserved | Sistema |
| IN-07 | Confirmación de recojo (reserved → onLoan) | Admin / Usuario |
| IN-08 | Devolución; garantía reembolsable si buen estado | Admin / Usuario |
| IN-09 | CRUD títulos y ejemplares (UID) | Admin |
| IN-10 | Watson FAQ (garantía, Yape, recojo, plazos) | Usuario |
| IN-11 | Core Data cache de catálogo / sesión básica | App |
| IN-12 | Consumo REST de la API propia | App |

## 3. Excluido (OUT) — EJEMPLO COMPLETO

| ID | Qué no se hace | Motivo |
|----|----------------|--------|
| OUT-01 | Delivery a domicilio | Complejidad operativa |
| OUT-02 | Multas automáticas por atraso | Fase 2 |
| OUT-03 | Cola de reservas “avísame cuando vuelva” | Fase 2 |
| OUT-04 | Pasarela Yape bancaria certificada | MVP simulado / protocolo |
| OUT-05 | App Android | Fuera de Móviles iOS |
| OUT-06 | Varias sucursales | MVP un solo local |

## 4. Restricciones — EJEMPLO

- UIKit + Storyboard (no solo SwiftUI)  
- REST propio (no iTunes / no APIs de examen)  
- Core Data obligatorio  
- Facebook Auth (Unidad 4 Móviles)  
- Watson (Unidad 2 Integrador)  

## 5. Supuestos — EJEMPLO

- Hay un local físico para recojo/devolución  
- Existe al menos un usuario admin sembrado  
- El “código de verificación” Yape se valida en MVP con reglas locales/API propia  

## 6. Criterio de alcance completo — EJEMPLO

Demo end-to-end: login → ver libro → pagar Yape → ver alquiler reservado → marcar recojo → devolver → garantía pendiente de devolución; admin puede crear título+ejemplar.
