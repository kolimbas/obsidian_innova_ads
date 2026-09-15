---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-14
---

# Testing

> Probar es cambiar **una** cosa, con presupuesto suficiente, el tiempo necesario, y decidir con un criterio escrito antes de ver los datos. Todo lo demás es mirar números y contarse un cuento.

← Volver a [[meta/playbooks/_index|Playbooks]]
---

## Qué vale la pena testear, en orden

1. **Ángulo del creativo** — la variable que más mueve. Siempre primero.
2. **Formato** — video vs. imagen vs. carrusel, con el mismo ángulo.
3. **Oferta** — precio, bonus, garantía. Cambia la conversión, no solo el clic.
4. **Destino** — WhatsApp vs. formulario vs. landing.
5. **Audiencia** — amplia vs. intereses vs. similar. Hoy es lo que menos diferencia hace, salvo en cuentas nuevas.

Botón, color, título: solo cuando lo de arriba ya está resuelto.

---

## Estructura de un test de creativos

```
Campaña TEST · presupuesto por conjunto (ABO)
├── Conjunto A · misma audiencia · anuncio ángulo 1 (2 formatos)
├── Conjunto B · misma audiencia · anuncio ángulo 2 (2 formatos)
└── Conjunto C · misma audiencia · anuncio ángulo 3 (2 formatos)

Campaña ESCALA · presupuesto de campaña
└── Conjunto amplia · los ganadores del test
```

Cada conjunto con el mismo presupuesto, sin tocar durante 5-7 días. El ganador pasa a la campaña de escala; el test sigue con ángulos nuevos. Así la campaña que vende nunca se reinicia por un experimento.

Alternativa cuando hay muchos creativos y datos: **un solo conjunto amplio con 6-10 anuncios** y dejar que Meta reparta. Es más barato pero reparte desparejo: algunos anuncios no gastan nunca. Se usa en cuentas ya rodadas.

---

## La herramienta de pruebas A/B de Meta

Sirve cuando se quiere aislar bien una variable (audiencias que se solapan, por ejemplo): divide a la gente para que nadie vea las dos versiones. Cuesta más presupuesto y tiempo. Para creativos, la estructura de arriba alcanza.

---

## Criterio de decisión (escribirlo en el plan antes de lanzar)

- **Métrica de decisión**: el KPI del brief. No "el que tenga mejor CTR".
- **Mínimo de datos por variante**: idealmente 30-50 resultados. Con 5 leads por lado no se decide nada; se decide con costo por clic y retención como indicios y se sigue testeando.
- **Duración**: 5-7 días completos, incluyendo fin de semana.
- **Diferencia mínima**: si el ganador no gana por al menos 20-30%, no hay ganador; hay dos anuncios que sirven.

---

## Registro

Cada test es una fila en `resultados.md` de la campaña: qué se probó, contra qué, con cuánto, cuánto duró, qué dio y qué se decidió. Sin registro, a los dos meses se vuelve a probar lo mismo.
