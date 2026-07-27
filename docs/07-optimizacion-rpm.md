# Capítulo 7 — Optimización del RPM: ubicación, formatos y densidad

> **La palanca más rentable que existe.** Aquí ganas más con el **mismo tráfico**. El
> tráfico cuesta meses; la optimización del RPM cuesta días y sus efectos son inmediatos.
> Un salto de RPM de 8 € a 12 € es **+50% de ingresos sin una sola visita nueva.** Este
> capítulo se relee cada trimestre.

---

## 7.1 El cambio de mentalidad post-2024: de "cazar clics" a "maximizar viewability"

Recuerda del Capítulo 1: AdSense paga **por impresión/viewability**, no por clic. Esto
**cambia por completo** la estrategia de ubicación respecto a los tutoriales antiguos.

| ❌ Mentalidad antigua (pre-2024) | ✅ Mentalidad actual (2026) |
|----------------------------------|----------------------------|
| Poner anuncios donde generen clics | Poner anuncios donde se **vean** (viewability) |
| CTR como métrica reina | **Viewability y RPM** como métricas reinas |
| Ubicaciones agresivas/engañosas | Ubicaciones visibles pero respetuosas con la UX |
| "Más anuncios = más dinero" | Densidad óptima; el exceso baja el RPM y arriesga la cuenta |

> **Principio:** ahora el objetivo es que **cada anuncio se cargue rápido y sea visible el
> mayor tiempo posible** para el usuario, sin destruir la experiencia (que reduce páginas/
> sesión y viewability). UX y RPM van de la mano.

---

## 7.2 Las ubicaciones que más rinden (datos 2026)

**Basado en datos del sector 2025-2026:**

| Ubicación | Rendimiento | Notas |
|-----------|-------------|-------|
| **In-content tras el 2º-3º párrafo** | 🟢 CTR 0,30-0,80%, alta viewability | El usuario está enganchado. La estrella del contenido |
| **Sticky/anchor inferior en móvil** | 🟢 +22% CTR sin subir rebote | Con triggers: aparece tras ~5 s, se oculta al hacer scroll |
| **Anchor lateral en escritorio** | 🟢 Visibilidad no intrusiva | Buena para desktop |
| **Entre secciones (H2)** en artículos largos (1.500+) | 🟢 Alta | Ideal cada bloque temático |
| **Above the fold (primeros 600px)** | 🟢 Capta ~80% de la atención | Pero cuidado con el límite del 15% del viewport |
| **In-article anchor** | 🟢 +20-30% viewability vs. mid-content estándar | Formato muy eficiente |
| Sidebar (escritorio) | 🟡 Media | Sticky sidebar mejora la viewability |
| Footer | 🔴 Baja | Poca gente llega; baja viewability |

### Formatos y tamaños recomendados

| Formato | Tamaño | Mejor uso |
|---------|--------|-----------|
| **Rectángulo grande** | 336×280 / 300×250 | In-content (el más rentable) |
| **Leaderboard** | 728×90 | Above the fold en escritorio |
| **Banner móvil** | 320×100 / 320×50 | Móvil |
| **Sticky/anchor** | Responsive | Móvil y desktop, alto rendimiento |
| **Multiplex** | Responsive | Feed de "contenido relacionado" al final |
| **In-feed / in-article** | Responsive | Se integran de forma nativa en el contenido |

---

## 7.3 Auto Ads vs. ubicación manual: la gran decisión

AdSense ofrece dos filosofías. No hay una respuesta universal; depende de tu fase.

| | **Auto Ads** | **Ubicación manual** |
|---|-------------|----------------------|
| **Qué es** | Google decide dónde y cuántos anuncios poner con IA | Tú colocas cada unidad donde quieres |
| **Esfuerzo** | 🟢 Mínimo (pegar un código) | 🔴 Alto (configurar cada hueco) |
| **Control** | 🔴 Bajo | 🟢 Total |
| **Riesgo UX/CLS** | 🟡 Puede saturar o generar saltos | 🟢 Controlas la experiencia |
| **Optimización** | 🟢 Google testea automáticamente | Depende de tu pericia |
| **Ideal para** | Principiantes, sitios pequeños, empezar | Publishers que optimizan en serio |

**Estrategia recomendada por fases:**
1. **Al empezar:** Auto Ads (o híbrido) para no complicarte y dejar que Google aprenda.
2. **Al crecer:** pasa a **híbrido** — desactiva los formatos de Auto Ads que molestan
   (in-page/vignette intrusivos) y define **manualmente** tus mejores ubicaciones
   (in-content tras 2º párrafo, anchor móvil, entre secciones).
3. **Al optimizar en serio:** control manual + A/B testing (7.6), y valora Auto Ads solo
   para "rellenar" oportunidades que se te escapen.

> **Truco:** con Auto Ads activo, usa los **controles de Auto Ads** para limitar la
> densidad y desactivar formatos intrusivos (vignettes que tapan la pantalla). Ganas la
> automatización sin sacrificar la UX ni arriesgar políticas.

---

## 7.4 Densidad óptima: cuántos anuncios (menos es más de lo que crees)

El error #1 de RPM es **saturar de anuncios**. Intuitivamente parece que más anuncios =
más dinero. Es **falso** por encima de cierto punto.

**Por qué el exceso de anuncios REDUCE ingresos:**
- 🔻 **Baja el CPM:** demasiados huecos diluyen la puja; los de abajo casi no se ven (viewability baja).
- 🔻 **Baja las páginas/sesión:** la mala UX hace que la gente se vaya → menos impresiones totales.
- 🔻 **Empeora Core Web Vitals:** más scripts de anuncios = peor INP/CLS → peor SEO → menos tráfico.
- 🔻 **Riesgo de política:** Google penaliza páginas donde los anuncios cubren **>15% del
  viewport inicial** o rompen la experiencia (Cap. 3).

> **Regla de densidad:** empieza **conservador** (2-3 anuncios bien colocados en un artículo
> medio) y **sube solo si los datos lo justifican.** Mide el RPM de página **y** las páginas
> por sesión: si añadir un anuncio sube el RPM pero hunde las páginas/sesión, has perdido.
> Optimiza el **ingreso total por sesión**, no el RPM aislado.

**Guía orientativa por longitud de artículo:**

| Longitud | Anuncios in-content sugeridos |
|----------|-------------------------------|
| < 800 palabras | 1-2 |
| 800-1.500 | 2-3 |
| 1.500-3.000 | 3-4 (entre secciones) |
| 3.000+ | 4-5 (bien espaciados) |

+ 1 anchor móvil + (opcional) 1 sticky sidebar en escritorio. **Siempre con espacio
reservado (Cap. 4) para no generar CLS.**

---

## 7.5 Optimización técnica de la viewability (dinero directo)

Como ahora se paga por viewability, estas acciones son **ingreso puro**:

- ✅ **Lazy-load de anuncios:** carga cada anuncio justo antes de que entre en pantalla. Sube
  la viewability (se muestran solo los que se van a ver) y mejora la velocidad.
- ✅ **Reserva de espacio (`min-height`):** evita CLS y sube la viewability hasta un 50% (Cap. 4).
- ✅ **Sticky con triggers inteligentes:** el anchor que aparece tras ~5 s y se oculta al
  hacer scroll da +22% CTR sin subir el rebote.
- ✅ **Velocidad de carga (Cap. 4):** anuncios que cargan antes de que el usuario se vaya = impresiones cobradas.
- ✅ **Above the fold con moderación:** capta el 80% de la atención, pero respeta el 15% del viewport.

---

## 7.6 A/B testing: optimizar con datos, no con intuición

Los profesionales **no adivinan**; prueban. Nunca asumas que un layout es mejor: mídelo.

**Proceso de experimentación:**
1. **Define una hipótesis:** "mover el anuncio del sidebar a in-content tras el 2º párrafo
   subirá el RPM sin bajar las páginas/sesión".
2. **Usa Experimentos de AdSense** o herramientas del partner (si estás en MCM, Cap. 8).
3. **Cambia una variable cada vez** (ubicación, formato, densidad).
4. **Deja correr suficiente tiempo/tráfico** para significancia estadística (no decidas con 2 días).
5. **Mide el ingreso total por sesión**, no solo el RPM. Y vigila páginas/sesión y CWV.
6. **Documenta y estandariza** el ganador; siguiente experimento.

> **Qué medir siempre juntos:** RPM de página, páginas por sesión, viewability, tiempo en
> página y Core Web Vitals. Una mejora de RPM que empeora cualquiera de los otros puede ser
> una pérdida neta. La foto completa es lo que importa.

---

## 7.7 Segmentación por dispositivo, país y contenido

- **Dispositivo:** móvil y escritorio necesitan layouts distintos. El **anchor móvil** es
  clave; en escritorio, el **sticky sidebar** y el leaderboard funcionan mejor.
- **País:** si tienes tráfico mixto, tu RPM medio esconde grandes diferencias. Analiza el
  RPM por país en AdSense; considera **enfocar contenido a Tier 1** para subir la media (Cap. 2).
- **Tipo de contenido:** tus artículos comerciales (alto CPC) toleran y merecen ubicaciones
  más prominentes que los informacionales de relleno.

---

## 7.8 Errores comunes de optimización de RPM

- ❌ Saturar de anuncios creyendo que gana más → baja CPM, páginas/sesión y CWV; riesgo de política.
- ❌ Optimizar el CTR (métrica obsoleta) en vez de la viewability y el RPM.
- ❌ No reservar espacio → CLS + viewability −50% (dinero perdido en cada carga).
- ❌ Decidir layouts por intuición sin A/B testing.
- ❌ Mirar solo el RPM y no las páginas/sesión → falsas victorias.
- ❌ Auto Ads sin controlar densidad → saturación e intrusividad.
- ❌ El mismo layout en móvil y escritorio → desaprovechas ambos.
- ❌ Ignorar el RPM por país/dispositivo → pierdes oportunidades de segmentación.
- ❌ No revisar el layout en meses → el mercado y tu contenido cambian.

---

## ✅ Checklist del Capítulo 7

- [ ] Anuncio in-content tras el 2º-3º párrafo (la mejor ubicación).
- [ ] Anchor/sticky móvil con triggers inteligentes activado.
- [ ] Densidad conservadora ajustada a la longitud; nunca >15% del viewport inicial.
- [ ] Espacio de todos los anuncios reservado (anti-CLS, +viewability).
- [ ] Lazy-load de anuncios activo.
- [ ] Decisión consciente Auto Ads / manual / híbrido según mi fase.
- [ ] A/B testing en marcha, cambiando una variable cada vez.
- [ ] Mido RPM **y** páginas/sesión **y** CWV juntos (ingreso total por sesión).
- [ ] Layouts diferenciados por dispositivo.
- [ ] Revisión trimestral del layout y del RPM por país/dispositivo.

---

**Fuentes de referencia:**
- [Best AdSense Placements 2025 (MonetizeMore)](https://www.monetizemore.com/blog/best-adsense-placements/)
- [High-Performing Ad Layouts (TheAdCompare)](https://theadcompare.com/advertising/high-performing-ad-layouts/)
- [Top Ad Formats for Publishers 2025 (OptiDigital)](https://optidigital.com/resources/blog/top-ad-formats-for-publishers-in-2025/)

*Siguiente: [Capítulo 8 → Técnicas avanzadas y salto a AdX](08-avanzado-adx-mcm.md)*
