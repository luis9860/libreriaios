# 20 — Requisitos del sistema / visión (plantilla completa con ejemplos)

> Documento tipo “System Requirements / Vision” corporativo: une negocio + RF/RNF + contexto.

---

## 1. Propósito

Definir el sistema **LibreriaRent** para que stakeholders (equipo, docentes, usuario) compartan la misma visión.

## 2. Alcance del sistema

Ver `05-ALCANCE.md`. Resumen: app iOS + API Spring Boot para alquiler de libros físicos con Yape, UID, recojo local.

## 3. Contexto (diagrama texto)

```text
Usuario/Admin → App iOS → API Spring Boot → BD
                 ↓
            Firebase / Facebook / Watson
```

## 4. Características principales (features)

| ID | Feature | Descripción | RF principales |
|----|---------|-------------|----------------|
| F1 | Identidad | Login email + Facebook | RF-01, RF-02 |
| F2 | Catálogo | Títulos y disponibilidad | RF-03..05 |
| F3 | Cobro | Yape alquiler+garantía | RF-06..08 |
| F4 | Préstamo | Reserva, plazo, recojo, devolución | RF-09..13 |
| F5 | Admin | Inventario UID | RF-14, RF-15 |
| F6 | Ayuda | Watson FAQ | RF-18 |

## 5. Supuestos y dependencias

- Local físico único  
- Keys de Facebook/Firebase/Watson disponibles para demo  
- Yape MVP simulado  

## 6. Documentos relacionados

| Doc | Contenido |
|-----|-----------|
| 14-NEGOCIO | Reglas de dominio |
| 18-RF | Requisitos funcionales |
| 19-RNF | No funcionales |
| 21-Casos de uso | Flujos |
| 08-Backlog | Historias Scrum |
| 13-Arquitectura | Diseño técnico |

## 7. Criterios de éxito del sistema

1. Demo E2E sin errores bloqueantes  
2. Cumple mínimos Móviles (REST+Core Data+Facebook+Firebase)  
3. Watson integrado  
4. Pruebas API documentadas  
