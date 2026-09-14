---
tags:
  - meta
  - cockpit
  - dataview
  - nivel-2
updated: 2026-09-14
---

# 🎛️ Cockpit

> Vista viva del estado operativo. Requiere el plugin Dataview (ya instalado). Si una tabla sale vacía es porque todavía no hay campañas cargadas.

← Volver a [[meta/README|Meta Ads KB]]

---

## Campañas activas

```dataview
TABLE client AS Cliente, objetivo AS Objetivo, presupuesto_diario AS "Pauta/día", inicio AS Inicio, updated AS Actualizada
FROM "meta/clientes"
WHERE status = "activa" AND file.name = "brief"
SORT client ASC
```

## Campañas en preparación

```dataview
TABLE client AS Cliente, status AS Estado, objetivo AS Objetivo, updated AS Actualizada
FROM "meta/clientes"
WHERE (status = "brief" OR status = "planificada") AND file.name = "brief"
SORT updated DESC
```

## Pausadas o cerradas (últimas 10)

```dataview
TABLE client AS Cliente, status AS Estado, fin AS Fin
FROM "meta/clientes"
WHERE (status = "pausada" OR status = "cerrada") AND file.name = "brief"
SORT fin DESC
LIMIT 10
```

---

## Tareas abiertas por cliente

```dataview
TASK
FROM "meta/clientes"
WHERE !completed
GROUP BY file.folder
```

---

## Clientes por fase

```dataview
TABLE estado AS Estado, fase AS Fase, updated AS Actualizada
FROM "clientes"
WHERE estado
SORT fase DESC
```

---

## Notas sin actualizar hace más de 30 días

```dataview
TABLE updated AS Actualizada
FROM "meta/clientes"
WHERE updated AND updated < date(today) - dur(30 days)
SORT updated ASC
```
