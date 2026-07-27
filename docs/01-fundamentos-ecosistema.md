# Capítulo 1 — Fundamentos y ecosistema publicitario

> **Objetivo del capítulo:** que entiendas *cómo se genera realmente el dinero* antes de
> tocar nada. El 90% de los principiantes optimizan a ciegas porque no saben qué mueve
> cada euro. Cuando entiendas la subasta y las métricas, cada decisión posterior tendrá
> sentido.

---

## 1.1 Qué es AdSense y dónde encaja en el ecosistema

Google AdSense es la herramienta que permite a un **publisher** (tú, el dueño de la web)
mostrar anuncios en su sitio y cobrar por ellos. Pero AdSense es solo **una pieza** de un
sistema mayor. Para dominarlo hay que ver el tablero completo:

```
   ANUNCIANTE                GOOGLE (intermediario)              PUBLISHER (TÚ)
  ┌──────────┐    puja    ┌────────────────────────┐   muestra  ┌──────────┐
  │ Google   │──────────▶│  Subasta en tiempo real │──────────▶│ Tu web   │
  │ Ads (DSP)│            │  (Ad Exchange / AdSense)│           │ + AdSense│
  └──────────┘            └────────────────────────┘           └──────────┘
       │                            │                                │
   Paga por espacio         Se queda una comisión          Recibe ~68% neto
```

- **Anunciante:** empresas que quieren aparecer. Pujan con dinero por mostrarse a tu
  audiencia, normalmente a través de **Google Ads** (la plataforma de compra).
- **Google:** organiza la subasta, decide qué anuncio gana y cobra una comisión.
- **Publisher (tú):** aportas el espacio (tu web) y la audiencia. Cobras lo que queda.

> **Hecho (documentado por Google):** el publisher se queda con el **80% de los ingresos
> de AdSense for content** *después* de que la plataforma de compra tome su parte. En la
> práctica, el reparto total deja al editor con **~68%** de lo que paga el anunciante.
> Esto es importante: cuando ves "RPM de 10 €", el anunciante pagó bastante más.

---

## 1.2 La subasta publicitaria: cómo se decide cada anuncio

Cada vez que alguien carga una página tuya con un hueco de anuncio, ocurre una **subasta
en tiempo real (RTB, Real-Time Bidding)** en milisegundos:

1. Tu web envía una señal: "tengo un hueco de 300×250 que ve un usuario de España
   interesado en hipotecas".
2. Cientos de anunciantes (vía Google Ads y otras plataformas) pujan por ese hueco.
3. Google ejecuta la subasta y **gana la puja más alta** (con matices de calidad).
4. Se muestra el anuncio y tú cobras.

**Qué determina cuánto se puja por TU hueco (y por tanto cuánto cobras):**

| Factor | Por qué importa | Lo controlas tú |
|--------|-----------------|-----------------|
| **País del usuario** | Anunciantes de EE. UU./UK pagan mucho más | Parcial (eliges el idioma/mercado) |
| **Tema/intención** | "Hipoteca" vale 20× más que "frases bonitas" | ✅ Sí (eliges nicho, Cap. 2) |
| **Época del año** | Q4 (Black Friday, Navidad) sube las pujas | No |
| **Competencia de anunciantes** | Más pujas = precio más alto | Parcial (nicho) |
| **Calidad y viewability del hueco** | Un anuncio que se ve vale más | ✅ Sí (layout, Cap. 7) |
| **Datos del usuario** | Cookies, intención de compra | No (y cada vez menos, por privacidad) |

### El cambio a subasta de primer precio

> **Hecho:** Google movió la subasta de AdSense de **segundo precio** a **primer precio**.
> En segundo precio, el ganador pagaba lo que pujó el segundo; en primer precio paga lo
> que pujó. Esto simplifica la compra para los anunciantes y, en la práctica, hace el
> mercado más transparente. Para ti como publisher no cambia la operativa, pero conviene
> saberlo si lees documentación técnica o negocias con partners.

---

## 1.3 El cambio clave de 2024: de pago por clic a pago por impresión

Este es uno de los cambios más importantes de la última década y **muchos tutoriales
viejos siguen enseñándolo mal**.

> **Hecho (anunciado por Google, implementado en 2024):** AdSense pasó de pagar
> principalmente **por clic (CPC)** a pagar **por impresión (CPM)**, alineándose con el
> estándar del sector display. Es decir: **ahora cobras principalmente por que el anuncio
> se muestre y se vea, no por que el usuario haga clic.**

**Consecuencias prácticas enormes:**

- ❌ **Muere la obsesión por el CTR.** Ya no se trata de "engañar" al usuario para que
  haga clic. Perseguir clics con ubicaciones tramposas ahora es contraproducente
  (arruina la UX sin subir ingresos y arriesga tu cuenta).
- ✅ **Reina la VIEWABILITY.** Lo que ahora se paga es que el anuncio **se cargue y sea
  visible**. Un anuncio que carga pero el usuario nunca ve (porque se fue antes) no se
  paga bien.
- ✅ **La velocidad y el tiempo en página valen dinero directo.** Si tus anuncios no
  terminan de cargar antes de que el usuario se vaya → impresión perdida → ingreso
  perdido. Por eso el Capítulo 4 (Core Web Vitals) es literalmente una palanca de RPM.

> **Nota de honestidad:** Google declaró que *no esperaba* que los ingresos de los
> publishers cambiaran de forma significativa con esta transición. En la práctica, la
> experiencia de editores es mixta: a quien tenía buen contenido y mala UX, la viewability
> le importa ahora más que nunca.

---

## 1.4 El diccionario que DEBES dominar: CPC, CPM, RPM, CTR, Viewability

Estas cinco métricas son el lenguaje del negocio. Confundirlas es como intentar cocinar
sin saber la diferencia entre gramos y litros.

| Métrica | Qué significa | Fórmula | Quién la "posee" |
|---------|---------------|---------|------------------|
| **CPC** | Coste Por Clic — lo que paga el anunciante por un clic | — | El anunciante |
| **CPM** | Coste Por Mil impresiones — lo que se paga por 1.000 anuncios mostrados | — | El mercado |
| **CTR** | Click-Through Rate — % de anuncios que reciben clic | (Clics / Impresiones) × 100 | Tu audiencia + layout |
| **RPM** | Revenue Per Mille — **lo que TÚ ganas por cada 1.000 visitas/páginas** | (Ingresos / Páginas vistas) × 1000 | **Tu métrica reina** |
| **Viewability** | % de anuncios que se muestran de forma visible (≥50% del área ≥1 seg) | — | Tu layout + velocidad |

### El RPM es tu estrella polar

De todas, **el RPM de página es la métrica que resume tu eficiencia de monetización.**
Traduce todo (nicho, país, layout, velocidad) a un solo número: *cuánto ganas por cada
mil visitas*. Es la métrica que debes optimizar obsesivamente.

**Dos tipos de RPM que no debes confundir:**

- **RPM de página:** ingresos por cada 1.000 páginas vistas. Es el que importa para el negocio.
- **RPM de sesión:** ingresos por cada 1.000 sesiones (visitas). Los partners premium
  (Mediavine, Raptive) suelen hablar en **RPM de sesión**, que es mayor porque una
  sesión suele incluir varias páginas.

> ⚠️ **Error clásico al comparar redes:** comparar el "RPM de página" de AdSense con el
> "RPM de sesión" de Mediavine y concluir cosas erróneas. Asegúrate siempre de comparar la
> misma métrica. (Más en el Capítulo 8.)

---

## 1.5 Cómo se conectan las métricas: el flujo del dinero

```
   CPM del mercado ──┐
                     ├──▶ Ingresos del hueco ──┐
   Viewability ──────┘                         │
                                               ├──▶ RPM de página ──▶ 💶 Facturación
   Nº de huecos por página ────────────────────┤
                                               │
   Páginas vistas (tráfico × páginas/sesión) ──┘
```

**Lectura estratégica:** puedes aumentar la facturación por **tres vías independientes**,
y lo inteligente es trabajarlas en paralelo:

1. **Más tráfico** → Capítulos 5 y 6 (SEO y contenido).
2. **Más páginas por sesión** → Capítulo 4 (UX, enlazado interno) y 6 (clusters).
3. **Más RPM** → Capítulos 2 (nicho), 7 (optimización) y 8 (AdX/MCM).

---

## 1.6 Ejemplo numérico completo (para que "haga clic" mentalmente)

Sitio de finanzas personales, audiencia mayoritariamente de EE. UU.:

- 200.000 páginas vistas/mes.
- 2 huecos de anuncio por página → 400.000 impresiones.
- CPM medio de esos huecos: 12 €.
- Viewability del 70%.

```
Impresiones "pagables" ≈ 400.000 × 0,70 = 280.000
Ingresos ≈ (280.000 / 1000) × 12 € = 3.360 €/mes
RPM de página ≈ (3.360 / 200.000) × 1000 = 16,8 €
```

Ahora observa el efecto de **mejorar solo la viewability** del 70% al 85% (subiendo
velocidad y reservando el espacio del anuncio, Cap. 4):

```
Impresiones pagables ≈ 400.000 × 0,85 = 340.000
Ingresos ≈ (340.000 / 1000) × 12 € = 4.080 €/mes  → +720 €/mes SIN una sola visita nueva
```

**Esto es lo que significa "optimizar el RPM": ganar más con el mismo tráfico.** Es la
palanca más rentable que existe, porque el tráfico cuesta meses de trabajo y la
optimización cuesta días.

---

## 1.7 Errores comunes en los fundamentos

- ❌ **Creer que AdSense paga por clic** (información obsoleta pre-2024). Diseñas todo mal.
- ❌ **Perseguir CTR** con ubicaciones agresivas → arruinas UX, ahora sin recompensa.
- ❌ **Ignorar la viewability** → dejas dinero sobre la mesa en cada carga de página.
- ❌ **No saber tu RPM de página** → navegas sin instrumentos.
- ❌ **Comparar RPM de página con RPM de sesión** → decisiones basadas en datos falsos.
- ❌ **Pensar que el tráfico lo es todo** → 500.000 visitas a RPM 3 € valen menos que
  150.000 a RPM 15 €.

---

## ✅ Checklist de dominio del Capítulo 1

- [ ] Entiendo la subasta: anunciante → Google → publisher, y quién se queda qué.
- [ ] Sé que AdSense paga **por impresión/viewability**, no por clic (desde 2024).
- [ ] Distingo CPC, CPM, CTR, RPM y Viewability, y sé cuál "poseo" yo.
- [ ] Tengo claro que el **RPM de página** es mi estrella polar.
- [ ] No confundo RPM de página con RPM de sesión.
- [ ] Entiendo que puedo crecer por 3 vías: tráfico, páginas/sesión y RPM.

---

**Fuentes de referencia de este capítulo:**
- [Google — Move to a first-price auction](https://blog.google/products/adsense/our-move-to-a-first-price-auction/)
- [AdSense cambio a pago por impresión 2024 (9to5Google)](https://9to5google.com/2023/11/02/google-adsense-payments-2024/)
- [Nueva estructura de pagos de AdSense (MonetizeMore)](https://www.monetizemore.com/blog/how-the-new-adsense-payment-structure-benefits-you/)

*Siguiente: [Capítulo 2 → Elección del nicho rentable](02-nicho-rentable.md)*
