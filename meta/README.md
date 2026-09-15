---
tags:
  - meta
  - ads
  - hub
  - nivel-1
updated: 2026-09-14
---

# 📘 Meta Ads KB

> Base operativa de Meta Ads de Innova. Todo lo que se aprende gestionando cuentas se guarda acá para que la segunda campaña sea más barata que la primera.

← Volver a [[ADS_MASTER]]
---

## Mapa

| Sección | Qué hay |
| --- | --- |
| [[meta/METODOLOGIA\|Metodología]] | Spec Kit por campaña: brief → research → plan → tasks → resultados → retro. Regla dura: nada se lanza sin plan confirmado. |
| [[meta/playbooks/_index\|Playbooks]] | Conocimiento reutilizable de la plataforma: estructura, objetivos, audiencias, píxel, creativos, métricas, presupuesto, testing, políticas, reporting, WhatsApp. |
| [[meta/clientes/_index\|Clientes]] | Roster operativo. Una carpeta por cliente con campañas, creativos y reportes. |
| [[meta/COCKPIT\|Cockpit]] | Vista viva (Dataview): campañas por estado, tareas abiertas, reportes pendientes. |
| [[meta/lecciones\|Lecciones]] | Una línea por cosa aprendida, con fecha y cliente. |
| [[meta/automatizaciones\|Automatizaciones]] | Los flujos n8n que conectan la pauta con la atención del lead y el reporte. Puente con el vault innova. |

---

## Cómo está organizado un cliente

```
meta/clientes/<slug>/
├── README.md              contexto operativo: cuenta, píxel, embudo, KPIs, umbrales
├── ACCESOS-PUNTERO.md     dónde viven las claves (nunca las claves)
├── campanas/
│   └── YYYY-MM-<slug>/    brief · research · plan · tasks · resultados · retro
├── creativos/             una nota por pieza o por tanda, con qué se probó y qué pasó
└── reportes/              semanal (YYYY-Www) y mensual (YYYY-MM)
```

---

## Principios que ordenan todo

1. **El cliente compra resultados, no impresiones.** Cada campaña tiene un KPI principal (CPL, CPA o ROAS) y un umbral de corte definido antes de gastar el primer peso.
2. **Los creativos son la palanca más grande.** Con el sistema actual de Meta la segmentación fina pesa cada vez menos y la variedad de creativos cada vez más. Ver playbook *Creativos*.
3. **Medir antes de pautar.** Píxel + Conversions API funcionando y verificados antes de lanzar. Sin medición no hay optimización, solo gasto.
4. **No tocar durante la fase de aprendizaje.** Cada cambio grande reinicia el aprendizaje. Ver playbook *Presupuesto y escalado*.
5. **Documentar lo que no funcionó.** El retro de una campaña mala vale más que el de una buena.
