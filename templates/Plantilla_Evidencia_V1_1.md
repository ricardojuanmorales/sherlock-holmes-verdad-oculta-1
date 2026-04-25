---
template_version: "1.1"
fecha_normalizacion: "2025"
uso: "Una por evidencia. Crear al capturar cada pieza y vincularla al expediente del caso correspondiente."
formato_oficial: "Markdown (MD)"
segundo_cerebro_oficial: "Obsidian"
estado: "Lista para reutilización institucional"
---

# Plantilla Oficial de Evidencia Individual V1.1 Normalizada
## Sherlock Holmes y la Verdad Oculta

> **Propósito:** Esta plantilla documenta una sola evidencia de manera trazable, verificable y reutilizable. Debe usarse cada vez que una evidencia entre formalmente al expediente de un caso.

---

## Instrucciones de uso

1. Use **una plantilla por evidencia**.
2. No borre campos oficiales; si algo no aplica, escriba `No aplica`.
3. Toda evidencia debe tener **ID único**.
4. Toda transformación debe quedar registrada.
5. Si intervino IA, debe documentarse.
6. La evidencia debe poder vincularse a un caso, a una hipótesis o a una decisión.
7. El idioma base es **español**.

---

## Metadatos rápidos

```yaml
evidencia_id: "E-000"
expediente_id: "EXP-UNICO-000"
titulo_evidencia: ""
version_ficha: "1.0.0"
estado: "capturada | en_analisis | validada | descartada | archivada"
fecha_registro: "AAAA-MM-DD"
hora_registro: "HH:MM"
responsable_registro: ""
quinto_elemento_validador: ""
```

---

## 1. Identificación general

**Título de la evidencia:**  
[Nombre breve y claro]

**ID de evidencia:**  
[Ej. E-001]

**Caso o expediente asociado:**  
[Ej. EXP-UNICO-001]

**Tipo de evidencia:**  
- [ ] Texto
- [ ] Imagen
- [ ] Audio
- [ ] Video
- [ ] Captura de pantalla
- [ ] Enlace
- [ ] Archivo
- [ ] Código
- [ ] Nota de campo
- [ ] Testimonio
- [ ] Resultado de prueba
- [ ] Otro: _________

**Estado actual:**  
- [ ] Capturada
- [ ] En análisis
- [ ] Validada
- [ ] Descartada
- [ ] Archivada

---

## 2. Descripción de la evidencia

### 2.1 Descripción breve
[Explique en 2 o 3 líneas qué es esta evidencia]

### 2.2 Descripción ampliada
[Explique el contenido con suficiente detalle para que otra persona la entienda sin verla directamente]

### 2.3 Relación con el caso
[Explique por qué esta evidencia importa dentro del caso]

### 2.4 Relación con hipótesis o preguntas
- Hipótesis relacionada:
- Pregunta rectora relacionada:
- Decisión o análisis al que aporta:

---

## 3. Origen y procedencia

**Fuente directa:**  
[Persona, documento, sitio, sistema, observación o contexto de donde proviene]

**Tipo de procedencia:**  
- [ ] Primaria
- [ ] Secundaria
- [ ] Terciaria
- [ ] Derivada
- [ ] Desconocida
- [ ] Mixta

**Contexto de obtención:**  
[Explique dónde, cómo y en qué circunstancias se obtuvo]

**Fecha de captura u obtención:**  
[AAAA-MM-DD]

**Hora de captura u obtención:**  
[HH:MM]

**Lugar o entorno de captura:**  
[Laboratorio, navegador, repositorio, aula, entorno virtual, otro]

**Responsable de captura:**  
[Nombre]

**Responsable de registro:**  
[Nombre]

---

## 4. Archivo o soporte asociado

**Nombre del archivo original:**  
[Nombre exacto]

**Formato del archivo:**  
[.png, .jpg, .pdf, .md, .txt, .mp4, .wav, .html, etc.]

**Tamaño aproximado:**  
[Indique si aplica]

**Ruta local:**  
[Ubicación del archivo]

**Ruta en repositorio:**  
[Ubicación dentro del proyecto]

**Ruta en el Segundo Cerebro Oficial del Proyecto: Obsidian:**  
[Si aplica]

**Hash o control de integridad:**  
[SHA256 / MD5 / No aplica]

**Copia de respaldo generada:**  
- [ ] Sí
- [ ] No

**Ubicación del respaldo:**  
[Indique si existe]

---

## 5. Cadena de custodia mínima

| Registro ID | Acción | Fecha | Hora | Responsable | Observaciones |
|---|---|---|---|---|---|
| CC-001 | Captura inicial |  |  |  |  |
| CC-002 | Registro en ficha |  |  |  |  |
| CC-003 | Copia al repositorio |  |  |  |  |
| CC-004 | Análisis o revisión |  |  |  |  |
| CC-005 | Uso en conclusión o entrega |  |  |  |  |

### Incidentes de custodia
- [ ] No hubo incidentes
- [ ] Hubo incidentes

**Detalle de incidentes si aplica:**  
[Explique pérdida parcial, edición accidental, duplicado, duda de autenticidad, archivo corrupto, etc.]

---

## 6. Transformaciones realizadas

> Toda transformación debe quedar documentada para proteger la integridad de la evidencia.

| Transformación ID | Tipo de cambio | Responsable | Fecha | Justificación |
|---|---|---|---|---|
| TR-001 | Ninguna / recorte / transcripción / limpieza / resumen / anotación / conversión |  |  |  |
| TR-002 |  |  |  |  |

### Descripción narrativa de transformaciones
[Explique paso a paso qué cambios se hicieron y por qué]

### ¿Se conserva el original sin alterar?
- [ ] Sí
- [ ] No
- [ ] No aplica

---

## 7. Evaluación de confiabilidad

### 7.1 Nivel preliminar de confiabilidad
- [ ] Alto
- [ ] Medio
- [ ] Bajo
- [ ] En disputa
- [ ] No determinado

### 7.2 Razones para ese nivel
- [ ]
- [ ]
- [ ]

### 7.3 Señales de confiabilidad
- [ ]
- [ ]
- [ ]

### 7.4 Señales de alerta
- [ ]
- [ ]
- [ ]

### 7.5 Necesidad de verificación adicional
- [ ] Sí
- [ ] No

**Si sí, explique qué falta por verificar:**  
[Detalle]

---

## 8. Análisis interpretativo

### 8.1 ¿Qué muestra esta evidencia?
[Explique el contenido observable]

### 8.2 ¿Qué permite inferir?
[Explique inferencias posibles, distinguiéndolas claramente de los datos]

### 8.3 ¿Qué no puede concluirse todavía?
[Explique límites interpretativos]

### 8.4 Relación con otras evidencias
| Evidencia vinculada | Tipo de relación | Comentario |
|---|---|---|
| E-000 | confirma / contradice / amplía / contextualiza / pone en duda |  |
| E-000 |  |  |

---

## 9. Uso de IA relacionado con esta evidencia

### ¿Intervino IA en algún momento?
- [ ] Sí
- [ ] No

### Si intervino IA, complete:

| IA-Log ID | Herramienta | Uso específico | Fecha | Resultado | Validación humana |
|---|---|---|---|---|---|
| IA-001 | Dr. Watson GPT 2025 / otra | resumen / clasificación / análisis / sugerencia / transcripción |  |  | sí / no |

**Prompt o instrucción breve utilizada:**  
[Registre lo esencial]

**Riesgos detectados en la intervención de IA:**  
- [ ]
- [ ]
- [ ]

**Correcciones o verificaciones humanas realizadas:**  
[Explique cómo se revisó la salida]

---

## 10. Uso de la evidencia en el caso

### Esta evidencia fue usada para:
- [ ] Abrir una hipótesis
- [ ] Confirmar una hipótesis
- [ ] Descartar una hipótesis
- [ ] Tomar una decisión técnica
- [ ] Sustentar una conclusión
- [ ] Generar una nueva duda
- [ ] No se ha usado todavía

### Decisiones o secciones impactadas
- [ ]
- [ ]
- [ ]

### Citas o referencias internas donde aparece
- [ ]
- [ ]
- [ ]

---

## 11. Valor documental

### ¿Qué pasaría si esta evidencia faltara?
[Explique su relevancia para la integridad del caso]

### Nivel de criticidad
- [ ] Crítica
- [ ] Importante
- [ ] Complementaria
- [ ] Accesoria

### Recomendación de preservación
- [ ] Preservar original y copias
- [ ] Preservar solo en expediente
- [ ] Puede archivarse sin prioridad
- [ ] Descartar al cierre con justificación

---

## 12. Checklist de control

- [ ] Tiene ID único
- [ ] Está asociada a un expediente
- [ ] Su origen fue documentado
- [ ] Tiene fecha y responsable
- [ ] Tiene ruta de archivo o soporte
- [ ] Su cadena de custodia fue iniciada
- [ ] Las transformaciones fueron registradas
- [ ] Su confiabilidad fue evaluada
- [ ] Se documentó el uso de IA si existió
- [ ] Puede ser entendida por un tercero

---

## 13. Validación interna

| Nombre | Rol | Validación | Fecha |
|---|---|---|---|
|  | Responsable de registro |  |  |
|  | Quinto Elemento |  |  |
|  | Revisor técnico o metodológico |  |  |

---

## 14. Control de versiones

| Versión | Fecha | Cambio | Responsable |
|---|---|---|---|
| 1.0.0 |  | Creación inicial |  |
| 1.0.1 |  |  |  |
| 1.1.0 |  |  |  |

---

## 15. Cierre simbólico

> **Principio rector:**  
> Una evidencia vale no solo por lo que muestra, sino por la claridad con que puede rastrearse, comprenderse y sostenerse éticamente.

**Formato oficial:** Markdown (MD)  
**Versión de plantilla:** 1.1 Normalizada  
**Estado:** Lista para reutilización institucional

---

## Nota de normalización V1.1

Toda evidencia crítica debe tener ruta verificable en el Repositorio Documental Oficial en Markdown (MD) y, cuando aplique, en el Segundo Cerebro Oficial del Proyecto: Obsidian.
