# ÍNDICE MAESTRO — Un solo estándar (sin trabajar doble)

> Este archivo es la **única hoja de ruta**.  
> El video de YouTube y Cibertec se cubren con los mismos documentos de `trabajo/`.  
> **No crees otro informe paralelo** copiando lo mismo.

---

## Sobre ISO (importante)

| Norma | Para qué sirve | ¿Obliga el índice del video? |
|-------|----------------|------------------------------|
| **ISO/IEC/IEEE 12207** | Ciclo de vida del software (procesos) | No fija plantillas Word/MD |
| **ISO/IEC/IEEE 29148** | Cómo escribir requisitos (RF/RNF) | No impone el outline del video |
| **ISO/IEC 25010** | Calidad (usabilidad, seguridad…) → inspira RNF | No |

**Conclusión:** no hay una ISO que diga “haz exactamente esas 10 diapositivas”.  
Lo que haremos es **un solo paquete de docs** que cubre el video + Cibertec + práctica corporativa.

---

## Mapa: Video → Nuestro archivo (ya existe o se agrega)

| # | Sección del video | ¿Cubierto? | Archivo en `docs/trabajo/` |
|---|-------------------|------------|----------------------------|
| 1 | **Introducción** (objetivos + descripción) | Sí | `00-KICKOFF` + `04-OBJETIVOS-SMART` + `20-REQUISITOS-SISTEMA` |
| 2 | **Análisis de requisitos** (necesidades, RF, RNF, prioridad) | Sí | `01-PROBLEMATICA` + **`18-RF`** + **`19-RNF`** + `08-BACKLOG` (prioridad) |
| 3 | **Planificación** (tiempo, hitos, roles) | Sí | `00-KICKOFF` (roles) + `09-RELEASE-PLAN` + `07-VIABILIDAD` |
| 4 | **Diseño** (arquitectura, UI, datos/flujos) | Parcial → completo con nuevos | `13-ARQUITECTURA` + **`25-DISENO-UI`** + **`26-MODELO-DATOS`** + `21-CASOS-DE-USO` + `22-API` |
| 5 | **Desarrollo e implementación** (metodología, tools, código/pruebas) | Sí | `00` (Scrum) + `13` (stack) + **`27-DESARROLLO-IMPLEMENTACION`** |
| 6 | **Pruebas** | Sí | `11-PLAN-PRUEBAS` + curso 2424 |
| 7 | **Despliegue y mantenimiento** | Parcial → completo | `17-MANUAL-INSTALACION` + **`28-DESPLIEGUE-MANTENIMIENTO`** |
| 8 | **Gestión de riesgos** | Sí | `06-INTERESADOS-RIESGOS` |
| 9 | **Aspectos legales y éticos** | Faltaba → se agrega | **`29-LEGAL-ETICO`** |
| 10 | **Conclusión y futuros pasos** | Faltaba → se agrega | **`30-CONCLUSION-FUTURO`** |

### Extra Cibertec (también en el mismo paquete)

| Cibertec | Archivo |
|----------|---------|
| SEPTE, justificación, alcance, viabilidad | `02` `03` `05` `07` |
| Product Backlog / Sprint / CI | `08` `10` `12` |
| Watson / Facebook / REST / Core Data | en alcance + arquitectura + RF |
| Manual usuario | `16` |
| Glosario / trazabilidad | `23` `24` |

---

## Orden de llenado (una sola vez)

```text
00 Kickoff
01 → 08   AT01 / discovery
18, 19    RF y RNF          ★ (lo del video “Análisis de requisitos”)
20, 21, 23, 24
25, 26    Diseño UI + datos
13, 22, 14
09 → 12   AT02
27        Desarrollo/implementación (doc)
código…
11 + pruebas
28, 17    Despliegue
06        Riesgos (si no lo llenaste en AT01)
29        Legal/ético
15        Informes sprint (durante)
16        Manual usuario
30        Conclusión
```

---

## Regla anti-doble trabajo

1. Rellenas **solo** `docs/trabajo/`.  
2. Si el profe pide Word: **exportas** esos MD, no reescribes.  
3. Si el video pide “Introducción”: usas Kickoff + Objetivos + Requisitos sistema (no un cuarto documento nuevo con lo mismo).  
4. RF/RNF = archivos **18 y 19** (ya están).
