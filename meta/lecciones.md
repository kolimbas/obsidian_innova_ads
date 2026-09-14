---
tags:
  - meta
  - lessons
  - nivel-2
updated: 2026-09-14
---

# 📒 Lecciones

> Una línea por cosa aprendida. Fecha, cliente (o "general"), qué pasó, qué hacemos distinto. Se alimenta desde cada `retro.md`.

← Volver a [[meta/README|Meta Ads KB]]

---

| Fecha | Cliente | Lección |
| --- | --- | --- |
| 2026-09-14 | general | El vault innova estuvo público con credenciales adentro. Acá `accesos.md` y `*.env` están en `.gitignore` desde el día uno; en el vault va solo el puntero. |
| 2026-09-14 | general | El patrón `accesos.md` en minúscula del `.gitignore` bloqueaba también el `ACCESOS.md` real (mayúscula) en cualquier Mac, porque `core.ignorecase=true` hace el match sin distinguir mayúsculas. El puntero que se supone que sí se versiona nunca habría llegado al repo. Se sacó ese patrón; solo quedan bloqueados los secretos reales (`*.env`, `.mcp.json`, `credenciales/`, etc.). |
