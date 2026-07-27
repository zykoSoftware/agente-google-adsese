# Capítulo 4 — Arquitectura web y Core Web Vitals

> **Aquí la técnica se convierte en dinero.** Desde que AdSense paga por impresión/
> viewability (Cap. 1), la velocidad de tu web **es una palanca directa de RPM**, no solo
> de SEO. Una web lenta pierde impresiones (ingresos) y posiciones (tráfico) a la vez.
> Este capítulo es doblemente rentable.

---

## 4.1 Por qué la velocidad es dinero (no solo SEO)

Dos cadenas causales que debes interiorizar:

**Cadena de ingresos:**
```
Web lenta → los anuncios cargan tarde → el usuario se va antes de que se muestren
         → impresiones perdidas → ingresos perdidos
```

**Cadena de tráfico:**
```
Web lenta → mala experiencia → Core Web Vitals malos → peor ranking en Google
         → menos tráfico → menos ingresos
```

> **Caso real documentado (web.dev / Netzwelt):** al comprometerse con los Core Web Vitals,
> este publisher logró **+27% de páginas vistas, viewability por encima del 75% y +18% de
> ingresos publicitarios.** La UX y los ingresos se optimizan **de la mano**, no en conflicto.

---

## 4.2 Los Core Web Vitals explicados (valores 2026)

Google mide la experiencia real de tus usuarios con tres métricas. Un "aprobado" exige que
las tres pasen en el **percentil 75** de las visitas reales.

| Métrica | Qué mide | 🟢 Bueno | 🟠 Mejorable | 🔴 Malo |
|---------|----------|----------|--------------|---------|
| **LCP** (Largest Contentful Paint) | Cuánto tarda en cargar el elemento principal | **< 2,5 s** | 2,5 – 4 s | > 4 s |
| **INP** (Interaction to Next Paint) | Cuánto tarda la página en responder a un clic/toque | **< 200 ms** | 200 – 500 ms | > 500 ms |
| **CLS** (Cumulative Layout Shift) | Cuánto "salta" el diseño mientras carga | **< 0,1** | 0,1 – 0,25 | > 0,25 |

> **Actualización importante:** **INP sustituyó a FID** como Core Web Vital (marzo 2024).
> Si lees guías que hablan de "FID", están desactualizadas. INP es más exigente: mide la
> capacidad de respuesta durante **toda** la visita, no solo la primera interacción.

> **Dato de contexto:** según el Web Almanac 2025, **solo el 48% de las páginas móviles**
> pasan los tres Core Web Vitals, y el **LCP es el más difícil** (solo ~62% de móviles lo
> aprueban). Si tú los pasas, ya estás por delante de la mitad de internet.

---

## 4.3 El CLS y los anuncios: el error que mata la viewability Y la UX

El **CLS** (saltos de diseño) merece atención especial porque los anuncios son su
**principal causa**: un anuncio carga, empuja el contenido hacia abajo, el usuario hace
clic sin querer o pierde su sitio → mala UX **y** clic accidental (riesgo de política).

> **Dato:** los sitios que **no reservan el espacio del anuncio** con contenedores de
> `min-height` sufren hasta un **50% menos de viewability**. Es decir: no reservar el
> espacio te cuesta CLS (SEO), UX **y** dinero directo.

**La solución (crítica):** **reserva siempre el espacio del anuncio antes de que cargue.**

```css
/* Contenedor de anuncio con espacio reservado: evita el salto de diseño (CLS) */
.ad-slot {
  min-height: 280px;   /* la altura del formato que vas a servir */
  display: block;
  margin: 24px auto;
  text-align: center;
  /* opcional: un fondo sutil mientras carga */
  background: #f6f7f9;
}
@media (max-width: 600px) {
  .ad-slot { min-height: 250px; } /* ajusta al formato móvil */
}
```

**Reglas anti-CLS con anuncios:**
- ✅ Reserva la altura de cada hueco con `min-height`/contenedor de tamaño fijo.
- ✅ Evita insertar anuncios que empujen contenido ya visible ("above the fold").
- ✅ Precarga fuentes y define tamaños de imágenes (`width`/`height`) para no sumar CLS.

---

## 4.4 Cómo mejorar cada métrica (procesos accionables)

### Mejorar el LCP (< 2,5 s)

| Palanca | Acción | Impacto |
|---------|--------|---------|
| Hosting | Usa hosting rápido (SSD/NVMe, buen TTFB). El hosting barato mata el LCP | 🟢 Alto |
| CDN | Sirve estáticos desde una CDN (Cloudflare, etc.) | 🟢 Alto |
| Imágenes | Formato **WebP/AVIF**, comprimidas, lazy-load (menos la imagen LCP), `srcset` responsivo | 🟢 Alto |
| Imagen principal | **Precarga** la imagen LCP (`<link rel="preload">`), NO le pongas lazy-load | 🟢 Alto |
| CSS/JS | Minimiza y elimina render-blocking; CSS crítico inline | 🟡 Medio |
| Caché | Caché de página completa (plugins de caché en WordPress) | 🟢 Alto |

### Mejorar el INP (< 200 ms)

| Palanca | Acción | Impacto |
|---------|--------|---------|
| JavaScript | Reduce el JS de terceros; difiere lo no crítico (`defer`/`async`) | 🟢 Alto |
| Scripts pesados | Menos plugins; audita qué scripts bloquean el hilo principal | 🟢 Alto |
| Anuncios/tags | Carga los scripts de anuncios de forma asíncrona y **lazy** | 🟡 Medio |
| Tareas largas | Divide tareas JS largas; evita ejecutar todo al cargar | 🟡 Medio |

### Mejorar el CLS (< 0,1)

- ✅ Reserva espacio de anuncios (apartado 4.3).
- ✅ Dimensiones explícitas en imágenes y vídeos.
- ✅ Reserva espacio para banners de cookies, embeds y widgets.
- ✅ Evita inyectar contenido dinámico por encima de lo visible.

---

## 4.5 El stack recomendado (elige según nivel)

| Nivel | Stack | Ventaja | Inconveniente |
|-------|-------|---------|---------------|
| 🟢 **Principiante** | WordPress + tema ligero (GeneratePress, Kadence, Astra) + plugin de caché + Cloudflare | Rápido de montar, ecosistema enorme, fácil de monetizar | Requiere mantenimiento y buenos plugins |
| 🟡 **Intermedio** | WordPress bien optimizado + hosting gestionado (buen TTFB) + CDN | Equilibrio potencia/facilidad | Coste algo mayor |
| 🔵 **Avanzado** | Static/JAMstack (Astro, Next.js, Hugo) + CDN | Velocidad máxima, CWV excelentes | Más complejidad técnica; integrar anuncios cuesta más |

> **Recomendación honesta:** para el 90% de los publishers, **WordPress con un tema ligero
> y bien optimizado es la mejor relación esfuerzo/resultado.** No te obsesiones con stacks
> exóticos: un WordPress bien montado pasa los Core Web Vitals sin problema. La velocidad
> se pierde por **temas pesados, exceso de plugins y hosting malo**, no por WordPress en sí.

**Temas a EVITAR:** los "multipropósito" cargados de funciones (page builders pesados como
ciertos usos de Divi/Elementor sin optimizar). Cada función extra es JS que penaliza INP.

---

## 4.6 Diseño móvil primero (mobile-first): donde se juega el partido

> **Hecho:** la mayoría del tráfico web es móvil, Google indexa en **mobile-first**, y la
> revisión de AdSense se hace principalmente en móvil. Si tu web va mal en móvil, lo demás
> da igual.

**Checklist móvil:**
- ✅ Texto legible sin zoom (16px+ de base).
- ✅ Botones y enlaces con área táctil suficiente (evita clics accidentales en anuncios).
- ✅ Anuncios que no rompen el layout ni tapan contenido.
- ✅ Nada de intersticiales intrusivos que tapen el contenido al llegar (Google penaliza).
- ✅ Menú hamburguesa claro, navegación con el pulgar.
- ✅ El **sticky/anchor de móvil** (Cap. 7) bien configurado: es de los formatos que más pagan.

---

## 4.7 Arquitectura de la información: estructura que monetiza

La estructura del sitio afecta a tres cosas a la vez: SEO, páginas por sesión (más
ingresos) y autoridad temática.

```
        Home
          │
   ┌──────┼──────┐
 Categoría A  Categoría B  Categoría C   ← "silos" temáticos
   │            │            │
 [Pillar]    [Pillar]     [Pillar]        ← guía madre de cada tema (Cap. 6)
   │            │            │
 art·art·art  art·art·art  art·art·art    ← artículos de apoyo enlazados al pillar
```

**Principios:**
- **Silos temáticos:** agrupa el contenido por temas (categorías) coherentes. Refuerza la
  autoridad temática (Cap. 6) y ayuda a Google a entender de qué va tu sitio.
- **Enlazado interno fuerte:** cada artículo enlaza a su pillar y a artículos hermanos.
  Esto **sube las páginas por sesión** (más impresiones = más ingresos) y reparte autoridad.
- **Profundidad de clic baja:** cualquier artículo alcanzable en ≤3 clics desde la home.
- **Breadcrumbs (migas de pan):** mejoran UX, SEO y navegación.

> **Palanca de ingresos infravalorada:** subir las **páginas por sesión** de 1,3 a 2,0
> mediante buen enlazado interno y "artículos relacionados" puede subir tus ingresos ~50%
> **sin una sola visita nueva.** Recuerda la ecuación: Ingresos = Visitas × Páginas/sesión × RPM/1000.

---

## 4.8 Herramientas para medir (gratis)

| Herramienta | Para qué |
|-------------|----------|
| **PageSpeed Insights** | Core Web Vitals de campo (datos reales) + laboratorio, por URL |
| **Search Console → Core Web Vitals** | Estado agregado de todo el sitio, URLs con problemas |
| **Chrome DevTools (Lighthouse / Performance)** | Diagnóstico técnico profundo |
| **CrUX / web.dev** | Datos de campo reales de usuarios de Chrome |
| **GTmetrix / WebPageTest** | Análisis de cascada de carga detallado |

> **Regla:** optimiza contra **datos de campo (field data)** del percentil 75, no solo
> contra el laboratorio (lab). El campo es lo que Google usa para rankear.

---

## 4.9 Errores comunes de arquitectura y velocidad

- ❌ Hosting barato compartido con TTFB alto → LCP arruinado desde la base.
- ❌ Tema pesado + 30 plugins → INP por las nubes.
- ❌ No reservar espacio de anuncios → CLS malo + viewability −50%.
- ❌ Imágenes gigantes sin comprimir ni WebP → LCP lento y datos desperdiciados.
- ❌ Lazy-load en la imagen principal (LCP) → la retrasas en vez de acelerarla.
- ❌ Web bonita en escritorio y rota en móvil → pierdes el 60-70% del tráfico.
- ❌ Sitios "planos" sin silos ni enlazado interno → baja autoridad y 1 página/sesión.
- ❌ Perseguir un 100/100 en Lighthouse a costa de tiempo → busca "verde", no la perfección.

---

## ✅ Checklist del Capítulo 4

- [ ] LCP < 2,5 s, INP < 200 ms, CLS < 0,1 en **datos de campo** (móvil).
- [ ] Espacio de anuncios reservado con `min-height` (anti-CLS, +viewability).
- [ ] Hosting rápido (buen TTFB) + CDN + caché de página.
- [ ] Imágenes en WebP/AVIF, comprimidas, con dimensiones; LCP precargada, resto lazy.
- [ ] JS de terceros reducido y diferido; pocos plugins.
- [ ] Diseño impecable y probado en móvil (mobile-first).
- [ ] Silos temáticos + enlazado interno fuerte + breadcrumbs.
- [ ] Páginas por sesión medidas y en objetivo de subida.
- [ ] Todo verificado en PageSpeed Insights y Search Console.

---

**Fuentes de referencia:**
- [web.dev — Caso Netzwelt (+18% ingresos con CWV)](https://web.dev/case-studies/netzwelt)
- [web.dev — Correlating Core Web Vitals and ad revenue](https://web.dev/articles/cwv-impact-ad-revenue)
- [Core Web Vitals 2026 (corewebvitals.io)](https://www.corewebvitals.io/core-web-vitals)
- [Web Almanac 2025 — Performance](https://almanac.httparchive.org/en/2025/performance)

*Siguiente: [Capítulo 5 → SEO y estrategia de tráfico](05-seo-trafico.md)*
