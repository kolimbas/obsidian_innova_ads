---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-21
---

# Catálogo y anuncios dinámicos

> Cuando el cliente tiene muchos productos (o vehículos), el anuncio que mejor rinde es el que Meta arma solo con el catálogo: le muestra a cada persona el producto que miró o el que más le va a interesar. En 2026 es el formato que mejor sostiene el rendimiento con el tiempo.

← Volver a [[meta/playbooks/_index|Playbooks]]

---

## Cuándo aplica

| Cliente | Catálogo | Formato de Meta |
| --- | --- | --- |
| E-commerce (Tiendanube, Shopify, Woo) | Productos | Anuncios de catálogo / Advantage+ de ventas |
| Concesionaria (autos, motos) | Vehículos | **Automotive Inventory Ads** |
| Inmobiliaria | Propiedades | Anuncios de inventario inmobiliario |
| Servicios con pocos productos | No aplica | Creativos estáticos y video |

Regla: con más de ~20 ítems que rotan, catálogo. Con 3 productos, no.

---

## Qué necesita

1. **Un feed**: archivo CSV, TSV o XML (o integración nativa) con los campos obligatorios, actualizado al menos una vez por día. Vendido o sin stock → sale del feed el mismo día, o el anuncio muestra lo que no hay.
2. **Píxel + Conversions API con eventos de catálogo**: `ViewContent`, `AddToCart`, `Purchase` con `content_ids` que coincidan con los ID del feed. En vehículos: `ViewContent` con `content_type = vehicle` y el VIN o ID como `content_ids`. Sin esto, no hay retargeting dinámico.
3. **Catálogo en el Portfolio del cliente** (Commerce Manager), con el feed programado y el píxel asociado.
4. **Plantillas de diseño** (Design Rules / marcos): precio, oferta, "nuevo ingreso", estacional. Meta las aplica sobre cada ítem; según datos de 2026, las cuentas que las usan rinden mejor.

### Campos mínimos

**Productos:** `id`, `title`, `description`, `availability`, `condition`, `price`, `link`, `image_link`, `brand`, `google_product_category` (opcional pero mejora).

**Vehículos:** `vehicle_id` (VIN o ID interno), `make`, `model`, `year`, `trim`, `price`, `mileage`, `body_style`, `state_of_vehicle` (new/used), `title`, `description`, `url`, `image[0..N]`, `availability`, `dealer_name`, `address`.

---

## Integraciones que ya lo resuelven

- **Tiendanube / Shopify / WooCommerce:** integración nativa con Meta: crea el catálogo, manda píxel + CAPI y sincroniza stock. No reinventar; solo verificar que los eventos lleguen con `content_ids`.
- **WordPress con plugin de inventario** (caso Alpha Cycles, plugin Motors): no hay integración nativa. El feed lo arma Innova desde la base (n8n → CSV público en Vercel o Drive) y Meta lo lee cada 6-24 h. Innova ya sincroniza el inventario de Alpha a Neon (flujo A18): el feed es un paso más.

---

## Estructura de campaña con catálogo

```
Campaña PROSPECCIÓN (Advantage+ de ventas o Ventas manual)
└── Conjunto amplio · catálogo completo · Advantage+ audiencia
    ├── Anuncio catálogo · plantilla precio
    ├── Anuncio catálogo · plantilla lifestyle
    └── 3-5 estáticos/video de marca (para que el sistema tenga variedad)

Campaña RETARGETING (Ventas · catálogo)
└── Conjunto "vieron producto 14 días sin comprar" · productos vistos y relacionados
```

Presupuesto: 70-80% prospección, 20-30% retargeting. En concesionarias, Meta sugiere 40/30/30 entre prospección, consideración y acción.

---

## Lo que dicen los datos de 2026

- Catálogo: **+23% ROAS y -37% CPA** frente a estáticos; las cuentas con 60-100% del gasto en catálogo, +44% ROAS (Confect, dataset de USD 834 M).
- Fatiga más lenta: el catálogo se renueva solo con la rotación de productos; las plantillas se cambian cada 4-6 semanas.
- Automotive Inventory Ads con audiencia ampliada: **+44% leads y -29% CPL** (caso de Meta, Rusnak Auto Group).
- Cuentas grandes rinden con 5 o más variantes de diseño de catálogo distintas (precio, lifestyle, prueba social, minimal, estacional).

---

## Errores que vemos venir

- Feed que no saca lo vendido: el cliente recibe consultas por unidades que no tiene.
- `content_ids` del píxel que no coinciden con `id` del feed: el retargeting dinámico queda vacío y nadie se da cuenta.
- Precio del feed distinto al del sitio o al de la concesionaria (en EE. UU., la FTC advirtió a 97 grupos en marzo de 2026 por precios no transparentes).
- Catálogo creado en el Portfolio de la agencia y no en el del cliente.

---

## Checklist antes de lanzar

- [ ] Catálogo en el Portfolio del cliente, feed programado, sin ítems rechazados
- [ ] Píxel con `content_ids` coincidentes (probar en Administrador de eventos → Probar eventos → ver el `content_ids` de un `ViewContent`)
- [ ] Al menos 2 plantillas de diseño
- [ ] Conjunto amplio + conjunto de retargeting
- [ ] Un ítem vendido de prueba: ¿desaparece del feed en la próxima corrida?
