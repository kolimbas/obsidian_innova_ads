---
tags:
  - innova
  - ads
  - clientes
  - hub
  - nivel-1
updated: 2026-09-14
---

# 👥 Clientes

> Hub comercial de Innova Ads. Una ficha por cliente: quién es, qué vende, cuánto paga, en qué fase está.

← Volver a [[ADS_MASTER]]

---

## Cartera actual

| Cliente | Objetivo | Estado | Fase | Pauta mensual |
| --- | --- | --- | --- | --- |
| *(todavía ninguno)* | | | | |

Estados posibles: 🔵 Pre-venta · 🟡 Setup · 🟢 Activo · ⏸️ Pausado · ⚫ Cerrado.

---

## Cómo se cotiza (propuesta inicial, a validar)

> [!warning] Números orientativos para arrancar la conversación
> Francisco define los finales. La idea es cobrar por lo que Innova hace, no por lo que gasta el cliente en Meta.

| Concepto | Qué incluye | Referencia |
| --- | --- | --- |
| **Setup** (una vez) | Auditoría de cuenta, píxel + CAPI, verificación de dominio, estructura, brief, primeros 6 creativos, lanzamiento | Equivalente a 1 fee mensual |
| **Fee mensual** | Optimización semanal, rotación de creativos, reporte mensual, reunión de status | Mínimo fijo en USD; por encima de cierta pauta, un % del gasto |
| **Pauta** | La paga el cliente directo a Meta desde su cuenta | Mínimo recomendado para que haya datos: ver [[meta/playbooks/presupuesto-y-escalado|presupuesto]] |
| **Extras** | Producción de video, landing, automatización de leads (Innova) | Se cotizan aparte |

Cobro: 50% del setup al confirmar, 50% contra lanzamiento. Fee mensual por adelantado. Conversión a pesos con el dólar blue de dolarhoy.com del día.

---

## Cómo usar este hub

- Cada cliente nuevo: una fila en la tabla, una ficha en `clientes/<slug>.md` (plantilla en `meta/templates/ficha-cliente.md`) y una carpeta operativa en `meta/clientes/<slug>/`.
- La ficha lleva frontmatter con `estado`, `fase` y `updated`.
- El alta completa está en [[workflows/onboarding-cliente-ads|Onboarding de cliente]].
