# 11 — Plan de pruebas (plantilla completa con ejemplos)

---

## 1. Objetivo — EJEMPLO

Asegurar que LibreriaRent cumple las reglas de negocio críticas: auth, catálogo, pago Yape → reserva UID, recojo/devolución y validación garantía ≥ valor, mediante pruebas unitarias, de API y checklist funcional iOS.

## 2. Alcance

| Incluye | Excluye |
|---------|---------|
| API REST (auth, books, exemplars, payments, rentals) | Integración bancaria real Yape |
| Flujos manuales iOS del MVP | Performance masivo inicial |
| Casos Gherkin de aceptación | Seguridad avanzada pentest |

## 3. Tipos de prueba — EJEMPLO

| Tipo | Herramienta | Momento |
|------|-------------|---------|
| Unitarias dominio/API | JUnit + Mockito | Cada sprint |
| API | Rest Assured / Cucumber+Serenity | AT02+ |
| Funcional móvil | Checklist + Appium (si hay tiempo) | Pre-EF |
| Performance | JMeter smoke GET /books | Opcional |
| Aceptación | Demo + PO | Fin de sprint |

## 4. Casos de prueba — EJEMPLO COMPLETO

| ID | Escenario | Resultado esperado | Pri |
|----|-----------|--------------------|-----|
| CP01 | Login email válido | 200 + token/sesión | Alta |
| CP02 | Login email inválido | 401/error claro | Alta |
| CP03 | GET /books con data | Lista con título y disponibles | Alta |
| CP04 | Crear Book con guarantee < bookValue | 400 validación | Alta |
| CP05 | Pago Yape OK → rental + exemplar reserved | Estados correctos; dueDate set | Alta |
| CP06 | Pago Yape fail → no rental | Ejemplar sigue available | Alta |
| CP07 | Recojo reserved → onLoan | Estado actualizado | Alta |
| CP08 | Devolución buen estado | available + guarantee refundable | Alta |
| CP09 | Facebook login (happy path) | Sesión member | Media |
| CP10 | Watson FAQ garantía | Respuesta coherente | Media |

## 5. Entrada / salida — EJEMPLO

- **Entrada:** build desplegable API; datos seed; casos escritos.  
- **Salida:** CP Alta en verde; 0 bugs bloqueantes; evidencias (capturas/logs) en carpeta pruebas.

## 6. Ambientes — EJEMPLO

| Ambiente | URL |
|----------|-----|
| Dev local | `http://localhost:8080` |
| Test | `[RELLENAR]` |

## 7. Riesgos de prueba — EJEMPLO

Simulador iOS ≠ dispositivo; Facebook necesita keys; Yape es simulado (documentar limitación).
