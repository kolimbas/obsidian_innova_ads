---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-14
---

# Estructura de cuenta

> Cómo se ordenan los activos de Meta y cómo Innova accede a los de un cliente sin usar su usuario.

← Volver a [[meta/playbooks/_index|Playbooks]]

---

## Las piezas

| Activo | Qué es | De quién tiene que ser |
| --- | --- | --- |
| **Portfolio empresarial** (Business Manager) | Contenedor de todo: páginas, cuentas publicitarias, píxeles, personas | **Del cliente.** Si no tiene, se le crea uno a su nombre, con su mail. |
| **Página de Facebook + cuenta de Instagram** | La identidad que firma los anuncios | Del cliente |
| **Cuenta publicitaria** | Donde viven campañas y facturación | Del cliente, con **su** método de pago |
| **Píxel / conjunto de datos** | La medición del sitio | Del cliente, creado en su Portfolio |
| **Cuenta de WhatsApp Business** | Para click-to-WhatsApp | Del cliente |
| **Portfolio de Innova** | Desde donde operamos | De Innova |

**Regla:** todo activo pertenece al cliente. Innova entra como **socio (partner)** con permisos sobre esos activos. El día que la relación termina, el cliente se queda con su historial, su píxel y sus audiencias. Es lo correcto y además es un argumento de venta.

---

## Cómo pedir acceso (paso a paso para el cliente)

1. El cliente entra a `business.facebook.com` → Configuración → Usuarios → **Socios** → *Agregar* → *Dar acceso a un socio a tus activos*.
2. Pega el **ID del Portfolio de Innova** (guardarlo en `ACCESOS-PUNTERO.md` del cliente; el ID no es secreto).
3. Marca: página (administrar), cuenta publicitaria (administrar campañas), píxel (administrar), Instagram, WhatsApp.
4. Innova ve los activos en su Portfolio y asigna a las personas del equipo.

Si el cliente no sabe hacerlo, se hace por videollamada compartiendo pantalla **de él**. Nunca pedimos usuario y contraseña.

---

## Checklist de una cuenta sana

- [ ] Portfolio verificado (verificación de empresa): lo piden para WhatsApp API y para límites de gasto altos.
- [ ] Dominio verificado en Seguridad de la marca → Dominios.
- [ ] Método de pago cargado por el cliente, con **límite de gasto de la cuenta** configurado como red de seguridad.
- [ ] Autenticación en dos pasos en el usuario del cliente que es administrador.
- [ ] Al menos **dos administradores** del Portfolio (si uno pierde acceso, no se pierde la cuenta).
- [ ] Página con información completa, foto, y sin advertencias en Calidad de la cuenta.
- [ ] Píxel instalado y recibiendo eventos (ver playbook *Píxel y Conversions API*).

---

## Jerarquía de una campaña

```
Campaña        → objetivo · presupuesto (si es presupuesto de campaña Advantage+)
└── Conjunto   → audiencia · ubicaciones · optimización · calendario · presupuesto (si es por conjunto)
    └── Anuncio → creativo · textos · llamado a la acción · destino · UTMs
```

Nombres, siempre iguales, para que los reportes se lean solos:

- Campaña: `[cliente] YYYY-MM · objetivo · qué vende` → `[NAUTILUS] 2026-10 · Leads · Viajes de egresados`
- Conjunto: `audiencia · ubicación` → `Amplia AR 25-55 · Auto` / `Similar compradores 3% · Auto`
- Anuncio: `ángulo · formato · versión` → `Precio · Video 9:16 · v2`

---

## Facturación en Argentina

Meta factura a cuentas argentinas en pesos con **IVA 21%** encima del gasto en pauta. Según la condición fiscal del cliente pueden aplicar percepciones. Aclararlo en la cotización para que el cliente no se sorprenda: "pauta de $X + IVA". Confirmar con el contador del cliente qué puede tomar como crédito fiscal.
