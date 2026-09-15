---
tags:
  - meta
  - playbook
  - glosario
  - nivel-3
updated: 2026-09-14
---

# Glosario de Meta Ads

> Ads Manager en español, la documentación y los tutoriales en inglés. Para que todo el equipo hable igual: cómo aparece en la interfaz, cómo aparece en inglés, y qué es en una línea.

← Volver a [[meta/playbooks/_index|Playbooks]]
---

## Estructura y cuenta

| En Ads Manager (ES) | En inglés | Qué es |
| --- | --- | --- |
| Portfolio empresarial | Business Portfolio / Business Manager | Contenedor de páginas, cuentas, píxeles y personas de una empresa |
| Cuenta publicitaria | Ad account | Donde viven campañas y facturación (`act_…`) |
| Socio | Partner | Otra empresa con acceso a tus activos sin usar tu usuario |
| Campaña → Conjunto de anuncios → Anuncio | Campaign → Ad set → Ad | Objetivo y presupuesto → audiencia, ubicaciones, optimización → creativo |
| Ubicaciones | Placements | Dónde se muestra: feed, historias, reels, Messenger, red de audiencia |
| Ubicaciones Advantage+ | Advantage+ placements | Meta elige las ubicaciones (antes "automáticas") |
| Presupuesto de campaña Advantage+ | Advantage+ campaign budget (ex CBO) | Presupuesto en la campaña, repartido entre conjuntos |
| Presupuesto por conjunto | Ad set budget (ABO) | Presupuesto fijo en cada conjunto |
| Conjunto de datos / Píxel | Dataset / Pixel | La medición del sitio y del servidor |
| Administrador de eventos | Events Manager | Donde se ven y configuran los eventos del píxel |
| Calidad de la cuenta | Account Quality | Rechazos, restricciones y apelaciones |
| Biblioteca de anuncios | Ad Library | Buscador público de anuncios activos de cualquier página |

## Objetivos y optimización

| ES | EN | Qué es |
| --- | --- | --- |
| Reconocimiento · Tráfico · Interacción · Clientes potenciales · Promoción de la app · Ventas | Awareness · Traffic · Engagement · Leads · App promotion · Sales | Los seis objetivos (ODAX) |
| Evento de conversión / de optimización | Optimization event | La acción a la que se optimiza el conjunto (Lead, Compra…) |
| Fase de aprendizaje | Learning phase | Primeros ~50 resultados por conjunto; el costo es inestable |
| Aprendizaje limitado | Learning limited | No llegó a 50 resultados en 7 días; rinde peor |
| Estrategia de puja | Bid strategy | Menor costo (default), límite de costo, límite de puja, ROAS mínimo |
| Ventana de atribución | Attribution window | 7 días clic / 1 día vista por defecto |
| Campaña Advantage+ de ventas / de clientes potenciales | Advantage+ sales / leads campaign | Campaña casi totalmente automática; pide creativos y datos |
| Audiencia Advantage+ | Advantage+ audience | Meta amplía la audiencia más allá de lo que definiste |

## Audiencias

| ES | EN | Qué es |
| --- | --- | --- |
| Segmentación detallada | Detailed targeting | Intereses, comportamientos, datos demográficos |
| Audiencia personalizada | Custom audience | Gente que ya interactuó: sitio, lista, video, página, formulario |
| Audiencia similar | Lookalike audience | Parecidos a una personalizada (1% a 10%) |
| Exclusión | Exclusion | Gente a la que no se le muestra |
| Personas que viven en / que están en | People living in / recently in | Residentes vs. presentes en el lugar |

## Creativos y formatos

| ES | EN | Qué es |
| --- | --- | --- |
| Texto principal · Título · Descripción | Primary text · Headline · Description | Los tres campos de texto del anuncio |
| Llamado a la acción | Call to action (CTA) | El botón |
| Secuencia | Carousel | Varias tarjetas deslizables |
| Colección | Collection | Portada + catálogo |
| Creativo Advantage+ | Advantage+ creative | Mejoras automáticas (recortes, música, texto) |
| Anuncio flexible / varias versiones | Flexible ad / multiple text options | Varias imágenes o textos en un anuncio; Meta combina |
| Formulario instantáneo | Instant form | Formulario de leads dentro de Meta |
| Anuncios que dirigen a WhatsApp | Click-to-WhatsApp ads | El botón abre un chat |
| Contenido generado por usuarios | UGC | Video tipo testimonio grabado por un cliente |
| Gancho | Hook | Primeros 2-3 segundos del video |

## Métricas

| ES | EN | Qué es |
| --- | --- | --- |
| Costo por resultado | Cost per result | Gasto ÷ resultados del objetivo |
| CPM | CPM | Costo por mil impresiones |
| CTR (clics en el enlace) | Link CTR | Clics al destino ÷ impresiones |
| CPC (clics en el enlace) | Link CPC | Gasto ÷ clics al destino |
| Frecuencia | Frequency | Impresiones ÷ personas alcanzadas |
| Alcance | Reach | Personas distintas que vieron el anuncio |
| Reproducciones de 3 segundos / ThruPlay | 3-second plays / ThruPlay | Cuántos empezaron a ver / cuántos vieron 15 s o el total |
| Tasa de retención / gancho | Hook rate | Reproducciones de 3 s ÷ impresiones |
| Valor de conversión de compras / ROAS | Purchase conversion value / ROAS | Ventas atribuidas ÷ gasto |
| Calidad de coincidencia de eventos | Event Match Quality (EMQ) | Cuántos datos del usuario manda cada evento (0-10) |
| Clientes potenciales | Leads | Resultados de formulario, sitio, llamada o mensaje |
| Conversaciones iniciadas | Messaging conversations started | Chats nuevos por WhatsApp/Messenger/Instagram |

## Técnico

| ES | EN | Qué es |
| --- | --- | --- |
| API de conversiones | Conversions API (CAPI) | Eventos mandados desde el servidor |
| Deduplicación | Deduplication | Mismo evento por píxel y CAPI con el mismo `event_id`, contado una vez |
| Verificación del dominio | Domain verification | Prueba de que el dominio es del cliente |
| Usuario del sistema | System user | Usuario técnico del Portfolio para tokens de la API |
| Token de acceso | Access token | Credencial de la Marketing API (secreto, nunca al vault) |
| Parámetros de URL / UTM | URL parameters / UTM | Etiquetas en el enlace para saber de dónde vino la visita |
| Categoría de anuncios especial | Special ad category | Crédito, empleo, vivienda, temas sociales: segmentación restringida |
