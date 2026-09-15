---
tags:
  - meta
  - accesos
  - nivel-2
client: <slug>
updated: {{date:YYYY-MM-DD}}
---

# 🔑 Accesos de <Cliente> — dónde están

> **Acá no hay ningún secreto y no lo va a haber.** Este archivo dice dónde viven las claves, nada más. `.gitignore` bloquea `accesos.md` (en cualquier mayúscula), `*.env` y `credenciales/`; por eso este puntero se llama `ACCESOS-PUNTERO.md` y sí se versiona.

---

## Dónde viven

`~/.config/innova/ads-<slug>.env` — `chmod 600`, fuera de todo repo.

Variables esperadas:

```
META_AD_ACCOUNT_ID=act_...        # no es secreto, pero va junto
META_PIXEL_ID=...                 # no es secreto
META_SYSTEM_USER_TOKEN=...        # token de usuario del sistema (Marketing API), SECRETO
META_PAGE_ID=...
WA_PHONE_NUMBER_ID=...            # si hay WhatsApp Cloud API
```

---

## Qué llegó, y cuándo

| Sistema | Qué | Cómo se accede | Fecha |
| --- | --- | --- | --- |
| Portfolio empresarial | Acceso como socio | Desde el Portfolio de Innova | |
| Cuenta publicitaria | Administrar campañas | Ídem | |
| Página + Instagram | Administrar | Ídem | |
| Píxel | Administrar | Ídem | |
| Marketing API | Token de usuario del sistema | `.env` | |

---

## Qué falta

- [ ] …
