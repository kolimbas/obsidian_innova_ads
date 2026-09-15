---
tags:
  - meta
  - methodology
  - spec-kit
  - nivel-2
updated: 2026-09-14
---

# Metodología — Spec Kit por campaña

> Regla dura: **ninguna campaña se crea en Ads Manager hasta que existen `brief.md`, `research.md`, `plan.md` y `tasks.md`, y Francisco confirmó el plan.** Es la misma lógica que el Spec Kit de n8n en el vault innova, adaptada a pauta.

← Volver a [[meta/README|Meta Ads KB]]
---

## Los seis artefactos

| Archivo | Qué contesta | Cuándo se escribe |
| --- | --- | --- |
| `brief.md` | **¿Qué quiere el cliente y qué vale conseguirlo?** Oferta, público, valor de un cliente, historia previa, KPI y umbral. | Primero, de la reunión de brief. |
| `research.md` | **¿Qué sabemos ya?** Campañas previas del cliente, campañas parecidas de otros clientes, playbooks aplicables, competencia en la Biblioteca de anuncios. | Después del brief. |
| `plan.md` | **¿Cómo se arma?** Objetivo, estructura campaña/conjunto/anuncio, audiencias, presupuesto, creativos, medición, calendario, umbrales de decisión. | Después del research, antes de tocar Ads Manager. |
| `tasks.md` | **¿Cuáles son los pasos?** Checklist ordenado con puntos de verificación. | Junto con el plan. |
| `resultados.md` | **¿Qué pasó?** Tabla semanal de métricas, decisiones tomadas y por qué. | Se va llenando mientras corre. |
| `retro.md` | **¿Qué aprendimos?** Qué funcionó, qué no, qué se promueve a playbook, tiempo invertido. | Al cerrar o al mes de correr. |

Plantillas: [[meta/templates/brief|brief]] · [[meta/templates/research|research]] · [[meta/templates/plan|plan]] · [[meta/templates/tasks|tasks]] · [[meta/templates/resultados|resultados]] · [[meta/templates/retro|retro]] · [[meta/templates/creativo|creativo]] · [[meta/templates/reporte-semanal|reporte semanal]] · [[meta/templates/cliente-README|README de cliente]] · [[meta/templates/ACCESOS-PUNTERO|ACCESOS-PUNTERO]] · [[meta/templates/ficha-cliente|ficha comercial]] · [[meta/templates/propuesta-comercial|propuesta comercial]] · [[meta/templates/acuerdo-de-gestion|acuerdo de gestión]] · [[meta/templates/auditoria-cuenta|auditoría de cuenta]] · [[meta/templates/brief-creativos|brief de creativos]].

Un bundle completo de ejemplo, con las plantillas llenas: `meta/clientes/innova/campanas/2026-10-agentes-ia-leads/`.

---

## Paso a paso

### 0. Intake

Llega un pedido (reunión, audio, WhatsApp). Identificar:

- **Cliente** → ¿existe `meta/clientes/<slug>/`? Si no, correr workflow *el onboarding* primero.
- **Slug de campaña** → `YYYY-MM-<que-vende>-<objetivo>`: `2026-10-turnos-leads`, `2026-11-hotsale-ventas`.
- Crear `meta/clientes/<slug>/campanas/<campaña>/` y copiar las plantillas.

### 1. Brief (`brief.md`)

Traducir el pedido a:

- **Oferta** — qué se vende exactamente, precio, qué la hace distinta.
- **Público** — quién compra, dónde está, qué problema tiene, qué ya probó.
- **Economía** — cuánto vale un cliente (ticket × recompra), qué CPL/CPA hace que el negocio gane. **Sin este número no hay umbral y no hay campaña.**
- **Historia** — qué pautó antes, con qué resultado, qué cuenta y píxel existen.
- **Embudo** — a dónde va el click: sitio, WhatsApp, formulario, mensaje.
- **KPI principal y umbral** — "CPL menor a X" o "ROAS mayor a Y". Uno solo.
- **Fuera de alcance** y **preguntas abiertas**.

Parar acá y confirmar con el cliente si alguna pregunta abierta cambia el plan.

### 2. Research (`research.md`)

El paso de reutilización. Siempre, en este orden:

1. **Campañas previas del mismo cliente** — leer todos los `retro.md` y `resultados.md` de su carpeta.
2. **Campañas parecidas de otros clientes** — mismo rubro, mismo objetivo, mismo embudo.
3. **Playbooks** — qué aplica de playbook *playbooks* y qué contradice.
4. **Competencia** — Biblioteca de anuncios de Meta: qué corren los 3-5 competidores, hace cuánto (un anuncio que lleva meses activo funciona).
5. **Plataforma** — cambios recientes en *research* (`research/research`) que afecten el plan.

Registrar como: **qué reutilizamos** y **por qué cada decisión**. Si una campaña previa cubre más del 60% del caso, es la **base** y el plan arranca de una copia.

### 3. Plan (`plan.md`)

Decidir por escrito, antes de abrir Ads Manager:

- **Objetivo de campaña** (uno de los seis) y **evento de optimización**.
- **Estructura** — cuántas campañas, conjuntos y anuncios, y por qué. Por defecto: pocas campañas, presupuesto en campaña, creativos variados.
- **Audiencias** — amplia, intereses, personalizadas, similares; exclusiones (clientes actuales, leads recientes).
- **Presupuesto** — diario, total, duración mínima de test, cuánto se necesita para salir de aprendizaje.
- **Creativos** — cuántos, qué ángulos, qué formatos. Mínimo 3 ángulos × 2 formatos.
- **Medición** — píxel/CAPI verificados, eventos, UTMs, dónde se ve el lead.
- **Umbrales de decisión** — a qué número se apaga un anuncio, a cuál se escala, cuándo se avisa al cliente.
- **Calendario** — lanzamiento, primera revisión (día 4-5), revisión semanal, cierre.
- **Riesgos** — políticas de Meta que puedan rechazar el anuncio, categoría especial, cuenta nueva sin historial.

Cerrar con un diagrama mermaid del embudo.

### 4. Tasks (`tasks.md`)

Checklist ordenado, agrupado por fase:

- Setup (accesos, píxel, dominio, método de pago, audiencias personalizadas)
- Creativos (brief, producción, aprobación del cliente)
- Build (campaña, conjuntos, anuncios, UTMs, nombres)
- Verificación (vista previa, test del píxel, prueba de formulario o WhatsApp)
- Lanzamiento
- Optimización (revisiones fechadas)
- Reporte y retro

### 5. Build y lanzamiento

Seguir workflow *el checklist de lanzamiento*. Tildar tareas a medida que se hacen. Si algo se desvía del plan, **se corrige el plan** (que no mienta).

### 6. Resultados (`resultados.md`)

Una fila por semana con las métricas del KPI principal y sus secundarias, y debajo **cada decisión con fecha y motivo**: "05/10: apagado anuncio B, CPL 2,3× el umbral tras 4 días". Es la memoria de la campaña.

### 7. Retro (`retro.md`)

Obligatorio antes de cerrar, y al mes si la campaña sigue. Secciones:

- **Qué funcionó / qué no**
- **Reutilizable** — qué se promueve a un playbook o al README del cliente
- **Gotchas de la plataforma** — rechazos, bugs, cambios
- **Tiempo invertido** vs. estimado
- **Pendientes**

Sumar una línea a *Lecciones* (`meta/lecciones`).

---

## Cuándo se pueden saltear pasos

**Nunca brief, plan y tasks.** Son el contrato.

`research.md` puede ser 5 líneas, pero la búsqueda se hace. `retro.md` puede ser 3 viñetas si la campaña fue chica, pero existe.

---

## Anti-patrones

- ❌ Lanzar sin saber cuánto vale un cliente para el negocio.
- ❌ Tocar presupuesto o audiencias cada día. Cada cambio grande reinicia el aprendizaje.
- ❌ Un solo creativo. El sistema necesita variedad para encontrar a quién mostrarle qué.
- ❌ Pautar a un sitio sin píxel o a un WhatsApp que nadie contesta.
- ❌ Reportar impresiones y alcance como si fueran resultados.
- ❌ Cerrar sin retro.
