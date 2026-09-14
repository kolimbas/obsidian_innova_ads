---
tags:
  - meta
  - n8n
  - automatizaciones
  - nivel-2
updated: 2026-09-14
---

# ⚙️ Automatizaciones alrededor de la pauta

> Dónde Innova Ads se conecta con Innova (n8n). La pauta trae el lead; estos flujos hacen que no se enfríe y que el cliente vea qué pasa sin pedirlo.

← Volver a [[meta/README|Meta Ads KB]]

---

## Regla

Los flujos n8n **se construyen y documentan en el vault innova** (`n8n/clients/<cliente>/flows/`) con su Spec Kit. Acá solo se listan y se linkea el bundle. Un cliente de Ads que necesita automatización es también un cliente de Innova, con su carpeta allá.

---

## Catálogo de flujos candidatos

| Flujo | Qué hace | Disparador | Estado |
| --- | --- | --- | --- |
| **Lead nuevo → WhatsApp/CRM** | Cuando entra un lead por formulario instantáneo de Meta, lo manda al WhatsApp del vendedor y lo carga en el CRM o Sheet del cliente en menos de 1 minuto. Es el que más vende: un lead atendido en 5 minutos vale varias veces más que uno atendido a la tarde. | Webhook de Meta Lead Ads (Leadgen) | 🔲 sin construir |
| **Reporte semanal automático** | Baja las métricas de la cuenta por la Marketing API (gasto, resultados, CPL/CPA, frecuencia) a un Sheet y arma el mail de lunes al cliente. | Cron lunes 08:00 | 🔲 sin construir |
| **Alerta de CPL** | Si el CPL del día supera el umbral del `plan.md` por 2 días seguidos, avisa por Telegram a Innova. No toca la campaña. | Cron diario | 🔲 sin construir |
| **Alerta de cuenta** | Anuncio rechazado, cuenta restringida, método de pago fallido: aviso inmediato. | Marketing API / mail de Meta | 🔲 sin construir |
| **Respuesta inicial en WhatsApp** | Para campañas click-to-WhatsApp: primera respuesta automática en segundos con las 2-3 preguntas de calificación; después sigue una persona. Reusa lo hecho para Alpha Cycles y Hernando Ventas. | Mensaje entrante (WhatsApp Cloud API) | 🔲 sin construir |
| **Audiencia de clientes → Meta** | Sube la lista de clientes actuales como audiencia personalizada (hasheada) para excluirlos o hacer similares. | Cron semanal | 🔲 sin construir |

---

## Qué necesita cada uno

- **Token de sistema** de la Marketing API desde el Business Manager de Innova, con permisos `ads_read` (reportes) y `leads_retrieval` (leads). Guardado en `~/.config/innova/ads-<cliente>.env`, nunca en el vault.
- Para leads: la página del cliente tiene que dar acceso a la app de Innova y aceptar el webhook. Se hace una vez por cliente en el onboarding.
- Instancia n8n: la de Innova que corresponda (ver el vault innova).

---

## Ya construido en Innova que se reutiliza

- Bot de WhatsApp con calificación y agendado (Alpha Cycles, Hernando Ventas).
- Reportes por mail con link a Sheet vivo (auditorías de Nautilus).
- Alertas por Telegram (bot de pendientes de Innova).
