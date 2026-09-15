---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-14
---

# Presupuesto y escalado

> Meta necesita datos para aprender y tiempo para aplicarlos. El presupuesto define cuánto aprende; la paciencia, si le dejamos usar lo aprendido.

← Volver a [[meta/playbooks/_index|Playbooks]]
---

## Cuánto hace falta

La fase de aprendizaje de un conjunto termina con unos **50 eventos de optimización en 7 días**. De ahí sale la cuenta:

```
presupuesto diario por conjunto ≈ 7 × costo por resultado esperado
```

Ejemplos: si esperamos un lead a USD 3, hacen falta unos USD 20/día por conjunto. Si esperamos ventas a USD 25, unos USD 175/día. Con menos, el conjunto queda en "aprendizaje limitado" y rinde peor de lo que podría.

**Regla comercial:** si el cliente no puede poner ese presupuesto para el evento que quiere, se optimiza a un evento más arriba en el embudo (contacto, ver contenido) o se le dice que con esa pauta no vamos a poder prometer resultados. Mejor decirlo antes que después.

Mínimo que aceptamos gestionar: el que haga que el fee de Innova no sea más grande que la pauta. Se define en *Clientes* (`clientes/clientes`).

---

## Presupuesto de campaña o de conjunto

- **De campaña (Advantage+)**: Meta reparte entre conjuntos según rendimiento. Por defecto cuando los conjuntos son parecidos.
- **De conjunto (ABO)**: control fijo por conjunto. Para tests donde queremos que cada variante gaste lo mismo, y para remarketing con presupuesto acotado.

---

## Fase de aprendizaje: qué la reinicia

Cualquier cambio "significativo" en el conjunto la reinicia, y durante esos días el costo suele empeorar:

- Cambiar el presupuesto más de ~20% de una vez.
- Cambiar audiencia, ubicaciones, evento de optimización o estrategia de puja.
- Agregar o editar creativos (en ese conjunto).
- Pausar más de 7 días.

Por eso: **la primera semana no se toca**, salvo un anuncio que esté gastando muy por encima del umbral sin ningún resultado.

---

## Escalado

Cuando una campaña rinde debajo del umbral de forma estable (una semana, no un día bueno):

1. **Vertical**: subir el presupuesto **20% cada 2-3 días** mientras el costo se mantenga. Si empeora más de un 20-30%, volver un paso.
2. **Horizontal**: duplicar el conjunto ganador con otra audiencia (amplia si era intereses; similar si era amplia) o sumar creativos nuevos. Suma volumen sin tocar lo que funciona.
3. **Tope realista**: cada mercado tiene un techo. Cuando escalar 20% sube el costo 30%, se llegó. Ahí conviene un producto nuevo o un ángulo nuevo, no más plata.

Nunca duplicar el presupuesto de golpe "porque anda bien". Es la forma clásica de matar una campaña que andaba.

---

## Cuándo apagar

- Un **anuncio** con gasto de 2-3× el costo esperado y cero resultados: apagar. Con resultados pero costo 2× el umbral sostenido 4-5 días: apagar.
- Un **conjunto** que después de salir de aprendizaje sigue arriba del umbral: apagar y probar otra audiencia, no "darle otra semana".
- Una **campaña** entera: solo con el cliente, en la reunión de status, con los números y una alternativa sobre la mesa.

---

## Calendario de revisión

| Momento | Qué se hace |
| --- | --- |
| Día 1 | Verificar que gasta, que los eventos llegan, que no hay rechazos. Nada más. |
| Día 4-5 | Primera lectura. Apagar solo lo claramente roto. |
| Día 7 | Fin de aprendizaje. Decisión por conjunto y por anuncio. Primer reporte al cliente. |
| Cada semana | workflow *Ciclo semanal*. |
| Día 30 | Retro, reporte mensual, decisión de escalar o replantear. |
