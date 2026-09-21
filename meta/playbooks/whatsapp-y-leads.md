---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-21
---

# WhatsApp y leads

> En Argentina el negocio se cierra por WhatsApp. La campaña que trae el lead es la mitad; la otra mitad es contestarlo en minutos. Acá es donde Innova Ads e Innova (automatización) son el mismo producto.

← Volver a [[meta/playbooks/_index|Playbooks]]

---

## Tres formas de captar un lead

| Forma                                 | Cómo                                                                        | Pros                                                                             | Contras                                                                                                                    |
| ------------------------------------- | --------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Click-to-WhatsApp**                 | El anuncio abre un chat de WhatsApp con un mensaje precargado               | Sin sitio, sin formulario; la conversación es el embudo; funciona muy bien en AR | Leads a veces poco calificados; si nadie contesta rápido, se pierde; medir requiere la API de WhatsApp o disciplina manual |
| **Formulario instantáneo** (Lead Ads) | El usuario completa un formulario dentro de Meta, con sus datos precargados | Muy barato por lead, sin sitio                                                   | Calidad baja si el formulario es "mayor volumen"; el lead no se entera de que mandó nada si no lo llaman rápido            |
| **Landing con formulario o botón**    | Sitio propio con píxel                                                      | Califica mejor, permite remarketing, mide todo                                   | Necesita sitio y píxel bien puestos; CPL más alto                                                                          |

Elección por defecto para servicios locales: **click-to-WhatsApp** si el cliente contesta rápido (o tiene bot); **formulario instantáneo de mayor intención** si no.

---

## Formulario instantáneo bien hecho

- Tipo **"mayor intención"**: agrega una pantalla de revisión antes de enviar. Baja el volumen y sube la calidad.
- **Una pregunta de calificación** (dos como máximo), con opciones: "¿Para cuándo lo necesitás?" o "¿En qué zona estás?". Una sola filtra curiosos sin matar el volumen; cinco lo matan (guías 2026).
- Pantalla de agradecimiento con un **botón a WhatsApp** o un "te llamamos en menos de X".
- Política de privacidad del cliente linkeada (obligatoria).
- Los leads quedan en la página de Facebook 90 días. **Nunca depender de bajarlos a mano**: webhook a n8n → WhatsApp del vendedor + Sheet/CRM. Ver *Automatizaciones* (`meta/automatizaciones`).
- **Leads de conversión:** si el CRM devuelve a Meta el estado del lead (calificado, reunión, cierre) por Conversions API, el conjunto se puede optimizar a *leads que califican* y no a envíos. Es lo que más mejora la calidad cuando hay volumen.

---

## Click-to-WhatsApp bien hecho

- La cuenta de WhatsApp Business del cliente conectada a su página desde el Portfolio.
- Mensaje precargado que ya avanza la conversación: "Hola, vi el anuncio de X. Quiero saber…" con las **preguntas frecuentes como botones** si se usa la API.
- **Respuesta en menos de 5 minutos.** Contactar en 5 minutos convierte unas 9 veces más que después de una hora (guías 2026). Si el cliente no puede, va bot de primera respuesta (Innova) que hace 1-2 preguntas de calificación y avisa al vendedor.
- **Ventana gratuita:** cuando alguien escribe desde un anuncio se abre una ventana de 24 h; si el negocio responde dentro, se extiende a **72 h en las que todo mensaje es gratis** (doc oficial de Meta). Después, WhatsApp cobra por mensaje de plantilla según categoría y país (Argentina, marketing: ~USD 0,06). Meta anunció cambios de tarifas para el 1-10-2026: confirmar en la tabla oficial antes de cotizar.
- Optimizar la campaña a **conversaciones iniciadas** al principio; cuando hay API de WhatsApp y se marcan los leads calificados, se puede optimizar a eventos de conversión de la conversación.

---

## Calidad del lead: la conversación con el cliente

Antes de lanzar se acuerda **qué es un lead válido** (zona, presupuesto, plazo) y se escribe en el brief. Después se reporta:

- Leads totales
- Leads válidos (según esa definición)
- Leads contactados en menos de 1 hora
- Cerrados

Si los válidos son pocos, se ajusta formulario, ángulo u oferta. Si los contactados a tiempo son pocos, el problema no es la pauta y hay que decirlo con el número en la mano. Es la conversación que evita que "la pauta no funciona" cuando lo que no funciona es la respuesta.

---

## Velocidad de respuesta, en números

No hay estudio argentino serio, pero la experiencia en todos los rubros dice lo mismo: un lead contactado en los primeros minutos se convierte varias veces más que uno contactado al día siguiente. Es el argumento para vender la automatización junto con la pauta, y el motivo por el que el flujo "lead nuevo → WhatsApp del vendedor" es el primero que se construye para cada cliente.
