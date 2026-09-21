---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-21
---

# Objetivos de campaña

> El objetivo le dice a Meta a quién mostrarle el anuncio: a la gente que suele hacer *eso*. Elegir mal el objetivo es la forma más cara de equivocarse.

← Volver a [[meta/playbooks/_index|Playbooks]]

---

## Los seis

| Objetivo                 | Optimiza para                                                               | Cuándo lo usamos                                                                                               |
| ------------------------ | --------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Reconocimiento**       | Alcance, recuerdo                                                           | Casi nunca para PyMEs. Solo lanzamientos locales con presupuesto aparte.                                       |
| **Tráfico**              | Clicks o visitas a la página de destino                                     | Solo si no hay forma de medir nada más. Trae clicks, no clientes.                                              |
| **Interacción**          | Mensajes, interacciones con la publicación, reproducciones                  | Click-to-WhatsApp o Messenger cuando el negocio vende conversando.                                             |
| **Clientes potenciales** | Leads: formulario instantáneo, conversiones en el sitio, llamadas, mensajes | Servicios, turnos, cotizaciones. El objetivo por defecto para la mayoría de nuestros clientes.                 |
| **Promoción de la app**  | Instalaciones y eventos en app                                              | Solo si el cliente tiene app.                                                                                  |
| **Ventas**               | Compras, carritos, conversiones de valor                                    | E-commerce y todo lo que se paga online. También sirve para leads de alta intención si el píxel tiene volumen. |

---

## Regla para elegir

Preguntarse **cuál es la acción que más cerca está de la plata** y que el píxel o el formulario pueden medir con volumen suficiente (unas 50 por semana por conjunto).

- Se puede medir compras con volumen → **Ventas**, evento Compra.
- Se puede medir leads pero no compras → **Clientes potenciales**, evento Lead o formulario.
- Hay leads pero pocos (menos de 50/semana) → subir un escalón en el embudo: optimizar a *Contacto* o *Ver contenido*, y a medida que crece el volumen bajar a Lead.
- El negocio cierra por WhatsApp → **Interacción** con destino WhatsApp, o **Clientes potenciales** con conversión "conversación iniciada". **Nunca Tráfico para WhatsApp**: optimiza clics y trae gente que no escribe.

Nunca elegir Tráfico "para empezar". Empieza igual de mal y termina peor.

---

## Advantage+

Meta viene juntando sus automatizaciones bajo el nombre Advantage+: presupuesto de campaña, audiencia, ubicaciones, creativo. Las campañas "Advantage+ de ventas" y "de clientes potenciales" entregan casi todo al sistema y piden a cambio **muchos creativos y un píxel con datos**.

Cuándo sí: cuenta con historial, píxel con volumen, catálogo o varios creativos, presupuesto que aguante aprendizaje.
Cuándo no: cuenta nueva, píxel vacío, un solo creativo, presupuesto chico. Ahí conviene una campaña manual con audiencia amplia y aprender antes de soltarle todo.

En la práctica arrancamos manual con **ubicaciones Advantage+** y **presupuesto de campaña**, y pasamos a Advantage+ completo cuando hay datos.

---

## Evento de optimización: el detalle que define todo

Dentro de Clientes potenciales o Ventas, el conjunto de anuncios optimiza a **un evento**. Ese evento tiene que:

1. Existir y dispararse bien (ver playbook *Píxel y Conversions API*).
2. Tener volumen (idealmente 50/semana por conjunto).
3. Estar lo más cerca posible de la venta.

Si optimizás a *Ver página* porque "hay más volumen", Meta te trae gente que mira páginas. Hace exactamente lo que le pedís.
