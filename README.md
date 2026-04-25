# Sherlock Holmes y la Verdad Oculta — V1.0

> *"No basta con tener una idea brillante. Hay que poder demostrarla, sostenerla éticamente y dejar evidencia clara de cómo se llegó a ella."*

---

## Inicio rápido

```bash
open index.html   # sin servidor, sin npm, sin configuración
```

---

## Estructura del repositorio

```
sherlock-mvp/
├── README.md
├── index.html                              ← MVP single-file · offline
│
├── docs/                                   ← Documentación de referencia
│   ├── 01_Base_Estrategica.md
│   ├── 02_RuleBook_Maestro.md
│   ├── 03_Norma_Multimodal_Obsidian.md
│   ├── 04_Estructura_10_Casos.md
│   ├── 05_Repositorio_Badges.md
│   ├── 06_Registro_Normalizacion.md
│   └── manuales/
│       └── MANUAL_USUARIO_Junior_DevOps_V1_0.md
│
├── templates/                              ← Plantillas oficiales — no editar directamente
│   ├── Plantilla_Expediente_V1_1.md
│   ├── Plantilla_Evidencia_V1_1.md
│   └── Plantilla_Bitacora_V1_0.md
│
├── casos/                                  ← Trabajo activo de los 5 equipos
│   ├── caso-01-manuscrito-extraviado/
│   │   └── EQ-HUM-01-Clio/
│   │       ├── expediente/
│   │       ├── evidencias/
│   │       ├── bitacoras/
│   │       └── CHANGELOG.md
│   ├── caso-02-portada-viral/
│   │   └── EQ-COM-02-Hermes/
│   ├── caso-03-jardin-especies/
│   │   └── EQ-BIO-03-Darwin/
│   ├── caso-04-conducta-invisible/
│   │   └── EQ-PSI-04-Freud/
│   └── caso-05-decanato-fantasma/
│       └── EQ-ADM-05-Fibonacci/
│
├── assets/                                 ← Recursos compartidos
│   ├── logos/
│   ├── imagenes-casos/
│   └── pistas-narrativas/
│
└── admin/                                  ← Solo Game Master y mentores
    ├── rubrica_evaluacion_v1_0.md
    ├── registro_badges_otorgados.md
    └── PROMPT_CONTINUACION_V1_0.md
```

---

## Convención de nomenclatura oficial

| Tipo | Patrón | Ejemplo |
|---|---|---|
| Expediente | `EXP-[FAC]-[EQ]-[NUM]_v[VER].md` | `EXP-HUM-01-001_v1_0.md` |
| Ficha de evidencia | `E-[NUM]_[descripcion].md` | `E-001_escaneo_manuscrito.md` |
| Archivo de evidencia | mismo nombre base que la ficha | `E-001_escaneo_manuscrito.png` |
| Bitácora | `SES-[NUM]_[FECHA].md` | `SES-004_2026-04-24.md` |

**Regla universal:** sin espacios · sin acentos en nombres de archivo · versión siempre al final.

---

## Regla de uso de plantillas

`templates/` es **zona protegida** — nunca se editan directamente. El flujo es:

```
1. Copiar plantilla → casos/[caso]/[equipo]/[subcarpeta]/
2. Renombrar con la convención oficial
3. Completar y versionar la copia de trabajo
4. Si la plantilla maestra cambia → versionar en templates/ + registrar en 06_Registro_Normalizacion.md
```

---

## Cómo añadir un caso o equipo nuevo

```bash
# Nuevo equipo en caso existente
mkdir -p casos/caso-01-manuscrito-extraviado/EQ-NEW-00-Nombre/{expediente,evidencias,bitacoras}

# Caso nuevo (niveles 2-10)
mkdir -p casos/caso-0N-nombre/EQ-XXX-0N-Nombre/{expediente,evidencias,bitacoras}
```

---

## Interoperabilidad Obsidian

La estructura espeja `casos/` para alinear los metadatos YAML de cada plantilla:

```yaml
ruta_repositorio:               "casos/caso-01-manuscrito-extraviado/EQ-HUM-01-Clio/expediente/"
ruta_segundo_cerebro_obsidian:  "Casos/Caso-01/EQ-HUM-01-Clio/"
```

---

## Referencia rápida de documentación

| Necesito... | Archivo |
|---|---|
| Entender el sistema | `docs/01_Base_Estrategica.md` |
| Reglas del juego | `docs/02_RuleBook_Maestro.md` |
| Nomenclatura e interoperabilidad | `docs/03_Norma_Multimodal_Obsidian.md` |
| Los 10 casos completos | `docs/04_Estructura_10_Casos.md` |
| Criterios de badges | `docs/05_Repositorio_Badges.md` |
| Vocabulario oficial | `docs/06_Registro_Normalizacion.md` |
| Roles del equipo de 5 | `docs/manuales/MANUAL_USUARIO_Junior_DevOps_V1_0.md` |
| Sistema interactivo | `index.html` |

---

**Versión:** 1.0 · **Formato:** Markdown (MD) · **Estado:** Piloto institucional activo
