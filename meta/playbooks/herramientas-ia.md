---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-14
---

# Herramientas de IA (Claude)

> Nace antes de un retro real, por decisión explícita — normalmente un playbook sale de una lección con más de un cliente encima, y acá todavía no hay ninguno. Se corrige o se descarta apenas haya una cuenta real probándolo. Fuentes y contexto en research del 14-09 (`research/2026-09-14`).

← Volver a [[meta/playbooks/_index|Playbooks]]

---

## Conector oficial de Meta Ads para Claude

Meta tiene un conector oficial (MCP, `https://mcp.facebook.com/ads`) que deja leer y operar una cuenta de Meta Ads desde Claude en lenguaje natural, sin credenciales de developer. 29 herramientas: reporting, campañas (crear/pausar/presupuestos), catálogo, diagnóstico de señales (píxel, CAPI, EMQ).

**Setup** (por cuenta, ~90 segundos): Claude → *Customize* → *Add custom connector* → URL `https://mcp.facebook.com/ads` → login con Facebook → elegir el Business Portfolio → activar el conector en el chat.

## Regla dura: un Claude Project por cliente

Nunca un solo conector compartido entre cuentas de distintos clientes. Un Project de Claude por cliente, igual que una carpeta por cliente en `meta/clientes/`. Evita que una pregunta sobre un cliente traiga de contexto datos de otro.

## Para qué sirve hoy

- **Ciclo semanal, paso "Leer"** (workflow *Ciclo semanal*): pedirle el diagnóstico CPM → CTR → conversión de la semana antes de la lectura manual, y contrastarlo.
- **Reporte del lunes**: armar el primer borrador del mail con los números de la API, para editar y no redactar de cero.
- **Auditoría de onboarding**: primera lectura de una cuenta nueva (campañas viejas, píxel, Calidad de la cuenta) en minutos en vez de horas.

## Para qué NO sirve (no confundir con criterio)

- **No genera creativos.** No ve imágenes ni video, solo texto. La revisión de piezas sigue siendo 100% humana — ver playbook *Creativos*.
- **Puede alucinar un número** si el prompt no dice ventana de tiempo, métrica exacta o filtro. Regla: pedirle siempre que muestre qué filtro usó, y cruzar contra Ads Manager antes de mandarle algo al cliente.
- **No diagnostica causa real** (no ve competencia, estacionalidad ni contexto de negocio). Una respuesta tipo "¿por qué bajó el ROAS?" es una hipótesis para revisar, no una conclusión para actuar.
- **No reemplaza el plan confirmado.** Que lo que crea quede pausado por default no es una licencia para saltear `brief.md` → `plan.md` → `tasks.md`; sigue siendo la misma regla dura de *Metodología* (`meta/METODOLOGIA`).

## Camino alternativo: n8n + Marketing API + Claude

Para lo que el conector no cubre (triggers automáticos, integración con el Sheet o CRM del cliente): un flujo n8n propio que llama a la API de Claude, con aprobación humana antes de tocar presupuesto o audiencias. Ver el flujo candidato "Diagnóstico asistido con Claude" en *Automatizaciones* (`meta/automatizaciones`).

## Riesgos si esto se ofrece a un cliente

- Acuerdo explícito sobre qué puede leer/tocar la IA en su cuenta, y quién responde si una recomendación ejecutada sale mal.
- El conector oficial es de menor riesgo que scraping o browser automation de terceros — pero sigue siendo la cuenta del cliente. Se prueba primero en una cuenta propia o de bajo riesgo antes de ofrecerlo como parte del servicio.
