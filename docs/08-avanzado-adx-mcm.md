# Capítulo 8 — Técnicas avanzadas y el salto a AdX

> **Aquí es donde se separan los que "ganan algo" de los que facturan de verdad.** El
> secreto peor guardado del sector: **AdSense casi nunca es donde está el dinero grande.**
> A partir de cierto tráfico, el mismo inventario puede pagar **2-3× más** a través de AdX
> y partners MCM. Si tu objetivo son 10.000 €+/mes, este capítulo es tu hoja de ruta de salida.

---

## 8.1 La verdad incómoda: AdSense es el suelo, no el techo

AdSense es perfecto para **empezar**: sin mínimos, fácil de integrar, fiable. Pero tiene
un techo. Los publishers serios lo usan como **peldaño hacia inventario premium.**

```
  AdSense          Ezoic          Mediavine         Raptive / AdX+MCM
  (empezar)   →   (crecer)   →    (premium)    →    (facturación seria)
  RPM 3-15€       RPM 5-25€       RPM 15-35€        RPM 20-40€+
```

> **El porqué técnico:** AdSense te da acceso a **una** fuente de demanda (la de Google). Un
> partner MCM o un setup de **header bidding** pone a **múltiples redes a pujar a la vez** por
> tu inventario. Más pujadores compitiendo = precio más alto por el **mismo** hueco. Es pura
> subasta: más competencia, mejor precio para ti.

---

## 8.2 Header bidding y AdX: por qué pagan más

| Concepto | Qué es | Por qué te paga más |
|----------|--------|---------------------|
| **AdSense** | Demanda de Google para publishers pequeños | Una sola fuente de puja |
| **Google AdX (Ad Exchange)** | El mercado premium de Google (parte de Google Ad Manager) | Acceso a demanda premium y pujas más altas; normalmente vía partner |
| **Header bidding** | Subasta simultánea entre varias redes **antes** de llamar al ad server | Múltiples redes compiten a la vez → precio óptimo |
| **Google Ad Manager (GAM)** | El "ad server" profesional que orquesta todo | Control total, múltiples fuentes de demanda |

> **Hecho:** el acceso directo a AdX y a header bidding suele requerir volumen y complejidad
> técnica alta. Por eso la vía práctica para el 95% de los publishers es un **partner MCM**,
> que te da todo eso "llave en mano".

---

## 8.3 Partners MCM (Multiple Customer Management): la vía práctica

Un partner MCM gestiona tu inventario a través de Google Ad Manager, te conecta a AdX +
header bidding + múltiples redes, y optimiza por ti. Tú pones el contenido; ellos, la
tecnología de monetización premium.

**Comparativa actualizada (datos 2025-2026):**

| Red | Requisito mínimo | RPM típico (sesión) | Notas 2026 |
|-----|------------------|---------------------|------------|
| **AdSense** | Sin mínimo (calidad) | 3 – 15 € | Punto de partida universal |
| **Ezoic** | **~250.000 usuarios/mes** (subió en feb. 2026) | 5 – 25 € | Abandonó el mercado de publishers pequeños; ya no es el "primer salto" fácil |
| **Mediavine** | **50.000 sesiones/mes** | 15 – 35 € | Premium, excelente para tráfico de EE. UU. |
| **Raptive** (antes AdThrive) | **25.000 páginas vistas/mes** (bajó de 100k en oct. 2025) | 20 – 40 €+ | De los RPM más altos del mercado; gestión personalizada; ahora más accesible |

> **Novedad clave 2025-2026:** el tablero cambió. **Raptive bajó su umbral a 25.000 páginas
> vistas/mes** (antes 100k), volviéndose accesible mucho antes. **Ezoic subió a ~250.000
> usuarios/mes**, dejando de ser el salto fácil para principiantes. **Traducción práctica:**
> hoy, para tráfico de calidad Tier 1, **Raptive o Mediavine son a menudo el objetivo directo**
> tras AdSense, sin pasar necesariamente por Ezoic.

### La hoja de ruta de migración recomendada (2026)

1. **0 → 25k páginas vistas/mes:** AdSense (+ optimización del Cap. 7). Construye tráfico.
2. **25k páginas vistas/mes:** aplica a **Raptive** (si tu tráfico es mayoritariamente Tier 1
   y de calidad). Suele ser el mayor salto de RPM.
3. **50k sesiones/mes:** **Mediavine** es otra gran opción premium.
4. **Volumen alto + capacidad técnica:** setup propio de **GAM + header bidding** o partner
   avanzado para exprimir el último 10-20%.

> ⚠️ **Requisito transversal:** los partners premium exigen **tráfico de calidad** (real,
> mayoritariamente orgánico, buena parte Tier 1) y cumplimiento de políticas. El tráfico
> comprado o de baja calidad te descarta. Todo lo aprendido en los Caps. 2-6 es el billete
> de entrada.

---

## 8.4 Ad refresh: la técnica que sube el RPM un 20-40%

El **ad refresh** recarga un anuncio (pide una nueva puja) cuando se cumplen ciertas
condiciones, generando una nueva impresión del mismo hueco.

> **Experiencia del sector:** un ad refresh **bien implementado** puede subir el RPM un
> **20-40%.** Pero **mal implementado viola políticas** y arriesga la cuenta. La diferencia
> está en los detalles.

**Cómo hacerlo BIEN (respetando políticas):**
- ✅ Refresca **solo anuncios en viewport** (que el usuario está viendo).
- ✅ Basado en **tiempo (p. ej. cada 30-60 s)** o en **interacción/scroll**, no en bucle ciego.
- ✅ Solo en usuarios **activos** (que hacen scroll, se mueven), no en pestañas abandonadas.
- ✅ Con **límites de frecuencia** razonables por sesión.
- ✅ Preferiblemente vía un **partner/GAM** que lo gestione conforme a políticas.

**Cómo NO hacerlo (te suspende):**
- 🚫 Refrescar cada pocos segundos en bucle.
- 🚫 Refrescar anuncios fuera de pantalla o en usuarios inactivos.
- 🚫 Inflar impresiones artificialmente sin interacción real.

> ⚠️ **Aviso:** el ad refresh con AdSense "puro" está sujeto a políticas estrictas y no
> siempre es viable. Es una de las razones para migrar a **GAM/MCM**, donde el refresh
> conforme a políticas está soportado y gestionado. No improvises refresh en AdSense sin
> conocer bien las reglas.

---

## 8.5 Otras técnicas avanzadas de maximización

| Técnica | Qué hace | Ganancia potencial | Complejidad |
|---------|----------|--------------------|-------------|
| **Header bidding / prebid** | Múltiples redes pujan a la vez | 🟢 Alta (10-30%+) | 🔴 Alta (o vía MCM) |
| **Price floors dinámicos** | Fija pujas mínimas óptimas por hueco/geo | 🟡 Media | 🔴 Alta |
| **Lazy loading avanzado** | Solo carga anuncios que se verán | 🟡 Media (viewability) | 🟢 Baja |
| **Ad refresh inteligente** | Nuevas impresiones conforme a políticas | 🟢 Alta (20-40%) | 🟡 Media (vía MCM) |
| **Formatos premium** (video outstream, native) | CPMs más altos | 🟢 Alta | 🟡 Media |
| **Optimización por geo/dispositivo** | Layout y floors por segmento | 🟡 Media | 🟡 Media |
| **Consent optimization (CMP)** | Maximiza consentimiento → más demanda | 🟡 Media | 🟢 Baja |

---

## 8.6 ¿Cuándo NO saltar todavía?

Honestidad profesional: no corras a migrar antes de tiempo.

- ❌ **Si no cumples el umbral de tráfico:** te rechazarán; consolida tráfico primero.
- ❌ **Si tu tráfico no es de calidad/Tier 1:** el salto de RPM será decepcionante; algunos
  partners ni te aceptan.
- ❌ **Si aún no has exprimido la optimización de AdSense (Cap. 7):** primero saca el máximo
  a lo que tienes; el salto a MCM multiplica una base ya optimizada, no arregla un layout malo.
- ❌ **Si vas a incumplir la exclusividad:** algunos partners exigen exclusividad; lee la letra pequeña.

> **Regla:** el salto a MCM **multiplica** lo que ya funciona. Primero construye tráfico de
> calidad y un layout optimizado; entonces el ×2-3 de RPM cae sobre una base sólida.

---

## 8.7 Errores comunes en técnicas avanzadas

- ❌ Ad refresh agresivo en AdSense → suspensión.
- ❌ Migrar a MCM con tráfico de baja calidad → rechazo o RPM decepcionante.
- ❌ Quedarse en AdSense por comodidad con 100k+ visitas de calidad → dejas la mitad del dinero.
- ❌ Montar header bidding a mano sin conocimiento → complejidad que no compensa (usa MCM).
- ❌ No leer la exclusividad/condiciones del partner → sorpresas contractuales.
- ❌ Elegir partner solo por el RPM prometido, ignorando soporte, pagos y requisitos.

---

## ✅ Checklist del Capítulo 8

- [ ] Entiendo que AdSense es el suelo y el dinero grande está en AdX/MCM.
- [ ] Conozco los umbrales 2026: Raptive 25k páginas vistas, Mediavine 50k sesiones, Ezoic ~250k usuarios.
- [ ] Tengo una hoja de ruta de migración según mi tráfico y calidad (Tier 1).
- [ ] He optimizado AdSense (Cap. 7) **antes** de plantear el salto.
- [ ] Si uso ad refresh, es conforme a políticas (viewport, tiempo, usuario activo, vía MCM).
- [ ] He verificado requisitos, exclusividad y condiciones de pago del partner objetivo.
- [ ] Mi tráfico es de calidad y mayoritariamente orgánico (billete de entrada a premium).

---

**Fuentes de referencia:**
- [Raptive vs Mediavine vs Ezoic 2025](https://thedigitalmalik.com/raptive-vs-mediavine-vs-ezoic/)
- [The new math behind premium ad network approvals (PPC.land)](https://ppc.land/is-your-site-finally-ready-the-new-math-behind-premium-ad-network-approvals/)
- [Display Ad Traffic Requirements (Blogging Guide)](https://bloggingguide.com/display-ad-traffic-requirements/)

*Siguiente: [Capítulo 9 → Diversificación de ingresos](09-diversificacion.md)*
