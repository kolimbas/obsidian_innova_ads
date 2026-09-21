---
tags:
  - innova
  - ads
  - clientes
  - hub
  - nivel-1
updated: 2026-09-21
---

# 👥 Clientes

> Hub comercial de Innova Ads. Una ficha por cliente: quién es, qué vende, cuánto paga, en qué fase está.

← Volver a [[ADS_MASTER]]

---

## Cartera actual

| Cliente | Objetivo | Estado | Fase | Pauta mensual |
| --- | --- | --- | --- | --- |
| [[clientes/alpha-cycles\|Alpha Cycles]] | Leads de motos en Miami → bandeja única | 🔵 Pre-venta · prioridad 1 | 0 | USD 1.500-3.000 |
| [[clientes/hernando-ventas\|Hernando Ventas]] | Leads de dueños de tiendas online → motor de WhatsApp | 🔵 Pre-venta · prioridad 2 | 0 | USD 300-600 |
| [[clientes/don-blanco\|Don Blanco]] | Encargos por WhatsApp · Día de la Madre | 🔵 Pre-venta · prioridad 3 (urgente) | 0 | USD 150-300 por fecha |
| [[clientes/altius-nutrition\|Altius Nutrition]] | Ventas de suplementos en Tiendanube | 🔵 Pre-venta · bloqueado (tienda cerrada) | 0 | USD 600-900 |
| [[clientes/innova\|Innova (interno)]] | Caso propio | ⏸️ En pausa (foco en clientes) | 3 | — |

Estados posibles: 🔵 Pre-venta · 🟡 Setup · 🟢 Activo · ⏸️ Pausado · ⚫ Cerrado.

### Orden de ataque (21-09-2026)

1. **Don Blanco** primero por calendario: Día de la Madre es el 18-10; el pitch tiene que salir esta semana para lanzar el 6-8 de octubre.
2. **Alpha Cycles**: la pauta era la fase 2 anunciada en el contrato; se propone ahora y se lanza cuando el Módulo 1 esté en producción.
3. **Hernando Ventas**: se propone ahora; se lanza la semana del 20-10, cuando ella pueda atender reuniones.
4. **Altius**: se propone "para el día que abra la tienda"; hoy está cerrada con contraseña.

Siguientes candidatos: Trujillo Abogados (consultas por WhatsApp; falta el contacto) y GPT Landings (crédito: categoría especial de Meta, segmentación restringida).

Ningún cliente actual lleva anuncios de catálogo ni dinámicos: campañas estándar con el material que ya tienen.

---

## Cómo se cotiza

Hoja de precios borrador: [[clientes/precios|precios]]. Lo que recibe el cliente: plantilla de plantilla `propuesta-comercial` y plantilla `acuerdo-de-gestion`.

### Resumen (propuesta inicial, a validar)

> [!warning] Números orientativos para arrancar la conversación
> Francisco define los finales. La idea es cobrar por lo que Innova hace, no por lo que gasta el cliente en Meta.

| Concepto | Qué incluye | Referencia |
| --- | --- | --- |
| **Setup** (una vez) | Auditoría de cuenta, píxel + CAPI, verificación de dominio, estructura, brief, primeros 6 creativos, lanzamiento | Equivalente a 1 fee mensual |
| **Fee mensual** | Optimización semanal, rotación de creativos, reporte mensual, reunión de status | Mínimo fijo en USD; por encima de cierta pauta, un % del gasto |
| **Pauta** | La paga el cliente directo a Meta desde su cuenta | Mínimo recomendado para que haya datos: ver playbook *Presupuesto y escalado* |
| **Extras** | Producción de video, landing, automatización de leads (Innova) | Se cotizan aparte |

Cobro: 50% del setup al confirmar, 50% contra lanzamiento. Fee mensual por adelantado. Conversión a pesos con el dólar blue de dolarhoy.com del día.

---

## Cómo usar este hub

- Cada cliente nuevo: una fila en la tabla, una ficha en `clientes/<slug>.md` (plantilla en `meta/templates/ficha-cliente.md`) y una carpeta operativa en `meta/clientes/<slug>/`.
- La ficha lleva frontmatter con `estado`, `fase` y `updated`.
- El alta completa está en workflow *Onboarding de cliente*.
