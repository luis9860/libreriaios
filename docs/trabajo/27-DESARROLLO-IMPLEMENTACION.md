# 27 — Desarrollo e implementación — plantilla con ejemplos

> Cubre el video: metodología, herramientas, codificación y pruebas.

## 1. Metodología — EJEMPLO

**Scrum** (Proyecto Integrador): sprints, Product Backlog, Sprint Backlog, Daily, Demo, Retro. Tablero **Trello**.

## 2. Herramientas y tecnologías — EJEMPLO

| Área | Herramienta |
|------|-------------|
| App | Xcode, Swift, UIKit, Storyboard, Core Data |
| API | IntelliJ/VS Code, Java, Spring Boot |
| Auth/Nube | Firebase, Facebook SDK |
| IA | IBM Watson Assistant |
| Control versiones | Git + GitHub |
| Pruebas | JUnit, Rest Assured, Postman; Appium opcional |
| Docs | Markdown → Word al entregar |

## 3. Proceso de codificación — EJEMPLO

1. Tomar card del Sprint Backlog  
2. Rama `feature/...`  
3. Implementar + prueba mínima  
4. PR / merge a main  
5. Actualizar Trello → Hecho  

Estándares: MVC modular iOS; capas API controller-service-repository; sin secretos en Git.

## 4. Pruebas en desarrollo

Unitarias en API cada historia Must; checklist manual iOS; ver `11-PLAN-PRUEBAS`.

## 5. Ambientes

| Ambiente | Uso |
|----------|-----|
| Local | Dev diario |
| Demo | Sustentación EF |

`[RELLENAR]` URLs reales cuando existan.
