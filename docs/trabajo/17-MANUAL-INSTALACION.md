# 17 — Manual de instalación (plantilla completa con ejemplos)

---

## 1. Componentes — EJEMPLO

| Componente | Tecnología | Versión objetivo |
|------------|------------|------------------|
| API | Spring Boot | 3.x / JDK 17 |
| App | Xcode / iOS | `[RELLENAR]` Xcode 15+ |
| BD | PostgreSQL o H2 dev | `[RELLENAR]` |

## 2. Prerrequisitos — EJEMPLO

- Git, JDK 17, Maven  
- Xcode + simulador  
- Cuentas: Firebase, Meta Facebook App, IBM Watson  
- Clonar: `https://github.com/luis9860/libreriaios.git`

## 3. API — EJEMPLO (cuando exista carpeta)

```bash
cd api
./mvnw spring-boot:run
# Health: http://localhost:8080/actuator/health  o /api/health
```

Variables: `[RELLENAR]` `DB_URL`, `JWT_SECRET`, etc.

## 4. App iOS — EJEMPLO

1. Abrir `LibreriaIOS.xcodeproj`  
2. Configurar Base URL (`http://localhost:8080` en simulador; IP LAN en device)  
3. Añadir `GoogleService-Info.plist` y Facebook keys en Info.plist  
4. Product → Run  

## 5. Smoke — EJEMPLO

| Paso | Esperado |
|------|----------|
| API up | 200 health |
| Login seed | Token OK |
| GET books | JSON lista |
| App catálogo | Muestra libros |

## 6. Problemas comunes — EJEMPLO

| Problema | Solución |
|----------|----------|
| App no alcanza localhost en iPhone físico | Usar IP de la PC en la misma WiFi |
| Facebook no abre | Revisar URL schemes y App ID |
| Cors / ATS | Ajustar Info.plist ATS excepciones solo en debug |
