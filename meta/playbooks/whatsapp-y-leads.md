---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-14
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
- **2-3 preguntas de calificación** personalizadas y una con opciones: "¿Para cuándo lo necesitás?", "¿En qué zona estás?", "¿Presupuesto aproximado?". Cada pregunta filtra curiosos.
- Pantalla de agradecimiento con un **botón a WhatsApp** o un "te llamamos en menos de X".
- Política de privacidad del cliente linkeada (obligatoria).
- Los leads quedan en la página de Facebook 90 días. **Nunca depender de bajarlos a mano**: webhook a n8n → WhatsApp del vendedor + Sheet/CRM. Ver [[meta/automatizaciones|Automatizaciones]].

---

## Click-to-WhatsApp bien hecho

- La cuenta de WhatsApp Business del cliente conectada a su página desde el Portfolio.
- Mensaje precargado que ya avanza la conversación: "Hola, vi el anuncio de X. Quiero saber…" con las **preguntas frecuentes como botones** si se usa la API.
- **Respuesta en menos de 5 minutos.** Si el cliente no puede, va bot de primera respuesta (Innova) que hace las 2-3 preguntas de calificación y avisa al vendedor.
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
