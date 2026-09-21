---
tags:
  - research
  - meta
  - capacitacion
  - nivel-2
updated: 2026-09-21
---

# 2026-09-21 — Capacitación: cómo se gestiona Meta Ads hoy

> Lo que cambió en la plataforma y lo que hoy separa a una cuenta bien llevada de una mal llevada, contrastado con fuentes de 2026. Cada regla dice de dónde sale. Lo que cambió un playbook está marcado con →.

← Volver a [[research/research|Research]]

---

## 1. Andromeda: el creativo es la segmentación

Meta reemplazó la etapa de *retrieval* del sistema de anuncios (qué anuncios entran a la subasta para cada persona) por un modelo neuronal miles de veces más complejo, llamado Andromeda. Lo que hace en la práctica: elige el anuncio por **coincidencia entre el contenido del creativo y la persona**, no por la audiencia que definió el anunciante.

Consecuencias verificadas en datos de terceros (Confect, dataset de 115.700 millones de impresiones y USD 834 millones de gasto):

- **Variaciones cosméticas cuentan como un solo anuncio.** Diez versiones del mismo concepto con otro título o recorte son "una entidad". Lo que suma son conceptos distintos: otro gancho, otro formato, otra propuesta de valor.
- **Amplio le gana a similares.** Datos de Lebesgue citados: targeting amplio rinde 49% más ROAS que audiencias similares bajo Andromeda.
- **Menos conjuntos, más creativos.** Un conjunto amplio con 25 creativos distintos dio 17% más conversiones a 16% menos costo que 5 conjuntos tradicionales.
- **La primera semana decide.** Un anuncio que no funcionó en la semana 1 rara vez mejora. Fatiga de estáticos: 2-3 semanas. Catálogo: 4-6 semanas.
- **Catálogo rinde más que estáticos:** +23% ROAS y -37% CPA en ese dataset; las cuentas con 60-100% del gasto en catálogo tienen +44% ROAS.

→ Playbooks *Creativos* y *Audiencias* actualizados: el mínimo pasa de "3 ángulos × 2 formatos" a **6-10 conceptos distintos por campaña**, con amplio por defecto y renovación cada 2-3 semanas. Nuevo playbook *Catálogo y anuncios dinámicos*.

## 2. Leads: calidad antes que volumen

De la guía de Lead Ads 2026 de adlibrary.com y de Meta:

- Formulario **"mayor intención"** siempre; **una sola pregunta de calificación**, no cinco.
- **Contactar en menos de 5 minutos convierte ~9× más** que después de una hora. Un mensaje automático al instante sube la conversión posterior 30-40%.
- Umbral de aprendizaje: 50 conversiones por conjunto por semana.
- La métrica que importa no vive en Ads Manager: **costo por lead calificado = CPL × tasa de descalificación**, y lead → reunión → cierre por conjunto, medido en el CRM.
- Meta permite optimizar a **leads de conversión**: se le devuelven a Meta los estados del CRM (calificado, reunión, cierre) vía Conversions API y optimiza a eso, no al envío del formulario.
- CPL orientativos 2026 (envíos sin calificar, mercados caros): servicios al hogar €8-30, e-commerce €2-10, servicios financieros €25-120, inmobiliario €12-40. Los calificados cuestan 2-4× más.

→ Playbook *WhatsApp y leads* actualizado (una pregunta, 5 minutos, leads de conversión).

## 3. Click-to-WhatsApp: el canal de Argentina

- Objetivo: **Interacción** con WhatsApp como destino, o **Clientes potenciales** con conversión de mensajería. **Nunca Tráfico** (optimiza clics, trae curiosos).
- Evento: *conversaciones de mensajería iniciadas*.
- Requisito: la cuenta de WhatsApp Business **vinculada al Portfolio empresarial y a la página**.
- Mensaje precargado específico y botones de respuesta rápida (máximo 3).
- **Ventana gratuita:** cuando alguien escribe desde un anuncio se abre una ventana de 24 h; si el negocio responde dentro, se extiende a **72 h en las que todo mensaje es gratis** (documentación oficial de Meta).
- Respuesta en menos de 5 minutos; con más de 50 conversaciones por semana, automatizar es obligatorio.
- Presupuesto: USD 20-50/día da datos en 5-7 días; no tocar 7 días.
- Cobro de WhatsApp desde julio de 2025: **por mensaje de plantilla entregado**, según categoría (marketing, utilidad, autenticación) y país. Los mensajes libres dentro de una ventana abierta no se cobran. Argentina, marketing: ~USD 0,06 por mensaje. Meta anunció cambios de tarifas para el 1 de octubre de 2026; confirmar en la tabla oficial antes de cotizar.

→ Playbooks *Objetivos* y *WhatsApp y leads* actualizados.

## 4. Concesionarias: anuncios de inventario

De Meta y de guías de concesionarias 2026:

- **Automotive Inventory Ads (AIA):** catálogo de vehículos (CSV/TSV/XML con VIN, marca, modelo, año, precio, kilometraje, fotos, disponibilidad) + píxel con eventos de vehículo + Conversions API. Meta muestra a cada persona el vehículo que miró o uno parecido.
- Caso Meta (Rusnak Auto Group): AIA + audiencia ampliada dio **44% más leads y 29% menos CPL**.
- Estructura: 40% prospección, 30% consideración, 30% acción. Radio de 15-30 millas. USD 50-100/día por conjunto. Mínimo realista: **USD 1.500-3.000/mes**; resultados consistentes en USD 5.000-10.000.
- Similares: Meta pide 1.000-5.000 registros de CRM.
- Cumplimiento en EE. UU.: la FTC mandó cartas de advertencia a 97 grupos de concesionarias en marzo de 2026 por precios y cargos no transparentes. Precio anunciado = precio real.
- CPM en EE. UU. 2025: ~USD 14 (Triple Whale), 20% más que 2024.

→ Nuevo playbook *Catálogo y anuncios dinámicos*. Aplica directo a Alpha Cycles.

## 5. Suplementos y salud: la política cambió el 22-07-2026

Meta reescribió sus normas de salud y bienestar (política oficial, actualizada el 22 de julio de 2026):

- Pasó de prohibir por **tipo de producto** a prohibir por **afirmación**. Antes/después ya no se rechaza automáticamente; lo que se rechaza es la promesa médica.
- Prohibido: curar enfermedades, resultados en un plazo sin aclaración, primeros planos "pellizcando grasa", afirmaciones negativas sobre el cuerpo, blanqueamiento de piel permanente.
- **Solo 18+:** productos de dieta, pérdida o ganancia de peso, procedimientos cosméticos. Suplementos generales sin promesa de peso: sin restricción de edad.
- Suplementos: "apoya la energía en el entrenamiento" pasa; "cura la fatiga crónica" no. Claims cognitivos, hormonales e inmunes son zona gris. Los testimonios (UGC) tienen las mismas reglas: "me arregló la ansiedad" es claim médico.
- ROAS esperable en suplementos: 1,4-2,1× el primer mes, 2,8-3,6× al sexto con recompra. Decidir a 7-14 días.

→ Playbook *Políticas y rechazos* actualizado. Aplica a Altius Nutrition (N+ FOCUS CODE es claim cognitivo: cuidado con el copy).

## 6. Argentina: números de referencia

- CPM promedio agosto 2026: **ARS 2.871**; CPC: **ARS 129** (Web360, cuentas reales). Con inflación, el número caduca; el método no.
- Presupuesto diario mínimo que acepta una cuenta argentina: **ARS 1.504/día** (agosto 2026).
- Global 2026: CPM ~USD 14, CPC ~USD 0,78, CTR 1,5-2,2%, CPL ~USD 28 en leads. Argentina es 5-7× más barata en CPM que EE. UU.

→ Playbook *Métricas* actualizado con estas referencias.

## 7. Herramientas de IA

Ver playbook *Herramientas de IA* (Juan, 14-09): conector oficial de Meta Ads para Claude, 29 herramientas, lo que crea queda pausado. Uso: lectura semanal y borrador del reporte; no decide.

---

## Fuentes

- [Meta Andromeda, guía 2026 — Confect](https://confect.io/tactics/meta-andromeda-2026)
- [Meta Lead Ads Guide 2026 — adlibrary.com](https://adlibrary.com/posts/meta-lead-ads-guide-2026)
- [Click-to-WhatsApp Ads 2026 — adlibrary.com](https://adlibrary.com/posts/meta-click-to-whatsapp-ads-guide)
- [Precios de la plataforma de WhatsApp Business — Meta for Developers](https://developers.facebook.com/documentation/business-messaging/whatsapp/pricing)
- [Facebook Ads para concesionarias 2026 — The Fractional CMO Team](https://www.thefractionalcmoteam.com/feeds/blog/car-dealership-facebook-ads)
- [Salud y bienestar — Normas de anuncios de Meta (22-07-2026)](https://transparency.meta.com/policies/ad-standards/restricted-goods-services/health-wellness/)
- [Meta Ads para marcas de suplementos 2026 — Landing Partners](https://www.landing.partners/blog/meta-ads-supplement-brands-vitamins-advertising-policy)
- [Cuánto cuesta publicidad en Instagram en Argentina 2026 — Web360](https://web360.com/blog/marketing-digital/cuanto-cuesta-publicidad-instagram-argentina-2026/)
- [Meta Ads benchmarks 2026 — ContentStudio](https://contentstudio.io/blog/meta-ads-benchmarks)
- [Meta Ads y WhatsApp para agencias 2026 — WP Reset](https://wpreset.com/meta-ads-whatsapp-lead-generation-best-practices-for-agencies-in-2026-from-click-to-chat-campaigns-to-qualified-leads/)
