---
tags:
  - claude
  - project-instructions
  - nivel-0
updated: 2026-09-14
---

# CLAUDE.md — Instrucciones del vault

> Leer antes de tocar cualquier cosa acá.

---

## Qué es este vault

Vault de Obsidian de **Innova Ads**, la unidad de publicidad digital de Innova Solutions. Hoy: Meta Ads gestionado para clientes. Es hermano de `obsidian_innova` (webs + automatización n8n) y sigue sus mismas convenciones.

- **`ADS_MASTER.md`** — punto de entrada. Solo linkea a hubs.
- **`clientes/`** — ficha comercial por cliente (contacto, cobro, alcance). Para humanos.
- **`meta/`** — base operativa de Meta Ads. Lo más crítico.
  - `meta/METODOLOGIA.md` — Spec Kit por campaña (brief → research → plan → tasks → resultados → retro).
  - `meta/playbooks/` — conocimiento reutilizable de la plataforma.
  - `meta/clientes/<slug>/` — trabajo operativo por cliente: README, ACCESOS (puntero), `campanas/`, `creativos/`, `reportes/`.
  - `meta/templates/` — plantillas. Se copian, no se editan.
- **`workflows/`** — procesos internos repetibles (onboarding, lanzamiento, ciclo semanal, reporte).
- **`research/`** — novedades de la plataforma y benchmarks, por fecha.
- **`reuniones/`** — actas.

---

## Reglas duras

1. **Ningún secreto en el repo.** Tokens de la Marketing API, claves de cuentas, App Passwords: van en `~/.config/innova/ads-<cliente>.env` con `chmod 600`. En el vault solo va `ACCESOS.md` diciendo *dónde* está cada cosa. `.gitignore` bloquea `*.env`, `.mcp.json` y credenciales sueltas; `ACCESOS.md` se versiona a propósito, porque nunca lleva un secreto, solo dice dónde está. El vault innova estuvo público con credenciales adentro; acá no se repite.
2. **Nunca operar con el usuario del cliente.** Siempre acceso como partner desde el Business Manager de Innova. Si el cliente pasa su login, se le explica por qué no.
3. **Ninguna campaña se lanza sin `brief.md`, `plan.md` y `tasks.md`** con el plan confirmado por Francisco. Ver [[meta/METODOLOGIA|Metodología]].
4. **Nunca contactar al cliente desde una automatización** sin que Francisco lo apruebe. Pruebas al mail de Francisco.
5. **La pauta la paga el cliente en su cuenta.** Innova no carga tarjeta propia en cuentas de clientes.
6. **Los números del reporte salen de Ads Manager o de la API**, nunca de memoria. Si no se pudo medir, se dice.

---

## Convenciones

- Frontmatter en todas las notas: `tags`, `updated` (YYYY-MM-DD) y el nivel (`nivel-0` a `nivel-3`) que colorea el grafo.
- Notas de cliente llevan `client: <slug>`. Notas de campaña llevan además `campaign`, `status` (`brief` · `planificada` · `activa` · `pausada` · `cerrada`) y `objetivo`.
- Jerarquía en el grafo: master → hub → nota. Las plantillas se linkean solo desde la nota que las consume (la metodología), no desde los hubs.
- Slugs en kebab-case. Campañas: `YYYY-MM-<slug>` dentro de `meta/clientes/<cliente>/campanas/`.
- Español rioplatense, voseo, corto. Nombres de la plataforma en el idioma en que aparecen en Ads Manager (en español).

---

## Memoria

La memoria entre conversaciones vive en el sistema de memoria de Claude, no acá. Acá van los hechos del negocio y de las campañas.

---

## Referencia rápida

| Quiero… | Voy a |
| --- | --- |
| Entender cómo se arma una campaña | `meta/METODOLOGIA.md` |
| Ver todos los clientes con pauta | `meta/clientes/_index.md` |
| Ver qué campañas están activas y qué tareas hay | `meta/COCKPIT.md` |
| Buscar cómo se hace algo en Meta | `meta/playbooks/_index.md` |
| Dar de alta un cliente | `workflows/onboarding-cliente-ads.md` |
| Ver qué aprendimos | `meta/lecciones.md` |
