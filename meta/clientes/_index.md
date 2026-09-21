---
tags:
  - meta
  - clients
  - hub
  - nivel-2
updated: 2026-09-21
---

# Clientes — operación de Meta Ads

> Una carpeta por cliente. Adentro: `README.md` con el contexto operativo, `ACCESOS-PUNTERO.md` con punteros (nunca claves), y `campanas/`, `creativos/`, `reportes/`.

← Volver a [[meta/README|Meta Ads KB]]

---

## Roster

| Cliente | Estado | Campañas activas | Pauta/mes | Notas |
| --- | --- | --- | --- | --- |
| [[meta/clientes/alpha-cycles/README\|Alpha Cycles]] | onboarding | 0 | USD 1.500-3.000 | Miami · leads a la bandeja única (A01-A03) · sin píxel · BM pendiente (mismo trámite que WhatsApp) · lanzar cuando el Módulo 1 esté en producción (2026-09-21) |
| [[meta/clientes/hernando-ventas/README\|Hernando Ventas]] | onboarding | 0 | USD 300-600 | Formulario → planilla → motor de WhatsApp que ya existe · sin página FB confirmada, sin píxel · lanzar semana del 20-10 (2026-09-21) |
| [[meta/clientes/don-blanco/README\|Don Blanco]] | onboarding | 0 | USD 150-300 por fecha | Encargos por WhatsApp, un conjunto por sucursal · Día de la Madre 18-10 → lanzar 6-8 de octubre (2026-09-21) |
| [[meta/clientes/altius-nutrition/README\|Altius Nutrition]] | onboarding | 0 | USD 600-900 | Ventas en Tiendanube · **tienda cerrada con contraseña** · política de salud 22-07-2026 (2026-09-21) |
| [[meta/clientes/innova/README\|Innova (interno)]] | pausado | 0 | — | Caso propio en pausa: foco en clientes (2026-09-21) |

> La ficha comercial (contacto, cobro, alcance) vive en `clientes/`. Este índice solo sigue a los clientes con pauta.

Estados: `onboarding` · `setup` · `activo` · `pausado` · `cerrado`.

---

## Cómo se da de alta un cliente acá

1. Crear `meta/clientes/<slug>/` con `campanas/`, `creativos/`, `reportes/`.
2. Copiar `meta/templates/cliente-README.md` como `README.md` y completarlo.
3. Copiar `meta/templates/ACCESOS-PUNTERO.md` como `ACCESOS-PUNTERO.md`: solo dónde vive cada acceso.
4. Agregar la fila arriba.
5. Seguir workflow *el onboarding* para lo técnico (partner, píxel, dominio, pago).
