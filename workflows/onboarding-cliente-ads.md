---
tags:
  - workflow
  - onboarding
  - nivel-2
updated: 2026-09-14
---

# Onboarding de cliente de Ads

> Desde que dice que sí hasta que se puede lanzar. Objetivo: que el plazo comercial arranque con todo en la mano, no con promesas.

← Volver a [[workflows/workflows|Workflows]]

---

## 1. Comercial (día 0)

- [ ] Ficha en `clientes/<slug>.md` (plantilla `meta/templates/ficha-cliente.md`), con cobro, alcance, KPI y umbral.
- [ ] Fila en `clientes/clientes.md` y en `ADS_MASTER.md`.
- [ ] Cobro del 50% del setup.
- [ ] Mail de bienvenida con la lista de lo que necesitamos (punto 2 y 4) y por qué.

## 2. Accesos (día 0-3)

- [ ] Carpeta `meta/clientes/<slug>/` con `README.md`, `ACCESOS.md`, `campanas/`, `creativos/`, `reportes/`.
- [ ] Fila en `meta/clientes/_index.md`.
- [ ] El cliente tiene Portfolio empresarial a su nombre. Si no, se le crea uno **con su mail** en videollamada.
- [ ] Nos agrega como **socio** con acceso a: cuenta publicitaria, página, Instagram, píxel, WhatsApp. Guía en [[meta/playbooks/estructura-de-cuenta|Estructura de cuenta]].
- [ ] Segundo administrador del Portfolio del lado del cliente.
- [ ] Método de pago cargado por el cliente + límite de gasto de la cuenta.
- [ ] Token de usuario del sistema para la Marketing API (si va a haber reportes automáticos), guardado en `~/.config/innova/ads-<slug>.env`.

## 3. Técnico (día 2-5)

- [ ] Auditoría de la cuenta: campañas viejas, audiencias, píxel existente, Calidad de la cuenta, rechazos previos. Se anota en el README del cliente.
- [ ] Píxel + Conversions API instalados y verificados ([[meta/playbooks/pixel-y-capi|checklist]]).
- [ ] Dominio verificado.
- [ ] Audiencias personalizadas base: visitantes 30/90/180, interacción IG/FB 90, lista de clientes si hay.
- [ ] Si hay WhatsApp: cuenta de WhatsApp Business conectada a la página. Si hay bot o flujo n8n: bundle en el vault innova.
- [ ] Preset de columnas "Innova" en Ads Manager.
- [ ] Sheet de reporte creado y compartido con el cliente (solo lectura).

## 4. Brief y material (día 1-5, en paralelo)

- [ ] Reunión de brief (45 min) → `campanas/<primera>/brief.md`.
- [ ] Definición de lead válido acordada por escrito.
- [ ] Material para creativos: fotos, videos, testimonios, logo, colores. Carpeta en Drive.
- [ ] Preguntas abiertas cerradas con el cliente.

## 5. Listo para lanzar

- [ ] Plan y tasks confirmados por Francisco.
- [ ] Creativos aprobados por el cliente.
- [ ] Seguir [[workflows/lanzamiento-de-campana|Lanzamiento de campaña]].

---

> [!warning] El plazo arranca acá
> Cuando están los accesos (2), el método de pago y el material (4). Se le dice al cliente el día 0 para que no haya sorpresas.
