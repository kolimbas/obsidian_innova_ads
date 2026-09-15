---
tags:
  - meta
  - playbook
  - nivel-3
updated: 2026-09-14
---

# Métricas

> Se mira **un** número para decidir (el KPI del brief) y tres o cuatro para entender por qué. Todo lo demás es ruido para el cliente.

← Volver a [[meta/playbooks/_index|Playbooks]]

---

## Las que importan

| Métrica                                          | Qué mide                                    | Para qué la usamos                                                                                                  |
| ------------------------------------------------ | ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **Costo por resultado** (CPL / CPA)              | Gasto ÷ leads o ventas                      | El KPI. Se compara contra el umbral del brief, no contra "benchmarks".                                              |
| **ROAS**                                         | Valor de compras ÷ gasto                    | KPI en e-commerce. Necesita `value` en el evento Compra.                                                            |
| **CPM**                                          | Costo por mil impresiones                   | Cuánto cuesta la audiencia. Sube con competencia, audiencias chicas y creativos que Meta considera de baja calidad. |
| **CTR (clics en el enlace)**                     | Clics al destino ÷ impresiones              | Si el creativo llama la atención. Usar el de *enlace*, no el "todos los clics".                                     |
| **CPC (enlace)**                                 | Gasto ÷ clics en el enlace                  | Resultado de CPM y CTR.                                                                                             |
| **Tasa de conversión de la página**              | Resultados ÷ visitas a la página de destino | Si el destino convierte.                                                                                            |
| **Frecuencia**                                   | Impresiones ÷ personas alcanzadas           | Fatiga.                                                                                                             |
| **Retención a 3 s** (hook rate)                  | Reproducciones de 3 s ÷ impresiones         | Si el video engancha. Debajo de ~25% el hook no funciona.                                                           |
| **ThruPlay ÷ reproducciones de 3 s** (hold rate) | Cuántos que empezaron llegaron al final     | Si el video sostiene.                                                                                               |

---

## Diagnóstico con tres números

El truco: **CPM → CTR → conversión**. Cada uno señala una parte distinta.

| Síntoma                                       | Probable causa                                                          | Qué tocar                                                                |
| --------------------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| CPM alto, CTR normal                          | Audiencia chica o competida, o cuenta nueva                             | Ampliar audiencia, ubicaciones automáticas, esperar aprendizaje          |
| CPM normal, CTR bajo (menos de 1% en enlace)  | El creativo no llama la atención o habla al público equivocado          | Nuevos hooks y ángulos                                                   |
| CTR bueno, conversión baja                    | La página, el formulario o la oferta no cierran; o el evento no se mide | Revisar destino y píxel antes de tocar la campaña                        |
| Todo bien, pero leads malos                   | El formulario califica poco o el ángulo atrae curiosos                  | Formulario de mayor intención, preguntas de calificación, cambiar oferta |
| Frecuencia arriba de 3-4/semana y CTR cayendo | Fatiga                                                                  | Creativos nuevos, ampliar                                                |

---

## Benchmarks: con cuidado

No usamos benchmarks de internet como umbral. Argentina tiene CPM bajos en dólares y varían por rubro, mes (noviembre y diciembre son caros) y calidad del creativo. **La primera semana de cada cuenta es su propio benchmark.** Lo que sí sirve como alarma:

- CTR de enlace por debajo de 1% en frío: el creativo no funciona.
- Retención a 3 s por debajo de 25%: el hook no funciona.
- Costo por resultado 2× el umbral después de 4-5 días con datos: apagar ese anuncio o conjunto.

Los números reales por rubro se van anotando en *Lecciones* (`meta/lecciones`) a partir de nuestros propios clientes.

---

## Ventanas de atribución

Por defecto Meta atribuye una conversión si pasó dentro de **7 días después del clic o 1 día después de ver** el anuncio. Para servicios con decisión larga, mirar también la columna de 28 días de clic (informe, no optimización). Para comparar con Google Analytics: nunca van a coincidir; Meta cuenta vistas y GA solo el último clic. Se explica una vez al cliente y se elige una fuente de verdad para el reporte (Ads Manager para pauta, el CRM o las ventas reales para el negocio).

---

## Columnas guardadas en Ads Manager

Crear un preset "Innova" con: gasto, resultados, costo por resultado, CPM, CTR (enlace), CPC (enlace), frecuencia, visitas a la página de destino, reproducciones de 3 s, ThruPlay, compras y valor de compras. Guardarlo en cada cuenta al hacer el onboarding.
