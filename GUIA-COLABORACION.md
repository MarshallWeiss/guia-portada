# Guía de colaboración — Guía Portada 2026

Documento dirigido al equipo de diseño que va a contribuir a la guía de portada. Explica qué tienes que hacer en Figma, cómo organizamos el trabajo y cómo me envías tus entregables.

---

## Contexto rápido

Estamos construyendo la **Guía Portada 2026**: una documentación completa de todos los bloques, casos de uso y plantillas de la nueva portada. Por ahora vive en local (en el ordenador de Marshall) como un mini-sitio HTML que replica la estructura de la página de Notion *"Guía portada 2026"*.

El objetivo es que cada bloque de la portada (B1, B2, B3, B4, Issues, Opinión, etc.) tenga sus plantillas documentadas en tres tamaños: **Desktop (1512px), Tablet (768px) y Mobile (375px)**, más una **carátula CMS** (lo que ve el editor al pickear).

---

## Tu trabajo

### En Figma

Archivo: **Marshall-3** (`MBaHuH8034s6Pg7BgvaJPc`)

He creado una serie de páginas con el prefijo **"Guía Notion —"**. Cada una corresponde a un bloque de la portada y contiene secciones grises, una por cada caso de uso/plantilla.

Dentro de cada sección gris hay **4 frames blancos vacíos** ya nombrados:

| Frame | Tamaño | Para qué |
|-------|--------|----------|
| `*_desktop.png` | 1512×900 | Vista desktop |
| `*_tablet.png` | 768×900 | Vista tablet |
| `*_mobile.png` | 375×900 | Vista móvil |
| `*_caratula_cms.png` | 400×300 | Carátula del CMS |

**Tu tarea:** diseñar dentro de cada frame blanco la versión del template que te haya tocado.

### Reglas importantes

1. **No muevas ni renombres los frames.** Los nombres están vinculados al sitio HTML. Si cambias algo, se rompe la referencia.
2. **No cambies el tamaño del frame**, salvo la altura si el contenido necesita más (el ancho debe mantenerse: 1512, 768, 375 o 400).
3. **Mantén el fondo blanco** del frame. El gris es solo del contenedor padre (la sección).
4. **Las carátulas CMS** deben tener un padding de 16px y contenido centrado para que no se vean apretadas.
5. **El fondo de la sección gris sirve como "marco visual"** — respétalo, no lo sobrescribas.

### Casos especiales

- Si en tu bloque **faltan casos de uso** (por ejemplo, identificas un template nuevo que no tengo listado), avísame y los añado a la estructura.
- Si un caso aparece en el Figma de producción pero no en nuestra estructura, también avísame.

---

## Cómo me envías tu trabajo

**No necesitas exportar nada.** Yo me encargo de exportar los PNGs y meterlos en el sitio HTML.

Cuando termines tu bloque asignado, simplemente:

1. **Avísame por Slack** indicando qué bloque/caso de uso has terminado.
2. **Confirma que todos los frames (Desktop + Tablet + Mobile + Carátula CMS) están completos.**
3. Si has añadido secciones nuevas o renombrado algo, **mándame la lista**.

Yo sincronizo, exporto, y actualizo el sitio HTML. Luego te paso el enlace para que revises.

---

## Estado actual (a 2026-04-15)

| Bloque | Estado | Notas |
|--------|--------|-------|
| **B1 — Apertura principal** | ✅ Imágenes colocadas | 6 templates (A, B, C, C+apoyos, D, E) |
| **B2 — Enfoques y análisis** | 🔲 Figma listo, pendiente diseño | 12 casos de uso (A a K) |
| **B3 — Opinión / Eventos / Nichos** | 🔲 Figma listo | 3 templates — pendiente revisar casos reales en producción |
| **B4 — El Corecito** | ✅ Imágenes colocadas | 2 templates (A, B) |
| **Issues (B5-B9)** | 🔲 Figma listo | 3 templates — pendiente revisar |
| **Lo mejor de EC** | 🔲 Figma listo | 1 template |
| **Secciones destacadas** | 🔲 Figma listo | 2 templates |
| **Secciones secundarias** | 🔲 Figma listo | 1 template |
| **De compras** | 🔲 Figma listo | 1 template |
| **Branded oro** | 🔲 Figma listo | 1 template |
| **Opinión** | ✅ Imágenes colocadas | 5 casos |

---

## Flujo completo (para referencia)

```
1. Marshall crea páginas en Figma (Marshall-3)
     ↓
2. Tú diseñas dentro de los frames blancos
     ↓
3. Me avisas cuando termines
     ↓
4. Exporto los PNGs desde Figma
     ↓
5. Los coloco en el sitio HTML local
     ↓
6. Reviso que todo se ve bien
     ↓
7. Te paso el enlace o screenshots
```

---

## ¿Por qué no GitHub / Notion directamente?

- **Notion no permite subir imágenes por API**, solo URLs externas. Por eso hicimos el HTML.
- **GitHub requeriría** aprender Git, y preferimos que te centres en el diseño.
- **El HTML local** es la fuente de verdad por ahora. Cuando esté completo, lo migraremos al sitio público que corresponda.

---

## Preguntas frecuentes

**¿Puedo crear mi propia sección dentro de una página "Guía Notion"?**
Sí, pero avísame para que actualice el nombre y las referencias en el HTML.

**¿Qué hago si un frame se me queda corto (el contenido no entra)?**
Estira el frame hacia abajo (solo la altura, nunca el ancho). Los nombres del frame siguen funcionando.

**¿Los carátulas CMS son obligatorias?**
Sí — es importante que el editor vea qué está pickeando. Si no tienes una versión final, deja un placeholder sencillo.

**¿Dónde puedo ver los casos reales en producción?**
Archivo Figma: **Portada EC — producción** (`4EeCeod1E3YwUrR3ESwp42`). Pregúntame por el link si no lo tienes.

**¿A quién me asigno qué bloque?**
Lo coordinamos entre todos en el siguiente stand-up.

---

## Contacto

Cualquier duda: **Marshall** (Slack directo). Si es urgente, mensaje directo; si es algo que puede esperar, en el canal del proyecto.
