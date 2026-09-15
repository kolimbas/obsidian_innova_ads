---
tags:
  - workflow
  - optimizacion
  - nivel-2
updated: 2026-09-14
---

# Ciclo semanal de optimización

> Todos los lunes, por cada cliente activo, en este orden. Una hora por cliente si está ordenado. Lo que se decide se escribe en `resultados.md` antes de tocar la campaña.

← Volver a [[workflows/workflows|Workflows]]

---

## 1. Salud (5 min)

- [ ] Calidad de la cuenta: rechazos, restricciones, avisos.
- [ ] Método de pago sin problemas.
- [ ] Los eventos siguen llegando (Administrador de eventos, últimos 7 días).
- [ ] El destino sigue funcionando.

## 2. Leer (15 min)

Con el preset de columnas "Innova", últimos 7 días vs. 7 anteriores:

- [ ] Costo por resultado vs. umbral, por campaña y por conjunto.
- [ ] Diagnóstico CPM → CTR → conversión (playbook *Métricas*).
- [ ] Frecuencia y CTR por anuncio: ¿fatiga?
- [ ] Leads válidos y contactados a tiempo (del Sheet o del CRM del cliente).

## 3. Decidir (10 min)

Según las reglas escritas en el plan:

- [ ] Apagar anuncios a 2× el umbral con datos suficientes.
- [ ] Escalar +20% lo que está bajo el umbral hace una semana.
- [ ] Duplicar horizontalmente si hay un ganador claro y presupuesto.
- [ ] Nada durante la fase de aprendizaje, salvo lo claramente roto.

Cada decisión: fecha, qué, por qué, en `resultados.md`.

## 4. Creativos (20 min)

- [ ] Al menos un creativo nuevo por campaña activa (nuevo hook o ángulo). Nota en `creativos/`.
- [ ] Pedir al cliente material si se está acabando.

## 5. Reportar (10 min)

- [ ] Fila de la semana en `resultados.md` y en el Sheet.
- [ ] Mail del lunes con la plantilla plantilla `reporte-semanal` (o el flujo n8n si ya existe).
- [ ] Si hay algo que el cliente tiene que hacer (contestar más rápido, mandar fotos), va en el mail, con el número que lo justifica.

## 6. Cerrar

- [ ] `updated` en el brief y el README del cliente.
- [ ] Tareas nuevas en `tasks.md`.
