---
tags:
  - meta
  - clients
  - nivel-2
updated: 2026-09-14
---

# Clientes — operación de Meta Ads

> Una carpeta por cliente. Adentro: `README.md` con el contexto operativo, `ACCESOS.md` con punteros (nunca claves), y `campanas/`, `creativos/`, `reportes/`.

← Volver a [[meta/README|Meta Ads KB]]

---

## Roster

| Cliente | Estado | Campañas activas | Pauta/mes | Notas |
| --- | --- | --- | --- | --- |
| *(todavía ninguno)* | | | | |

> La ficha comercial (contacto, cobro, alcance) vive en `clientes/`. Este índice solo sigue a los clientes con pauta.

Estados: `onboarding` · `setup` · `activo` · `pausado` · `cerrado`.

---

## Cómo se da de alta un cliente acá

1. Crear `meta/clientes/<slug>/` con `campanas/`, `creativos/`, `reportes/`.
2. Copiar `meta/templates/cliente-README.md` como `README.md` y completarlo.
3. Copiar `meta/templates/ACCESOS.md` como `ACCESOS.md`: solo dónde vive cada acceso.
4. Agregar la fila arriba.
5. Seguir [[workflows/onboarding-cliente-ads|el onboarding]] para lo técnico (partner, píxel, dominio, pago).
