# 13 — Arquitectura (plantilla)

## 1. Vista de contexto

```text
[ App iOS ] --REST--> [ API Spring Boot ] --BD--> [ Database ]
     |                      ^
  Core Data              Pruebas Java
  Firebase / Facebook
  Watson
```

## 2. Componentes

| Componente | Responsabilidad |
|------------|-----------------|
| App iOS | UI, navegación, cache Core Data |
| API Spring Boot | Negocio, persistencia servidor |
| Firebase | `[RELLENAR]` |
| Watson | Asistente de ayuda |
| Trello | Gestión Scrum |

## 3. Módulos app iOS (MVC modular)

| Feature | Storyboard | Notas |
|---------|------------|-------|
| Auth | `[RELLENAR]` | |
| Catalog | `[RELLENAR]` | |
| Payments | `[RELLENAR]` | Yape |
| Rentals | `[RELLENAR]` | |
| Admin | `[RELLENAR]` | |
| Watson | `[RELLENAR]` | |

## 4. Principios

- Agregar módulos, no reescribir pantallas viejas  
- Pantallas hablan con **protocolos**, no con Core Data/URLSession directo  
- Un storyboard por feature  

## 5. Decisiones abiertas

| Decisión | Opciones | Estado |
|----------|----------|--------|
| `[RELLENAR]` | | Pendiente / Decidido |
