# Marketplace Inverso de Servicios — Plan de acción (30 días)

> **Estado:** borrador v1 (pendiente de incorporar el dossier original).
> **Visión:** una web donde cualquier persona o empresa publica lo que necesita y los profesionales le mandan ofertas. Empezamos en Madrid y después, toda España.
> **Objetivo de estos 30 días:** tener el **guion del proyecto** (qué es, a quién sirve, cómo gana dinero, cómo se construye) y una **primera validación real**. No es lanzar el producto completo.

---

## 1. Decisiones tomadas

| Tema | Decisión |
|---|---|
| Alcance | Plataforma **general** (cualquier servicio) |
| Ciudad inicial | Madrid |
| Ingresos | Comisión sobre el servicio (abierto a combinar con otros modelos) |
| Recursos | Tú solo, pocas horas, programación con IA, presupuesto limitado |
| Ventaja propia | Conoces por dentro la **automoción** (talleres y recambios) |

---

## 2. Mi recomendación clave: plataforma general, arranque por automoción

Una plataforma "de todo" no puede lanzarse con todo a la vez. Con pocas horas y sin presupuesto, si una web vacía tiene 40 categorías, cada categoría tendrá cero ofertas y el cliente no vuelve.

**Propuesta:** diseñar la plataforma para que sea general (la estructura, la marca y la base de datos admiten cualquier categoría), pero **lanzar primero una sola categoría: reparación y mantenimiento de coches en Madrid.** Después se abren categorías de una en una cuando la anterior funciona. Así empezaron casi todos los marketplaces que hoy son generales.

**Por qué la automoción:**
- **Conoces el gremio.** Sabes cómo presupuestan los talleres, qué margen tienen, cuánto cuestan las piezas y quién decide. Esa es tu única ventaja injusta, y es buena.
- **El cliente sufre de verdad.** Desconfía del taller, no sabe si le cobran de más y quiere comparar precios. Un marketplace inverso resuelve eso directamente.
- **Presupuestos comparables.** "Pastillas delanteras, Seat León 2018" es una petición concreta que se puede comparar, a diferencia de "reformar mi cocina".
- **Demanda recurrente.** Revisiones, ITV, neumáticos, frenos: un coche necesita algo varias veces al año.
- **Tickets adecuados para cobrar comisión** (entre 80 y 1.000 €).
- **Hueco en el mercado.** Los comparadores de talleres que existen se centran en precios cerrados de servicios estándar. "Describe tu avería y recibe ofertas" está mucho menos cubierto.

> ⚠️ **Antes de nada:** revisa tu contrato con Áncora (exclusividad, no competencia, uso de contactos de clientes). No utilices datos ni listados de clientes de la empresa para este proyecto. Que tu propio conocimiento del sector sea tu ventaja es legítimo, y que el proyecto se aproveche de la cartera de tu empresa te podría traer problemas.

---

## 3. Modelo de ingresos

### El problema de la comisión pura
Si el cliente y el taller se conocen a través de tu web y el pago se hace en el taller, lo normal es que la siguiente vez te salten, e incluso que no declaren la primera. No puedes comprobar a cuánto se cerró el trabajo. Es el mayor riesgo del modelo que quieres.

### Cómo hacer que la comisión funcione
Para cobrar comisión, **el pago (o al menos una señal) tiene que pasar por tu plataforma**, y además tiene que haber motivos para no saltársela:
1. **Pago o señal online** al aceptar la oferta (por ejemplo, con Stripe Connect, que reparte automáticamente tu comisión y el dinero del taller).
2. **Garantía de la plataforma:** si algo sale mal, tú median. Esto solo funciona si el pago pasó por ti.
3. **Reseñas verificadas:** el taller solo acumula reputación si trabaja a través de la web.
4. **Precio cerrado:** la oferta aceptada es la que se paga, sin sorpresas. Es lo que más valora el cliente con talleres.

### Opciones de ingreso (se pueden combinar)
| Modelo | Quién paga | Ventajas | Inconvenientes |
|---|---|---|---|
| **Comisión (8–15 %)** | Taller | Solo pagan si ganan; escala con el volumen | Te saltan si el pago no pasa por ti |
| **Pago por oferta enviada** (1–5 €) | Taller | Cobras seguro y es fácil de montar | Frena a los talleres al principio |
| **Suscripción** (20–60 €/mes) | Taller | Ingreso predecible | Difícil vender sin volumen demostrado |
| **Tarifa de gestión** (1–3 €) | Cliente | Aumenta los ingresos por trabajo | El cliente la ve como una barrera |
| **Destacados / publicidad** | Taller o marcas | Margen alto | Solo con mucho tráfico |

**Recomendación por fases:**
- **Fase 1 (validación):** gratis para todos. Solo se mide si hay demanda y si los talleres responden.
- **Fase 2:** comisión del **~10 % cobrada con un pago o señal online**, más garantía. Es tu modelo, protegido.
- **Fase 3:** añadir suscripción "Pro" o destacados para los talleres que más trabajan.

No recomiendo cobrar al cliente por **ver** las ofertas. Es justo lo que le hace irse a la competencia gratuita.

---

## 4. Cómo se construye (sin saber programar)

| Fase | Herramientas | Coste |
|---|---|---|
| **1. Validación manual** | Landing (Carrd/Framer) + formulario (Tally) + Google Sheets + WhatsApp Business | 0–30 € |
| **2. Web propia sencilla** | Programada con Claude Code: Next.js + Supabase (usuarios y base de datos) + Stripe Connect (pagos), publicada en Vercel | 0–25 €/mes al principio |
| **3. Crecer** | App móvil, más categorías, automatizar la búsqueda de profesionales | Según tracción |

En la fase 1 no se programa nada: tú haces a mano lo que luego hará la web. Así sabes **exactamente** qué tienes que programar después.

---

## 5. Plan semana a semana (pensado para ~5–8 h/semana)

### Semana 1 — Definir y preguntar
- [ ] Revisar el contrato con Áncora (ver aviso arriba).
- [ ] Pasarme el dossier y ajustar este documento.
- [ ] Analizar 3–4 competidores (talleres y servicios generales): cómo cobran y qué quejas tienen en sus reseñas.
- [ ] **5 entrevistas a conductores** (familia, amigos, compañeros): ¿cómo eligieron el último taller?, ¿qué les preocupó?, ¿pagarían por adelantado a través de una web?
- [ ] **5 conversaciones con talleres** (independientes, no de cadena): ¿cuántos clientes nuevos quieren?, ¿cuánto pagarían por uno?, ¿aceptarían una comisión del 10 %?
- **Entregable:** notas de entrevistas + 3 conclusiones.

### Semana 2 — Guion del proyecto
- [ ] Nombre provisional y dominio.
- [ ] Definir el **flujo completo**: el cliente pide → los talleres ofertan → el cliente elige → paga la señal → se hace el trabajo → reseña.
- [ ] Lista de categorías futuras (automoción → hogar → ...) con orden de apertura.
- [ ] Modelo de ingresos elegido y números básicos: cuánto gana la plataforma por trabajo y cuántos trabajos al mes hacen falta para cubrir costes.
- **Entregable:** documento "Guion del proyecto" v1.

### Semana 3 — Prueba manual en pequeño
- [ ] Landing con formulario: "Describe qué le pasa a tu coche y recibe presupuestos de talleres de Madrid".
- [ ] Apuntar **8–10 talleres** que acepten recibir peticiones por WhatsApp.
- [ ] Difundir entre conocidos, grupos de barrio y redes. Objetivo: **5–10 peticiones reales**.
- [ ] Gestionar cada petición a mano y apuntar los resultados.
- **Entregable:** hoja de peticiones con resultados (¿hubo ofertas?, ¿en cuánto tiempo?, ¿se contrató?).

### Semana 4 — Conclusiones y siguiente paso
- [ ] Analizar la prueba: qué funcionó, qué no, cuánto se habría ganado con comisión.
- [ ] Decidir: seguir con automoción, ajustar o probar otra categoría.
- [ ] Hoja de ruta de los meses 2–6 (incluida la web propia con Claude Code).
- **Entregable:** Guion del proyecto v2 + hoja de ruta.

---

## 6. Señales de que vamos bien (al final del mes)
- Al menos la mitad de los talleres contactados quieren recibir peticiones.
- Las peticiones reciben **2 o más ofertas en menos de 48 h**.
- Al menos 2–3 peticiones terminan en trabajo realizado.
- Algún taller dice "sí" a pagar un 10 % o una cuota por cliente conseguido.

---

## 7. Lo que NO hacemos este mes
- Programar la plataforma completa.
- Abrir varias categorías a la vez.
- Constituir una sociedad (aún no hace falta; si se cobra algo, se valora darse de alta como autónomo).
- Gastar en diseño, marca o publicidad a lo grande.
