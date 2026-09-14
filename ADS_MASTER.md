---
tags:
  - innova
  - ads
  - master
  - nivel-0
updated: 2026-09-14
---

# 📣 INNOVA ADS

> Unidad de publicidad digital de Innova Solutions. Arranca con **Meta Ads** (Facebook + Instagram + Messenger + WhatsApp) gestionado para clientes. Hermano del vault `obsidian_innova` (webs y automatización): mismas convenciones, mismo equipo.

---

## Qué vendemos

Gestión de campañas en Meta para PyMEs argentinas que necesitan **leads o ventas medibles**, no "presencia". Cada cliente recibe: estrategia, estructura de cuenta, creativos, optimización semanal y un reporte que entiende sin traductor.

> [!info] Dónde se cruza con Innova
> Un lead que entra por Meta necesita que alguien lo atienda rápido. Ahí entra la automatización de Innova (n8n, WhatsApp API, CRM). Ver [[meta/automatizaciones|Automatizaciones]] para los flujos que conectan pauta con atención.

---

## Stack

| Herramienta | Rol |
| --- | --- |
| **Meta Business Suite / Ads Manager** | Cuentas publicitarias, campañas, facturación |
| **Business Manager (Portfolio)** | Acceso como *partner* a las cuentas del cliente, nunca con su usuario |
| **Píxel + Conversions API** | Medición en el sitio y del lado del servidor |
| **Meta Lead Ads + WhatsApp** | Captura de leads sin sitio, click-to-WhatsApp |
| **Google Sheets / Looker Studio** | Reportes al cliente |
| **n8n (Innova)** | Reporte automático, alertas de CPL, aviso de lead nuevo |
| **Canva / CapCut** | Producción de creativos estáticos y video corto |
| **GitHub** | Este vault, versionado |

---

## Modelo de negocio

> [!warning] A definir por Francisco
> Propuesta inicial, para discutir antes de la primera cotización. Ver detalle en [[clientes/clientes|Clientes]].

- **Setup inicial** (una vez): auditoría de cuenta, píxel/CAPI, estructura, primeros creativos.
- **Fee mensual** de gestión, con un mínimo.
- **Pauta**: la paga el cliente **directo a Meta con su tarjeta**, desde su propia cuenta publicitaria. Innova nunca intermedia la plata de la pauta.
- Cobro por deliverable, como en Innova: 50% al confirmar, 50% contra entrega del setup.

---

## Workflow por cliente

> [!example] Las 7 fases
> **1. Brief** → qué vende, a quién, cuánto vale un cliente, qué pasó antes con pauta
> **2. Accesos y setup técnico** → partner en el Business Manager, píxel + CAPI, dominio verificado, método de pago
> **3. Estrategia y plan** → objetivo, embudo, audiencias, presupuesto, KPIs y umbrales
> **4. Creativos** → mínimo 3 ángulos × 2 formatos antes de lanzar
> **5. Lanzamiento** → checklist, fase de aprendizaje, primera semana sin tocar
> **6. Optimización** → ciclo semanal: apagar, escalar, rotar creativos
> **7. Reporte y renovación** → mensual, con decisión: seguir, escalar o cortar

---

## Meta Ads — base de conocimiento

→ Ver [[meta/README|Meta Ads KB]] (metodología por campaña, playbooks, roster de clientes, cockpit)

---

## Clientes

→ Ver [[clientes/clientes|Clientes]] (hub con la cartera)

| Cliente | Objetivo | Estado | Fase |
| --- | --- | --- | --- |
| Innova (interno) | ⚙️ Leads por WhatsApp para agentes de IA | 🟡 Planificada | 3 |

---

## Workflows operativos

→ Ver [[workflows/workflows|Workflows]] (onboarding, lanzamiento, ciclo semanal, reporte mensual)

---

## Research

→ Ver [[research/research|Research]] (cambios de plataforma, novedades de Meta, benchmarks)

---

## Reuniones

→ Ver [[reuniones/reuniones|Reuniones]]

---

## Pendientes globales

- [ ] Validar la hoja de precios borrador (`clientes/precios.md`)
- [ ] Crear el Business Manager de Innova Ads (o usar el de Innova) y verificarlo
- [x] Armar 1 caso propio: campaña de Innova planificada en `meta/clientes/innova/` (2026-09-14) → falta lanzarla
- [ ] Definir la plantilla de reporte que ve el cliente (Sheet o Looker)
- [ ] Que el contador/abogado revise `meta/templates/acuerdo-de-gestion.md` antes del primer cliente
