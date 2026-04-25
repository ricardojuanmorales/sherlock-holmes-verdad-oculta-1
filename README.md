# Sherlock Holmes y la Verdad Oculta — V1.0

> *"No basta con tener una idea brillante. Hay que poder demostrarla, sostenerla éticamente y dejar evidencia clara de cómo se llegó a ella."*

---

## Descripción del proyecto

**Sherlock Holmes y la Verdad Oculta V1.0** es un juego de investigación transdisciplinario con ambiente lúdico-virtual, diseñado como una experiencia de aprendizaje, creación y competencia ética para equipos universitarios. Equipos de 5 *Junior DevOps* deben colaborar para resolver casos de complejidad ascendente, verificar evidencias, construir prototipos funcionales y demostrar pensamiento investigativo riguroso.

En el trasfondo narrativo, **Sherlock Holmes** preparó un sistema de retos para encontrar a la próxima generación capaz de continuar su legado, con el apoyo ambiguo y útil de **Dr. Watson GPT 2025** — un asistente de IA que orienta, pero nunca reemplaza el juicio humano.

---

## Inicio rápido

```bash
# 1. Descarga o clona el repositorio
git clone https://github.com/tu-org/sherlock-mvp

# 2. Abre el MVP directamente en el navegador
open index.html
# — También funciona con doble clic o arrastrando el archivo al navegador
# — No requiere servidor, npm, ni conexión a internet
```

El MVP funciona **completamente offline**. Todos los datos, estilos y lógica están embebidos en un único archivo HTML de ~185KB.

---

## Estructura del repositorio

```
sherlock-mvp/
├── README.md                           ← Este documento
├── index.html                          ← MVP completo · single-file · sin dependencias
│
├── docs/
│   ├── 01_Base_Estrategica.md          ← Mapa sistémico, pilares y RoadMap evolutivo
│   ├── 02_RuleBook_Maestro.md          ← Reglas oficiales, mandamientos y evaluación
│   ├── 03_Norma_Multimodal_Obsidian.md ← Interoperabilidad, nomenclatura y Obsidian
│   ├── 04_Estructura_10_Casos.md       ← Los 10 casos con premisa, competencias y productos
│   ├── 05_Repositorio_Badges.md        ← 35 badges con criterios y evidencia mínima
│   └── 06_Registro_Normalizacion.md    ← Historial de normalización terminológica V1.1
│
└── templates/
    ├── Plantilla_Expediente_V1_1.md    ← Fuente principal de verdad documental del caso
    ├── Plantilla_Evidencia_V1_1.md     ← Ficha trazable por evidencia individual
    └── Plantilla_Bitacora_V1_0.md      ← Memoria operativa de cada sesión de trabajo
```

---

## El MVP — `index.html`

### Tecnología

| Atributo | Detalle |
|---|---|
| Formato | HTML5 + CSS3 + JavaScript ES6 — monolito autocontenido |
| Dependencias externas | Solo Google Fonts (Fraunces · Instrument Sans · JetBrains Mono) |
| Funcionamiento offline | Sí — todos los datos están embebidos como objetos JS |
| Tamaño | ~185KB sin comprimir |
| Compatibilidad | Cualquier navegador moderno: Chrome, Firefox, Safari, Edge |
| Servidor requerido | No |

### Funciones del MVP

El MVP tiene 6 pestañas de navegación, todas interactivas:

#### 🏠 Panel principal
Vista de entrada con frase del universo narrativo, acceso rápido a las 6 secciones (tarjetas clickeables) y los 10 pilares del sistema con descripción completa.

#### 📂 Casos
10 tarjetas de caso, todas clickeables sin importar su estado. Al tocar cualquier tarjeta se abre un **modal de detalle** con: premisa completa, pregunta rectora destacada, competencias del investigador requeridas, tipos de evidencia esperada, productos mínimos esperados, nota de dificultad y badges aplicables (cada uno abre directamente el modal del badge correspondiente).

El **Caso 1** incluye además un bloque de **nivel simulado** con el Equipo Clio activo: hipótesis con estados (fuerte / abierta / débil), evidencias capturadas, badges ganados y en progreso, y próximo paso programado.

#### 👥 Equipos
Tablero de gestión de los 5 equipos del piloto con estadísticas globales (evidencias totales, badges otorgados). Las tarjetas de equipo muestran acento cromático por facultad, barra de progreso y mini-avatares. Al tocar una tarjeta se abre la **vista individual** con: encabezado oscuro con código y mentor, 4 métricas destacadas, tarjetas de los 5 miembros con contribución concreta, hipótesis activas, badges, última bitácora de sesión, log de IA y línea de evidencias con estado.

#### 🏅 Badges
35 insignias en 10 familias, filtrables. Al tocar cualquier badge se abre un **modal de detalle** con: criterio oficial de otorgación, pasos numerados para ganarlo, evidencia mínima requerida por escrito, y equipos del piloto que ya lo han obtenido.

#### 📖 Glosario
Más de 50 términos del vocabulario oficial con buscador en tiempo real. Cada término es un acordeón expandible con definición breve, definición operativa y ejemplo de uso en contexto.

#### 📋 Plantillas
Las 3 plantillas oficiales con campos documentados y botón **Vista previa** que abre un **modal interactivo** con sidebar de secciones navegables y contenido con datos simulados reales: YAML completo, tablas, checklists y bloques de evidencia ya completados para ilustrar el uso correcto.

---

## Los 5 equipos del piloto V1.0

| Equipo | Código | Facultad | Caso activo | Avance |
|---|---|---|---|---|
| Equipo Clio | EQ-HUM-01 | Humanidades · Historia | Caso 1 — El Manuscrito Extraviado | 78% |
| Equipo Hermes | EQ-COM-02 | Comunicación · Periodismo | Caso 2 — La Portada Viral | 62% |
| Equipo Darwin | EQ-BIO-03 | Ciencias Naturales · Biología | Caso 3 — El Jardín de las Especies | 45% |
| Equipo Freud | EQ-PSI-04 | Ciencias Sociales · Psicología | Caso 4 — La Conducta Invisible | 33% |
| Equipo Fibonacci | EQ-ADM-05 | Administración · Contabilidad | Caso 5 — El Decanato Fantasma | 19% |

Cada equipo tiene 5 integrantes con roles diferenciados: Arquitectura, Interfaz/UX, Lógica/Análisis, Testing y Quinto Elemento.

---

## Los 10 casos

| Niv. | Caso | Disciplina | Complejidad |
|---|---|---|---|
| 1 ✓ | El Manuscrito Extraviado | Humanidades / Historia | ●○○○○○○○○○ |
| 2 | La Portada Viral | Comunicación / Periodismo | ●●○○○○○○○○ |
| 3 | El Jardín de las Especies Imposibles | Ciencias Naturales / Biología | ●●●○○○○○○○ |
| 4 | El Experimento de la Conducta Invisible | Ciencias Sociales / Psicología | ●●●●○○○○○○ |
| 5 | Los Números del Decanato Fantasma | Administración / Contabilidad | ●●●●●○○○○○ |
| 6 | La Rúbrica que Pensaba Sola | Educación / Pedagogía | ●●●●●●○○○○ |
| 7 | El Plano del Edificio que No Coincidía | Arquitectura / Planificación | ●●●●●●●○○○ |
| 8 | El Laboratorio de los Ecos Digitales | Ingeniería / Computación | ●●●●●●●●○○ |
| 9 | El Reglamento de las Dos Verdades | Derecho / Ciencias Políticas | ●●●●●●●●●○ |
| 10 ★ | La Verdad Oculta de la Ciudad Universitaria | Salud Pública / Medicina Comunitaria | ●●●●●●●●●● |

El Caso 1 está activo con nivel simulado disponible en el MVP (Equipo Clio, Piloto V1.0).

---

## Los 35 badges — familias

| Familia | IDs | Foco |
|---|---|---|
| 1 — Observación y razonamiento | 001–003 | Ver lo que otros no ven |
| 2 — Investigación y verificación | 004–007 | Encontrar y contrastar fuentes |
| 3 — Documentación y custodia | 008–011 | Preservar la memoria del caso |
| 4 — IA Ética | 012–015 | Integrar IA con criterio y transparencia |
| 5 — Equipo y coordinación | 016–018 | Colaborar con disciplina operativa |
| 6 — Comunicación y storytelling | 019–021 | Comunicar con claridad y valor |
| 7 — Desarrollo técnico y MVP | 022–025 | Construir soluciones funcionales |
| 8 — Testing, auditoría y calidad | 026–028 | Verificar antes de entregar |
| 9 — Quinto Elemento | 029–032 | Custodiar la memoria viva del equipo |
| 10 — Badges épicos | 033–035 | Excelencia integral del sistema |

---

## Las 3 plantillas oficiales

Todas están en `templates/` en formato Markdown (MD) V1.1 con bloque YAML al inicio. Las vistas previas interactivas están disponibles en el MVP (pestaña Plantillas → 👁 Vista previa).

### `Plantilla_Expediente_V1_1.md`
Fuente principal de verdad documental. **Una por caso.** 24 secciones: portada, identidad del equipo, resumen ejecutivo, línea de tiempo, inventario de evidencias, cadena de custodia, registro de uso de IA, bitácora, matriz de hipótesis, análisis, conclusión y checklist de entrega. Abrir al inicio y mantener sincronizada hasta el cierre.

### `Plantilla_Evidencia_V1_1.md`
Ficha individual por evidencia. **Una por evidencia.** 15 secciones: identificación, descripción ampliada, origen y procedencia, cadena de custodia mínima, transformaciones realizadas, evaluación de confiabilidad, análisis interpretativo, uso de IA y valor documental. Ninguna evidencia entra al expediente sin ficha con ID único.

### `Plantilla_Bitacora_V1_0.md`
Memoria operativa de cada sesión. **Una por sesión.** 17 secciones: participación del equipo, propósito, agenda ejecutada, avances por área, evidencias nuevas, uso de IA, decisiones tomadas, problemas detectados, evaluación breve, reflexión del equipo y próximos pasos. La redacta el Quinto Elemento al finalizar cada bloque de trabajo.

---

## Flujo de trabajo del equipo

```
Equipo de 5 Junior DevOps
│
├─ Integrante 1 · Arquitectura    → Organiza la lógica del caso o prototipo
├─ Integrante 2 · Interfaz / UX   → Claridad visual, legibilidad y accesibilidad
├─ Integrante 3 · Lógica          → Funcionalidad, flujo de datos, consistencia
├─ Integrante 4 · Testing         → Valida criterios, revisa fallos, sostiene calidad
└─ Integrante 5 · Quinto Elemento → Documenta, custodia evidencias, trazabilidad ética
         │
         ▼
  1. Abre expediente del caso (Plantilla_Expediente_V1_1.md)
  2. Investiga y recopila evidencias
  3. Registra cada evidencia (Plantilla_Evidencia_V1_1.md)
  4. Documenta cada sesión (Plantilla_Bitacora_V1_0.md)
  5. Registra uso de IA en el IA-log del expediente
  6. Cierra el caso con conclusión argumentada y checklist completo
         │
         ▼
  Evaluación → Badges → Progresión al siguiente nivel
```

---

## Los 10 pilares del sistema

| # | Pilar | Principio |
|---|---|---|
| 1 | Propósito humano antes que automatización | La tecnología sirve a las personas, no al revés |
| 2 | Ética antes que velocidad | Ganar sin ética equivale a perder |
| 3 | Evidencia antes que opinión | Toda afirmación importante necesita respaldo verificable |
| 4 | Cadena de custodia antes que improvisación | Cada evidencia debe poder rastrearse por completo |
| 5 | Documentación antes que olvido | Lo que no se documenta bien se vuelve frágil e inútil |
| 6 | Colaboración antes que ego | Ningún miembro resuelve el caso solo |
| 7 | Aprendizaje en flujo | Los retos deben ser exigentes pero alcanzables |
| 8 | IA como asistente, no como reemplazo | Dr. Watson orienta; el juicio final es del equipo |
| 9 | Accesibilidad, justicia y respeto | La competencia no justifica exclusión ni opacidad |
| 10 | Legado y comunidad | Cada cohorte produce conocimiento reutilizable |

---

## Documentación de referencia

| Archivo | Contenido clave |
|---|---|
| `docs/01_Base_Estrategica.md` | 7 capas del sistema, actores, flujo sistémico, RoadMap por 10 fases |
| `docs/02_RuleBook_Maestro.md` | 12 mandamientos del detective ético, evidencia válida, faltas y consecuencias |
| `docs/03_Norma_Multimodal_Obsidian.md` | Design for InterOperability, nomenclatura, ciberseguridad, uso ético de IA |
| `docs/04_Estructura_10_Casos.md` | Los 10 casos completos: premisa, competencias, evidencias, productos, badges |
| `docs/05_Repositorio_Badges.md` | 35 badges: criterios, pasos, evidencia mínima, sistema de puntaje |
| `docs/06_Registro_Normalizacion.md` | Tabla de términos normalizados V1.1 y archivos afectados |

---

## Interoperabilidad

El proyecto está diseñado para circular sin pérdida semántica entre:

```
Markdown (MD) ↔ Obsidian ↔ GitHub ↔ VS Code ↔ Claude ↔ ChatGPT ↔ NotebookLM ↔ Perplexity
```

El **Segundo Cerebro Oficial del Proyecto** es **Obsidian**. Toda documentación crítica tiene ruta en el repositorio MD y, cuando aplique, en Obsidian (campo `ruta_segundo_cerebro_obsidian` en los metadatos YAML de cada plantilla).

---

## Cómo contribuir

1. **Crea una rama** con nombre descriptivo: `caso-01-ses-005` o `equipo-clio-evidencia-nueva`
2. **Usa las plantillas oficiales** — no improvises nuevos formatos sin consenso del mentor
3. **Documenta antes de entregar** — expediente, evidencias y bitácoras deben estar al día
4. **Registra el uso de IA** — toda interacción relevante con Dr. Watson GPT 2025 u otra IA consta en el expediente
5. **El Quinto Elemento valida** — antes de entregar, revisa coherencia documental
6. **Versiona con criterio** — semántica `1.0.0 → 1.0.1 → 1.1.0 → 2.0.0`
7. **Actualiza el changelog** — cada cambio significativo queda registrado

---

## Estado del proyecto

| Componente | Estado |
|---|---|
| MVP `index.html` | ✅ Funcional — piloto listo |
| Pestaña Panel | ✅ Completa con 10 pilares y acceso rápido clickeable |
| Pestaña Casos | ✅ 10 casos · modal de detalle · Nivel 1 simulado activo |
| Pestaña Equipos | ✅ 5 equipos simulados · vista resumen + vista individual completa |
| Pestaña Badges | ✅ 35 badges · modal expandido · filtro por familia |
| Pestaña Glosario | ✅ 50+ términos · buscador en tiempo real |
| Pestaña Plantillas | ✅ 3 plantillas · vista previa interactiva con sidebar navegable |
| `docs/` | ✅ 6 documentos normalizados V1.1 |
| `templates/` | ✅ 3 plantillas oficiales YAML + Markdown |
| `sherlock-mvp.zip` | ✅ 11 archivos empaquetados listos para distribución |

---

## Créditos y licencia

**Proyecto:** Sherlock Holmes y la Verdad Oculta V1.0  
**Unidad central:** Equipos de 5 Junior DevOps transdisciplinarios  
**Asistente narrativo:** Dr. Watson GPT 2025  
**Formato base oficial:** Markdown (MD)  
**Segundo Cerebro Oficial del Proyecto:** Obsidian  
**Idioma base:** Español  

### Licencia de uso institucional

Este repositorio está destinado a uso académico e institucional. Se permite copiar, adaptar y redistribuir con fines educativos no comerciales citando la fuente. Se permite adaptar los casos al contexto local con crédito al proyecto original. No se permite el uso comercial sin autorización expresa. Las contribuciones quedan bajo la misma licencia.

---

**Versión:** 1.0 · **Formato:** Markdown (MD) · **Estado:** Piloto institucional activo
