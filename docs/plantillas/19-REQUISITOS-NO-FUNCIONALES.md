# 19 — Requisitos no funcionales (RNF) — plantilla completa con ejemplos

> Los RNF describen **cómo** debe ser el sistema (calidad), no el “qué funcional”.

---

## 1. Categorías usadas

Usabilidad, Rendimiento, Seguridad, Disponibilidad, Compatibilidad, Mantenibilidad, Portabilidad, Legales/cumplimiento, Operación.

---

## 2. Lista RNF — EJEMPLO COMPLETO

| ID | Categoría | Requisito | Métrica / verificación | Prioridad |
|----|-----------|-----------|------------------------|-----------|
| RNF-01 | Usabilidad | Un usuario nuevo completa alquiler (catálogo→pago) en ≤ 5 minutos en demo guiada | Cronómetro en prueba de usabilidad | Must |
| RNF-02 | Usabilidad | Pantallas con textos en español claros (ejemplar, garantía, Yape) | Revisión PO + checklist | Must |
| RNF-03 | Rendimiento | GET /api/books responde p95 &lt; 2s con ≤ 100 títulos en ambiente local | Medición Postman/JMeter smoke | Should |
| RNF-04 | Rendimiento | Scroll del catálogo iOS sin freeze perceptible en simulador | Prueba manual | Should |
| RNF-05 | Seguridad | Contraseñas no se almacenan en texto plano (hash en API / Keychain en app según diseño) | Revisión código | Must |
| RNF-06 | Seguridad | Comunicación app-API por HTTP local en dev; HTTPS en despliegue | Config ambientes | Should |
| RNF-07 | Seguridad | Celular Yape se muestra enmascarado en historiales | UI/API review | Should |
| RNF-08 | Disponibilidad | API disponible durante la demo EF (plan B: laptop local) | Ensayo previo | Must |
| RNF-09 | Compatibilidad | App corre en iOS `[RELLENAR]`+ (simulador Xcode del lab) | Build + run | Must |
| RNF-10 | Compatibilidad | API documentada con endpoints JSON REST | README / OpenAPI | Must |
| RNF-11 | Mantenibilidad | App modular por features (un storyboard por módulo) | Revisión arquitectura | Must |
| RNF-12 | Mantenibilidad | Código API con capas controller-service-repository | Revisión | Should |
| RNF-13 | Escalabilidad | Diseño permite agregar medios de pago sin reescribir pantallas de catálogo (protocolos) | Diseño DI | Should |
| RNF-14 | Portabilidad | Backend independiente de iOS (cualquier cliente REST futuro) | Contrato API | Should |
| RNF-15 | Legales | Aviso de privacidad básico (email, Facebook, celular Yape) | Pantalla/texto legal | Should |
| RNF-16 | Operación | Seed de datos demo (admin, socio, ≥3 libros) para sustentación | Script seed | Must |
| RNF-17 | Calidad | Plan de pruebas con casos Alta en verde antes de EF | Informe pruebas | Must |
| RNF-18 | Integración | Facebook, Firebase y Watson configurables por archivos/keys sin hardcode secretos en Git | .gitignore + env | Must |
| RNF-19 | `[RELLENAR]` | | | |

---

## 3. Restricciones de plataforma (curso)

| RNF / restricción | Origen |
|-------------------|--------|
| UIKit + Storyboard | Móviles II |
| Core Data | Móviles II / U2 |
| REST propio | Móviles II proyecto |
| Facebook Auth | Móviles II U4 |
| Watson | Integrador U2 |
| Pruebas Java sobre API | Pruebas 2424 |

## 4. No aplicables / diferidos

- Alta disponibilidad multi-región  
- Certificaciones PCI / Yape oficial  
- Soporte Android  

## 5. Historial

| Versión | Fecha | Autor | Cambio |
|---------|-------|-------|--------|
| 0.1 | `[RELLENAR]` | `[RELLENAR]` | Borrador |
