---
tags:
  - meta
  - accesos
  - nivel-2
client: innova
updated: 2026-09-14

---

# 🔑 Accesos de Innova (interno) — dónde están

> **Acá no hay ningún secreto y no lo va a haber.** Este archivo dice dónde viven las claves, nada más.

← Volver a [[meta/clientes/innova/README|Innova · operación]]

---

## Dónde viven

`~/.config/innova/ads-innova.env` — `chmod 600`, fuera de todo repo. A crear en el setup.

```
META_AD_ACCOUNT_ID=act_...
META_PIXEL_ID=...
META_SYSTEM_USER_TOKEN=...        # SECRETO
META_PAGE_ID=...
WA_PHONE_NUMBER_ID=...            # la línea de Innova ya conectada a WhatsApp Cloud API
```

---

## Qué llegó, y cuándo

| Sistema | Qué | Cómo se accede | Fecha |
| --- | --- | --- | --- |
| Portfolio empresarial | Propietario | Cuenta de Francisco | — |
| Cuenta publicitaria | A crear | — | — |
| Píxel | A crear | — | — |
| Marketing API | Token de usuario del sistema | `.env` | — |

---

## Qué falta

- [ ] Crear o verificar el Portfolio de Innova
- [ ] Crear la cuenta publicitaria y cargar la tarjeta de Innova
- [ ] Crear el píxel y ponerlo en innovasolutionsai.io (píxel + CAPI)
- [ ] Usuario del sistema + token para reportes
