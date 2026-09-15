---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-14
---

# Píxel y Conversions API

> Sin medición no hay optimización. Meta aprende de los eventos que le mandamos; si le mandamos pocos o mal, aprende poco o mal.

← Volver a [[meta/playbooks/_index|Playbooks]]

---

## Las dos vías

| Vía | Cómo funciona | Qué pierde |
| --- | --- | --- |
| **Píxel** (navegador) | Script en el sitio que dispara eventos cuando el usuario hace algo. | Bloqueadores, iOS, cookies que caducan. Hoy pierde una parte importante de los eventos. |
| **Conversions API** (servidor) | El sitio o el backend manda el evento directo a Meta. | Nada del lado del navegador. Necesita que alguien lo implemente. |

**Los dos juntos**, con deduplicación: el mismo evento se manda por las dos vías con el mismo `event_id` y Meta se queda con uno. Es el estándar desde hace años y sigue siendo lo que más mejora el costo por resultado en cuentas chicas.

---

## Eventos estándar que usamos

| Evento | Cuándo se dispara |
| --- | --- |
| `PageView` | Toda página. Automático. |
| `ViewContent` | Ficha de producto o de servicio. |
| `Lead` | Formulario enviado en el sitio. |
| `Contact` | Click en botón de WhatsApp o llamada. Muy útil como evento intermedio para negocios que cierran conversando. |
| `Schedule` | Turno reservado. |
| `AddToCart` · `InitiateCheckout` · `Purchase` | E-commerce, con `value` y `currency`. Sin valor no hay ROAS. |

Los eventos personalizados sirven para diagnóstico, pero para optimizar conviene un estándar: el sistema los entiende mejor.

---

## Cómo lo implementamos según el sitio

- **Sitio hecho por Innova (Lovable/Next + Vercel):** píxel por script y CAPI desde el backend o desde n8n con el token del conjunto de datos. Un endpoint recibe el evento del front con su `event_id` y lo reenvía. Bundle en el vault innova.
- **Shopify / Tiendanube / WooCommerce:** usar la integración nativa de la plataforma con Meta, que ya manda píxel + CAPI. No reinventar.
- **Sitio ajeno sin acceso:** Google Tag Manager si hay, y CAPI vía la "puerta de enlace de la API de conversiones" que Meta ofrece hosteada. Última opción: solo píxel y aceptar la pérdida.
- **Sin sitio:** formularios instantáneos y click-to-WhatsApp. No hace falta píxel para eso, pero sí para remarketing.

---

## Verificación antes de lanzar (obligatoria)

1. **Administrador de eventos → Probar eventos**: navegar el sitio y ver cada evento llegar, por navegador y por servidor, con el mismo ID.
2. **Calidad de coincidencia de eventos (EMQ)**: mirar el puntaje de los eventos de conversión. Menos de 6 sobre 10 significa que mandamos pocos datos del usuario (mail, teléfono, nombre, IP, user agent). Más datos hasheados, mejor puntaje, mejor atribución.
3. **Deduplicación**: en el detalle del evento, "Eventos deduplicados" tiene que ser alto. Si es 0, los `event_id` no coinciden.
4. **Dominio verificado** en el Portfolio del cliente.
5. Un evento de prueba con la extensión Meta Pixel Helper, y ninguna advertencia.

---

## Cosas que pasan siempre

- El sitio tiene dos píxeles (uno viejo del diseñador anterior). Sacar el que no se usa.
- El evento `Lead` se dispara al *cargar* la página del formulario y no al enviarlo. Todo el mundo "convierte".
- `Purchase` sin `value`. El ROAS da 0 y el cliente cree que la pauta no vende.
- El consentimiento de cookies bloquea el píxel y nadie lo notó. Verificar aceptando y sin aceptar.
- El píxel está en el Portfolio del diseñador anterior y no del cliente. Hay que crear uno nuevo en el Portfolio correcto: la historia del viejo no se transfiere.
