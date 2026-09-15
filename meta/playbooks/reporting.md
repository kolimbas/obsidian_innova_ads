---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-14
---

# Reporting

> El cliente tiene que poder contestar en 30 segundos: ¿cuánto gasté, cuánto conseguí, a qué costo, y qué van a hacer ustedes esta semana? Todo lo demás va después, si lo pide.

← Volver a [[meta/playbooks/_index|Playbooks]]

---

## Cadencia

| Cuándo | Qué | Formato |
| --- | --- | --- |
| **Lunes** | Semana anterior: gasto, resultados, costo por resultado vs. umbral, tendencia, qué hicimos, qué hacemos | Mail de 5-8 líneas + link al Sheet vivo. Plantilla en plantilla `reporte-semanal`. |
| **Mensual** | Lo mismo acumulado + creativos ganadores + decisión (seguir, escalar, replantear) | Reunión de 30 min con el Sheet en pantalla. |
| **Cuando pasa algo** | Cuenta restringida, campaña apagada por costo, oportunidad | Mensaje el mismo día. |

Automatizar lo del lunes es el primer flujo n8n que se construye para un cliente de Ads (ver *Automatizaciones* (`meta/automatizaciones`)).

---

## Qué va y qué no

**Va, en este orden:** gasto · resultados · costo por resultado · vs. umbral acordado · comparación con la semana anterior · qué se decidió y por qué · qué viene.

**No va al frente:** impresiones, alcance, "engagement", likes. Si el cliente los pide, van al final del Sheet. Reportar alcance como logro es la forma más rápida de que el cliente crea que la pauta no sirve el día que mire su caja.

**Siempre se aclara:** los números son de Ads Manager con atribución 7 días clic / 1 día vista. Lo que el cliente cobró es el número que manda; si tiene CRM o registro de ventas, se cruza y se reporta la conversión real de lead a cliente.

---

## UTMs

Todos los anuncios llevan parámetros de URL con los valores dinámicos de Meta, cargados en el campo "Parámetros de URL" del anuncio:

```
utm_source=meta&utm_medium=paid_social&utm_campaign={{campaign.name}}&utm_content={{ad.name}}&utm_term={{adset.name}}&placement={{placement}}
```

Así Google Analytics y el CRM del cliente ven de qué campaña y anuncio vino cada visita, sin cargar nada a mano. Con los nombres estandarizados de playbook *Estructura de cuenta*, los reportes se leen solos.

---

## El Sheet de reporte

Una pestaña por cliente en un Sheet compartido de solo lectura con el cliente:

| Semana | Gasto | Resultados | Costo/resultado | Umbral | CPM | CTR enlace | Frecuencia | Notas |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

Y una pestaña "Decisiones" con fecha, qué se cambió y por qué (copia de lo que va en `resultados.md`). El cliente que puede leer las decisiones confía más y pregunta menos.

---

## Looker Studio

Solo si el cliente lo pide o paga más de cierto nivel. El conector nativo de Meta a Looker es de terceros y suele ser pago; para PyMEs el Sheet alcanza y se entiende mejor.
