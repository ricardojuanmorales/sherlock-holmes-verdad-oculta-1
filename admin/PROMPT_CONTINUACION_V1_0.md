# Prompt de Continuación — Sherlock Holmes y la Verdad Oculta V1.0
## Documento de transferencia de contexto entre sesiones

> **Propósito:** Este documento permite retomar el desarrollo del proyecto en una conversación nueva de Claude sin perder el contexto, las decisiones tomadas, el estado actual del código ni los archivos producidos.  
> **Fecha de corte:** 25 de abril de 2026  
> **Estado al cierre de sesión:** MVP V1.0 completo y funcional

---

## INSTRUCCIONES PARA CLAUDE (leer primero)

Eres Claude y estás tomando el relevo de una sesión previa donde construiste el repositorio completo de **Sherlock Holmes y la Verdad Oculta V1.0**. Este documento contiene el estado exacto del proyecto, los archivos producidos, las decisiones técnicas tomadas y las reglas de trabajo que se acordaron. Léelo completo antes de hacer cualquier cosa.

**Reglas de trabajo que siguen vigentes:**
1. Un paso a la vez. No avances sin confirmar el entregable actual.
2. Cada paso produce archivos descargables via `present_files`. Espera confirmación.
3. Si algo no está claro, pregunta antes de generar.
4. No uses herramientas de build, npm, ni servidores. Todo funciona abriendo el archivo.
5. Idioma base: **español**. El código puede estar en inglés.
6. Si el proceso se congela o es muy largo, detente, entrega lo generado y espera instrucción.
7. El MVP es **un único archivo `index.html` autocontenido** — sin archivos externos, sin dependencias de servidor.

---

## 1. Identidad del proyecto

| Atributo | Valor |
|---|---|
| Nombre | Sherlock Holmes y la Verdad Oculta V1.0 |
| Naturaleza | Juego académico de investigación transdisciplinaria con ambiente lúdico-virtual |
| Unidad base | Equipos de 5 Junior DevOps (4 investigadores + 1 Quinto Elemento) |
| Contexto | Comunidad universitaria puertorriqueña |
| Formato base oficial | Markdown (MD) |
| Segundo Cerebro Oficial del Proyecto | Obsidian |
| Idioma base | Español |
| Frase rectora | *"No basta con tener una idea brillante. Hay que poder demostrarla, sostenerla éticamente y dejar evidencia clara de cómo se llegó a ella."* |

---

## 2. Estado actual del repositorio

### Estructura completa de archivos producidos

```
sherlock-mvp/                          ← Carpeta raíz del repositorio
├── README.md                          ← ✅ Actualizado V1.0 final (269 líneas · 14.8KB)
├── index.html                         ← ✅ MVP completo (3,031 líneas · 185KB)
│
├── docs/
│   ├── 01_Base_Estrategica.md         ← ✅ 10.8KB — Mapa sistémico y RoadMap evolutivo
│   ├── 02_RuleBook_Maestro.md         ← ✅ 15.9KB — Reglas, mandamientos y evaluación
│   ├── 03_Norma_Multimodal_Obsidian.md← ✅ 11.2KB — Interoperabilidad y Obsidian
│   ├── 04_Estructura_10_Casos.md      ← ✅ 17.6KB — Los 10 casos completos
│   ├── 05_Repositorio_Badges.md       ← ✅ 14.6KB — 35 badges con criterios
│   └── 06_Registro_Normalizacion.md   ← ✅ 6.2KB — Normalización terminológica V1.1
│
└── templates/
    ├── Plantilla_Expediente_V1_1.md   ← ✅ 12.5KB — 24 secciones · fuente de verdad
    ├── Plantilla_Evidencia_V1_1.md    ← ✅ 8.3KB — 15 secciones · ficha por evidencia
    └── Plantilla_Bitacora_V1_0.md     ← ✅ 6.8KB — 17 secciones · memoria de sesión
```

**ZIP empaquetado:** `sherlock-mvp.zip` — 11 archivos · 304KB descomprimido · ~92KB comprimido

---

## 3. Arquitectura del MVP (`index.html`)

### Tecnología
- HTML5 + CSS3 + JavaScript ES6 puro — **monolito autocontenido**
- Sin frameworks, sin npm, sin servidor
- Google Fonts cargadas desde CDN (Fraunces · Instrument Sans · JetBrains Mono)
- Funciona offline excepto las fuentes tipográficas

### Paleta de colores (variables CSS)

```css
--ink:           #1a1614   /* tinta oscura — fondo header */
--ink-light:     #2e2623   /* tinta nav */
--parchment:     #f4ead5   /* pergamino — fondo general */
--parchment-dark:#e8d9b8
--parchment-mid: #ede0c4
--red:           #8b1e1e   /* rojo expediente */
--red-light:     #a32424
--green:         #2e5d4b   /* verde detector */
--green-light:   #3a7460
--amber:         #c4813a   /* ámbar — acento cálido */
--sepia:         #7a5c3a
--muted:         #6b5a4a
```

### Tipografías
- Display/títulos: `Fraunces` (serif, óptico)
- Cuerpo: `Instrument Sans` (sans-serif)
- Código/IDs: `JetBrains Mono`

### Estética general
Vintage dossier + forensics moderno. Textura noise sobre el fondo. Sombras suaves. Animación `fadeIn` al cambiar pestañas. Scrollbar personalizado.

### Estructura de navegación (6 pestañas)

```
🏠 Panel  |  📂 Casos  |  👥 Equipos  |  🏅 Badges  |  📖 Glosario  |  📋 Plantillas
```

Función de cambio de pestaña: `switchTab(id, btn)` — también existe `goTab(id)` para navegación programática desde las tarjetas del Panel.

---

## 4. Datos embebidos en el MVP (objetos JS)

### `CASES` — 10 casos
Cada caso tiene:
```javascript
{
  level, status, title, discipline, complexity,
  premise, question,
  badges: [],        // nombres de badges aplicables
  badgeIds: [],      // IDs tipo 'BADGE-001'
  products: [],      // array de strings
  competencies: [],  // competencias requeridas
  evidenceTypes: [], // tipos de evidencia esperada
  difficulty,        // string — nota de dificultad
  simulation: {      // null para casos 2-10; objeto para caso 1
    team, teamCode, progress, phase,
    hypothesis: [{id, text, status}],
    evidences: [{id, type, desc, status}],
    badgesEarned: [], badgesInProgress: [],
    lastEntry, nextStep
  }
}
```

### `BADGES` — 35 badges
```javascript
{ id, fam, icon, name, level, type, criterion }
```
Familias 1–10. Niveles: I, II, III, IV, Épico. Tipos: Individual, Grupal, Individual/Grupal, Q5.

### `FAM_LABELS` — etiquetas de familias de badges
```javascript
{1:'Observación', 2:'Investigación', 3:'Documentación', 4:'IA Ética',
 5:'Equipo', 6:'Comunicación', 7:'Desarrollo', 8:'Testing',
 9:'Quinto Elemento', 10:'Épicos'}
```

### `GLOSSARY` — 50+ términos
```javascript
{ term, cat, brief, operative, example }
```

### `TEMPLATES` — 3 plantillas
```javascript
{ icon, version, name, file, desc, when, fields:[], sections }
```

### `TEAM_COLORS` — colores por equipo (array de 5)
```javascript
{ accent, avBg, avFg }
// azul / rojo / verde / ámbar / morado
```

### `TEAMS` — 5 equipos (objeto completo)
```javascript
{
  id, code, name, faculty, caseNum, caseName,
  progress, sessions, evidencias, iaLogs, badgesEarned,
  statusLabel, mentor,
  members: [{name, ini, role, roleShort, spec, contrib, q5?}],
  pregunta, hipotesis: [{id, text, status}],
  badges: [{name, earned}],
  bitacora: {ses, quien, texto},
  aiLog: {tool, uso, resultado, validado},
  evidencias: [{id, tipo, desc, status}]
}
```

### Datos de badges expandidos
- `BADGE_STEPS` — objeto `{id: [paso1, paso2, paso3]}` para los 35 badges
- `BADGE_EVMIN` — objeto `{id: string}` — evidencia mínima requerida
- `BADGE_TEAMS_EARNED` — objeto `{id: [teamName, ...]}` — equipos que lo ganaron

### `TEMPLATE_SECTIONS` — vistas previas de plantillas
Array de 3 elementos (uno por plantilla), cada uno con:
```javascript
{ sections: [{id, label, content}] }
// content = HTML con datos simulados del Equipo Clio / Caso 1
```

---

## 5. Funciones JS principales del MVP

### Navegación
- `switchTab(id, btn)` — cambia pestaña activa
- `goTab(id)` — navega programáticamente (desde cards del Panel)

### Renderizado inicial
- `renderCases()` — genera el grid de casos clickeables
- `renderBadgesFilter()` — genera botones de filtro por familia
- `renderBadgesGrid()` — genera grid de badges (respeta `activeFam`)
- `filterBadges(fam, btn)` — filtra badges por familia
- `renderGlossary(terms)` — genera acordeones del glosario
- `filterGlossary()` — filtra en tiempo real
- `toggleGlossary(i)` — abre/cierra acordeón individual
- `renderTemplates()` — genera lista de plantillas con botones
- `renderTeamsOverview()` — genera grid de tarjetas de equipo
- `openTeam(id)` — abre vista detalle de equipo
- `backToTeams()` — regresa a la vista overview de equipos

### Modales
- `openCase(idx)` — abre modal detalle de un caso (incluye bloque simulación si existe)
- `closeCase()` / `closeCaseHelper()`
- `openBadge(id)` — abre modal detalle de un badge
- `closeBadge()`
- `openTpl(idx)` — abre modal vista previa de plantilla con sidebar navegable
- `switchTplSec(i, btn)` — cambia sección en el sidebar de la plantilla
- `closeTpl()`

### Variables globales relevantes
- `activeFam` — familia activa en el filtro de badges (0 = todas)
- `_currentTplIdx` — índice de plantilla activa en el modal de preview

---

## 6. Los 5 equipos del piloto (estado al cierre)

| Equipo | Código | Facultad | Caso | % |
|---|---|---|---|---|
| Clio | EQ-HUM-01 | Humanidades · Historia | 1 — El Manuscrito Extraviado | 78% |
| Hermes | EQ-COM-02 | Comunicación · Periodismo | 2 — La Portada Viral | 62% |
| Darwin | EQ-BIO-03 | Ciencias Naturales · Biología | 3 — El Jardín de las Especies | 45% |
| Freud | EQ-PSI-04 | Ciencias Sociales · Psicología | 4 — La Conducta Invisible | 33% |
| Fibonacci | EQ-ADM-05 | Administración · Contabilidad | 5 — El Decanato Fantasma | 19% |

**Estadísticas globales actuales:** 5 equipos · 25 Junior DevOps · 47 badges otorgados · 138 evidencias capturadas

---

## 7. Miembros de cada equipo (referencia rápida)

### Equipo Clio (Humanidades)
Sofía Maldonado-Torres (ARQ), Rodrigo Vega-Acosta (UX), Tanisha Morales-Rivera (LOG), Alejandro Figueroa-Ortiz (QA), Yolanda Nieves-Cruz (Q5). Mentor: Dra. Carmen Quiñones.

### Equipo Hermes (Comunicación)
Omar Delgado-Sánchez (ARQ), Valeria Ramos-Colón (UX), Keisha Pérez-Burgos (LOG), Javier Suárez-Marín (QA), Camila Hernández-Agosto (Q5). Mentor: Prof. Rafael Meléndez.

### Equipo Darwin (Biología)
Daniela Reyes-Meléndez (ARQ), Marcus Ruiz-Santiago (UX), Isadora Fontánez-López (LOG), Emmanuel Torres-Díaz (QA), Natalia Correa-Medina (Q5). Mentor: Dr. Antonio Pagán-Jiménez.

### Equipo Freud (Psicología)
Ricardo Álvarez-Guerrero (ARQ), Paola Castillo-Vega (UX), Xiomara González-Pons (LOG), Sebastián Moreno-Ríos (QA), Amara Jiménez-Ortega (Q5). Mentor: Dra. Miriam Colón-Berríos.

### Equipo Fibonacci (Administración)
Andrés Vázquez-Rodríguez (ARQ), Luna Pagán-Serrano (UX), Carlos Cotto-Rivera (LOG), Isabella Mercado-Benítez (QA), Felipe Ayala-Ramos (Q5). Mentor: Prof. José Ayala-Vargas.

---

## 8. Estado de los modales — qué contiene cada uno

### Modal de caso (`caseModal`)
- Encabezado oscuro con número gigante de fondo, disciplina, título, complejidad, estado
- Bloque de simulación (solo Caso 1): progreso, hipótesis con estado, evidencias, badges, próximo paso
- Pregunta rectora destacada con borde ámbar
- Premisa completa
- Competencias del investigador (chips)
- Tipos de evidencia esperada (chips)
- Productos mínimos esperados (lista con puntos)
- Nota de dificultad (caja roja suave)
- Badges aplicables como botones que abren `openBadge()`

### Modal de badge (`badgeModal`)
- Icono grande, familia, nombre, nivel, tipo (Q5 / Individual / Grupal)
- Criterio oficial de otorgación (caja)
- Pasos numerados para ganarlo (lista)
- Evidencia mínima requerida (caja ámbar)
- Equipos del piloto que ya lo han obtenido (chips verdes)

### Modal de plantilla (`tplModal`)
- Header con icono, versión y nombre
- Layout de dos columnas: sidebar oscuro (secciones) + contenido blanco
- Sidebar navegable con `switchTplSec()`
- Contenido renderiza HTML con datos simulados reales del Caso 1 / Equipo Clio

---

## 9. Normalización V1.1 vigente

Los siguientes términos están normalizados en todos los documentos:

| Antes | Ahora |
|---|---|
| ruta_obsidian | ruta_segundo_cerebro_obsidian |
| documentación espejo en Obsidian | registro estructurado en el Segundo Cerebro Oficial del Proyecto: Obsidian |
| formatos espejo: MD / JSON / HTML | formatos interoperables: Markdown (MD) / JSON / HTML |

El formato base oficial es **Markdown (MD)**. El Segundo Cerebro Oficial del Proyecto es **Obsidian**.

---

## 10. Inventario de decisiones técnicas tomadas

| Decisión | Razonamiento |
|---|---|
| Monolito HTML sin frameworks | Requisito explícito: funcionar con doble clic, sin servidor, sin npm |
| Datos embebidos como objetos JS | Permite edición directa del archivo sin build tools |
| Modales con overlay (position:fixed) | Mejor que nuevas páginas para no perder estado de la app |
| `document.body.style.overflow='hidden'` al abrir modal | Evita scroll del fondo mientras el modal está abierto |
| `onclick="if(event.target===this)closeModal()"` en overlay | Cierra el modal al hacer clic fuera sin necesidad de event delegation complejo |
| `_currentTplIdx` como variable global | Permite que `switchTplSec()` sepa qué plantilla está activa sin pasar parámetros |
| Colores de equipo como array `TEAM_COLORS` | Desacoplado del array `TEAMS` para reutilizar en cualquier componente |
| CSS var() en toda la paleta | Facilita theming y consistencia sin variables duplicadas |
| `font-optical-sizing: auto` en Fraunces | Activa el eje óptico de la fuente variable para mejor renderizado |
| Rutas de plantillas en `href` de descarga | `href="templates/filename.md"` — funciona cuando el ZIP está descomprimido en carpeta |
| Google Fonts como única dependencia externa | Tipografía no puede embeberse en ~185KB sin comprimir dramáticamente el archivo |

---

## 11. Lo que NO se ha construido todavía (backlog sugerido)

Los siguientes elementos fueron mencionados o son lógicos continuaciones del proyecto y aún no existen:

### Funcionalidades MVP
- [ ] Sistema de progresión real: desbloquear casos al completar el anterior
- [ ] Formulario de apertura de expediente desde el MVP (crear nuevo equipo)
- [ ] Tablero de administración para el Game Master
- [ ] Exportación de expediente a Markdown desde el MVP
- [ ] Modo oscuro / modo pergamino (toggle)
- [ ] Vista de ranking entre los 5 equipos
- [ ] Notificaciones / sistema de alertas de badges ganados

### Contenido
- [ ] Niveles 2–10 con simulación activa (actualmente solo el Nivel 1 tiene datos simulados)
- [ ] Cartas de pista por caso (narrativa de "Dr. Watson GPT 2025 dice...")
- [ ] Rúbricas detalladas por nivel (PDF o MD)
- [ ] Casos opcionales de especialidad local puertorriqueña
- [ ] Conexiones narrativas entre casos (pistas que vinculan casos)

### Infraestructura
- [ ] Integración con Obsidian (vault plantilla lista para usar)
- [ ] GitHub Actions para validación automática de nomenclatura de archivos
- [ ] Script de inicialización de expediente nuevo desde terminal
- [ ] Panel de métricas en tiempo real (requeriría backend)

---

## 12. Archivos fuente originales (MD adjuntos en la sesión anterior)

Estos archivos fueron el material de origen. Están disponibles en el repositorio de Claude como documentos adjuntos de la sesión anterior. Si se necesitan de nuevo, pedir al usuario que los adjunte:

- `README_Sherlock_Holmes_y_la_Verdad_Oculta_V1_0.md`
- `Sherlock_Holmes_y_la_Verdad_Oculta_Base_Estrategica_V1_1_Normalizada.md`
- `RuleBook_Maestro_Sherlock_Holmes_y_la_Verdad_Oculta_V1_1_Normalizado.md`
- `Norma_Base_Uso_Multimodal_Interoperabilidad_y_Obsidian_V1_0.md`
- `Estructura_Inicial_10_Casos_Ascendente_V1_0.md`
- `Repositorio_Oficial_de_Badges_y_Criterios_de_Otorgacion_V1_0.md`
- `Mega_Glosario_Unico_V1_0.md`
- `Plantilla_Generica_Oficial_Expediente_de_Caso_Unico_V1_1_Normalizada.md`
- `Plantilla_Oficial_Evidencia_Individual_V1_1_Normalizada.md`
- `Plantilla_Oficial_Bitacora_de_Sesion_V1_0.md`
- `Registro_Normalizacion_Fina_de_Lenguaje_V1_0.md`

---

## 13. Cómo retomar el trabajo — instrucciones para el usuario

### Para continuar el desarrollo del MVP

1. Adjunta el archivo `index.html` actual a la nueva conversación (o el ZIP completo)
2. Comparte este documento `PROMPT_CONTINUACION_V1_0.md`
3. Indica qué quieres hacer a continuación (ver backlog en sección 11)
4. Claude leerá este documento y el HTML adjunto antes de hacer cualquier cambio

### Para añadir un caso nuevo simulado (niveles 2–10)

Indica: *"Añadir simulación al Caso [N] con el Equipo [Nombre]"*. Claude tomará el patrón del Caso 1 y construirá el bloque de datos correspondiente para la propiedad `simulation` del caso en el array `CASES`.

### Para añadir funcionalidades al MVP

Describe la función deseada. Claude editará el `index.html` directamente con `str_replace` quirúrgico y entregará el archivo actualizado via `present_files`.

### Para añadir nuevos miembros o equipos

Proporciona: nombre completo, rol (ARQ/UX/LOG/QA/Q5), especialidad y equipo. Claude actualizará el array `TEAMS` en el script del MVP.

### Para actualizar el estado de progreso de un equipo

Indica: *"Equipo [Nombre]: progreso [X]%, sesión [N] completada, evidencias [N], badges nuevos: [lista]"*. Claude actualizará los datos en el objeto correspondiente del array `TEAMS`.

---

## 14. Fragmento de código de referencia — cómo se añade un caso simulado

Para añadir simulación al Caso 2 (actualmente `simulation: null`), el patrón es:

```javascript
simulation: {
  team: 'Equipo Hermes', teamCode: 'EQ-COM-02', progress: 62,
  phase: 'Fase 2 — Investigación de fuente original',
  hypothesis: [
    { id:'H1', text:'Portada real con titular modificado 3 semanas después.', status:'strong' },
    { id:'H2', text:'Imagen auténtica descontextualizada intencionadamente.', status:'open' },
    { id:'H3', text:'Fabricación completa usando plantilla del medio.', status:'weak' },
  ],
  evidences: [
    { id:'E-001', type:'Captura', desc:'Portada viral con metadatos de descarga', status:'ok' },
    { id:'E-002', type:'Wayback', desc:'Portada original — 3 semanas anterior', status:'ok' },
    { id:'E-003', type:'EXIF', desc:'Reporte metadatos — timestamp manipulado', status:'an' },
  ],
  badgesEarned: ['Cazador de Fuentes','Ojo de Baker Street','Watson Bien Consultado','Voz del Detective'],
  badgesInProgress: ['Triangulador de la Verdad','Doble Verificación'],
  lastEntry: 'SES-003: Timestamp manipulado confirmado por análisis EXIF. H1 gana fuerza.',
  nextStep: 'Identificar origen del primer posteo del titular modificado — SES-004 programada.'
}
```

---

## 15. Resumen ejecutivo del estado del proyecto

**Lo que existe y funciona:**
- MVP HTML single-file completo con 6 pestañas interactivas
- 10 casos con modal de detalle completo; Caso 1 con nivel simulado activo
- 5 equipos universitarios simulados con vista individual de dashboard
- 35 badges con modal expandido, pasos, evidencia mínima y estado en equipos del piloto
- Glosario con 50+ términos y buscador en tiempo real
- 3 plantillas con vistas previas interactivas navegables por secciones
- 6 documentos de referencia normalizados V1.1
- README.md completo que refleja el estado real del proyecto
- ZIP empaquetado con los 11 archivos del repositorio

**Principios que no deben romperse en ninguna iteración:**
- El MVP sigue siendo un único archivo HTML autocontenido
- Todos los datos siguen siendo objetos JS embebidos directamente
- La paleta, tipografía y estética vintage dossier se mantienen
- El idioma base es español (los comentarios de código pueden ser inglés)
- Cada cambio se entrega como archivo descargable antes de continuar

---

*Documento generado al cierre de la sesión de desarrollo V1.0 · 25 de abril de 2026 · Claude Sonnet 4.6*  
*Formato oficial: Markdown (MD) · Para uso interno del proyecto*
