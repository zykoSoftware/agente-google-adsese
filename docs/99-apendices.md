# Apéndices ejecutables

> El bloque para **actuar**. Aquí tienes el plan de 90 días, las checklists maestras, la
> calculadora de ingresos, el stack de herramientas, los KPIs, un glosario y una idea de
> arquitectura para automatizar el reporting con este mismo repositorio.

---

## A. Plan de acción de 90 días (de cero a monetizando)

> Asume dedicación seria y parte de cero. Los plazos de tráfico/ingresos reales llegan
> **después** (12-24 meses); estos 90 días construyen los **cimientos correctos** para que
> ese crecimiento ocurra.

### Mes 1 — Fundación (Caps. 1-4)

| Semana | Objetivos |
|--------|-----------|
| **1** | Estudiar fundamentos (Cap. 1). Elegir nicho con la matriz de decisión (Cap. 2). Validar CPC + dificultad + volumen. Decidir idioma/país. |
| **2** | Comprar dominio + hosting rápido. Montar WordPress + tema ligero. Configurar HTTPS, CDN, caché (Cap. 4). Crear las 5 páginas legales + CMP de cookies (Cap. 3). |
| **3** | Keyword research a fondo (Cap. 5): construir el banco de keywords y el primer cluster (pillar + spokes). Calendario editorial. Configurar GSC, GA4, GTM. |
| **4** | Escribir y publicar los primeros 8-10 artículos de calidad (Cap. 6). Optimización on-page. Verificar Core Web Vitals en verde (Cap. 4). |

### Mes 2 — Contenido y aprobación (Caps. 3, 5, 6)

| Semana | Objetivos |
|--------|-----------|
| **5-6** | Completar hasta 20-25 artículos originales de 1.000+ palabras. Completar el primer cluster. Enlazado interno. |
| **7** | Repasar la checklist de aprobación (Cap. 3). Pulir navegación, móvil, páginas legales. Verificar indexación en GSC. |
| **8** | **Solicitar AdSense.** Mientras esperas: seguir escribiendo y empezar el segundo cluster. Configurar captación de emails (lead magnet, Cap. 9). |

### Mes 3 — Monetización y optimización (Caps. 7, 9)

| Semana | Objetivos |
|--------|-----------|
| **9** | Una vez aprobado: implementar anuncios (empezar con Auto Ads o híbrido, Cap. 7). Reservar espacios (anti-CLS). |
| **10** | Añadir afiliación al contenido comercial (Cap. 9). Declarar afiliaciones. Primeros formularios de email. |
| **11** | Optimización de RPM: ubicación in-content tras 2º párrafo, anchor móvil, densidad conservadora (Cap. 7). Medir RPM + páginas/sesión. |
| **12** | Revisar KPIs del primer mes. Ajustar layout con datos. Planificar los siguientes clusters. Establecer la cadencia sostenible de publicación. |

**Al final de los 90 días deberías tener:** sitio técnicamente sólido, 30-40 artículos de
calidad en 2-3 clusters, AdSense aprobado y monetizando, afiliación y captación de email
activas, y un sistema de trabajo. **A partir de aquí: consistencia durante 12-24 meses.**

---

## B. Checklist maestra de lanzamiento (todo en una página)

**Técnica y legal:**
- [ ] Dominio propio + hosting rápido (buen TTFB) + CDN + caché
- [ ] HTTPS en todo el sitio
- [ ] Core Web Vitals en verde (LCP <2,5s / INP <200ms / CLS <0,1) en móvil
- [ ] Espacio de anuncios reservado (anti-CLS)
- [ ] 5 páginas legales (About, Contacto, Privacidad, Aviso legal, Términos)
- [ ] CMP de cookies (obligatorio con tráfico UE)
- [ ] GSC + GA4 + GTM configurados

**Contenido:**
- [ ] Nicho validado (CPC alto + dificultad asumible + volumen + intención)
- [ ] 20-25+ artículos originales de 1.000+ palabras
- [ ] Organizado en clusters (pillar + spokes) con enlazado interno
- [ ] E-E-A-T: bios de autor, experiencia real, fuentes
- [ ] Sin thin content ni AI-spam sin revisar

**Monetización:**
- [ ] AdSense aprobado e implementado (ubicaciones óptimas, densidad conservadora)
- [ ] Afiliación en contenido comercial (declarada)
- [ ] Captación de emails activa
- [ ] KPIs monitorizados mensualmente

---

## C. Calculadora de ingresos (modela tu negocio)

**Fórmula base:**
```
Ingresos mensuales = (Páginas vistas / 1000) × RPM de página
Páginas vistas = Sesiones × Páginas por sesión
```

**Tabla de escenarios (para fijar objetivos realistas):**

| Sesiones/mes | Páginas/sesión | Páginas vistas | RPM | Ingresos/mes |
|--------------|----------------|----------------|-----|--------------|
| 10.000 | 1,5 | 15.000 | 8 € | 120 € |
| 50.000 | 1,8 | 90.000 | 12 € | 1.080 € |
| 100.000 | 2,0 | 200.000 | 15 € | 3.000 € |
| 250.000 | 2,0 | 500.000 | 20 € | 10.000 € |
| 250.000 | 2,0 | 500.000 | 35 € (MCM) | 17.500 € |
| 500.000 | 2,2 | 1.100.000 | 25 € | 27.500 € |

**Lecciones de la tabla:**
- Para **10.000 €/mes** necesitas, aprox., **500.000 páginas vistas/mes a RPM 20 €** (nicho
  rentable + Tier 1) — o **la mitad de tráfico si saltas a MCM** (RPM 35 €).
- **Subir el RPM y las páginas/sesión** puede duplicar ingresos **sin más tráfico** (compara
  filas 4 y 5). Por eso los Caps. 4, 7 y 8 son tan rentables.
- Un RPM de 3 € (nicho pobre) exigiría **~3,3 millones** de páginas vistas para esos 10.000 €.
  **El nicho lo cambia todo** (Cap. 2).

> **Ejercicio:** fija tu objetivo de ingresos, tu RPM realista (por nicho/país) y calcula
> hacia atrás las páginas vistas que necesitas. Eso te dice cuántos artículos y cuánto
> tráfico perseguir. Convierte un sueño en un plan.

---

## D. Stack de herramientas recomendado

| Categoría | Herramientas | Nota |
|-----------|--------------|------|
| **CMS** | WordPress + tema ligero (GeneratePress, Kadence, Astra) | El estándar del publisher |
| **Hosting** | Hosting con buen TTFB (gestionado si puedes) | No escatimes: afecta LCP y todo lo demás |
| **CDN / seguridad** | Cloudflare | Velocidad + protección |
| **Caché** | Plugin de caché (WP Rocket u opciones gratuitas) | Crítico para CWV |
| **Analítica** | Google Analytics 4, Search Console, Tag Manager | Gratis, imprescindibles |
| **Keyword research / SEO** | Google Keyword Planner (CPC), Ahrefs / Semrush / Ubersuggest | Planner para CPC; el resto para KD y backlinks |
| **Velocidad** | PageSpeed Insights, GTmetrix, WebPageTest | Medir CWV de campo |
| **Datos estructurados** | Rich Results Test | Validar schema |
| **Email** | Plataforma de email marketing (con lead magnet) | El activo que posees |
| **Monetización (crecer)** | AdSense → Raptive / Mediavine (MCM) → GAM | Migración por umbrales (Cap. 8) |
| **Imágenes** | Compresor + WebP/AVIF | LCP y peso de página |

---

## E. KPIs y sus objetivos de referencia

| KPI | Qué es | Objetivo de referencia |
|-----|--------|------------------------|
| **RPM de página** | Ingresos por 1.000 páginas vistas | Depende del nicho; sube trimestre a trimestre |
| **Páginas por sesión** | Páginas que ve un visitante por visita | > 1,8-2,0 (enlazado interno) |
| **Viewability** | % de anuncios realmente vistos | > 70% (ideal 80%+) |
| **LCP / INP / CLS** | Core Web Vitals | <2,5s / <200ms / <0,1 (campo, móvil) |
| **% tráfico orgánico** | Peso del SEO en tus visitas | 70-95% |
| **CTR en SERP** | Clics/impresiones en Google | Mejorar con títulos/metas |
| **Keywords en top 3 / top 10** | Posiciones ganadoras | Crecimiento mensual |
| **% ingresos no-AdSense** | Diversificación | Subir hacia 40-60% con el tiempo |
| **Coste por artículo vs. ingreso** | Economía del contenido | Ingreso vitalicio > coste |

---

## F. Glosario esencial

| Término | Definición |
|---------|------------|
| **AdSense** | Programa de Google para monetizar webs con anuncios (para publishers). |
| **AdX (Ad Exchange)** | Mercado premium de Google, parte de Ad Manager; CPMs más altos, normalmente vía partner. |
| **CPC** | Coste Por Clic: lo que paga el anunciante por un clic. |
| **CPM** | Coste Por Mil impresiones. |
| **CTR** | Click-Through Rate: % de anuncios que reciben clic. |
| **RPM** | Revenue Per Mille: lo que ganas por cada 1.000 páginas (o sesiones). Tu métrica reina. |
| **Viewability** | % de anuncios mostrados de forma visible (≥50% del área ≥1 s). Lo que ahora se paga. |
| **Core Web Vitals** | LCP, INP, CLS: métricas de experiencia de usuario de Google. |
| **LCP / INP / CLS** | Carga del elemento principal / respuesta a interacción / estabilidad visual. |
| **E-E-A-T** | Experience, Expertise, Authoritativeness, Trust: marco de calidad de Google. |
| **YMYL** | "Your Money or Your Life": temas sensibles (finanzas, salud…) con listón de calidad alto. |
| **SERP** | Página de resultados de búsqueda. |
| **KD** | Keyword Difficulty: dificultad de rankear una keyword. |
| **Cola larga (long-tail)** | Keywords específicas, menor volumen, menor competencia, mayor intención. |
| **Pillar / Cluster** | Guía madre + artículos de apoyo enlazados; estrategia de autoridad temática. |
| **MCM** | Multiple Customer Management: gestión de tu inventario vía partner (Raptive, Mediavine…). |
| **Header bidding** | Subasta simultánea entre varias redes antes del ad server; sube el precio. |
| **GAM** | Google Ad Manager: ad server profesional. |
| **CMP** | Consent Management Platform: gestión del consentimiento de cookies (RGPD/TCF). |
| **Ad refresh** | Recargar un anuncio para generar nuevas impresiones (conforme a políticas). |
| **Tráfico inválido** | Clics/impresiones no legítimos; causa común de suspensión. |
| **Tier 1** | Países que mejor pagan (EE. UU., UK, Canadá, Australia, Alemania…). |

---

## G. Los 12 errores que hunden proyectos (resumen de todo el libro)

1. Elegir un nicho con poco valor publicitario (RPM bajo) → techo de ingresos bajísimo.
2. Ignorar el país de la audiencia → hasta 10× menos ingresos por el mismo tráfico.
3. Solicitar AdSense sin páginas legales o con thin content → rechazo.
4. Hacer clic en tus propios anuncios o comprar tráfico → suspensión permanente.
5. Web lenta / mala en móvil → pierdes tráfico (SEO) e impresiones (ingresos).
6. Saturar de anuncios → baja el CPM, las páginas/sesión y los CWV; riesgo de política.
7. Perseguir CTR en vez de viewability (información obsoleta pre-2024).
8. Publicar AI-spam sin revisión → low value, sin E-E-A-T, sin rankings.
9. Dispersarte en muchos temas → sin autoridad temática, no rankeas en ninguno.
10. Depender solo de AdSense → frágil; ignoras la afiliación (que suele pagar más).
11. Quedarse en AdSense con 100k+ visitas de calidad → dejas la mitad del dinero (MCM).
12. Rendirse a los 3-6 meses → justo antes de que el SEO empiece a componer.

---

## H. Idea de arquitectura: automatizar el reporting (para este repo)

Como el repositorio se llama `agente-google-adsese`, aquí tienes una arquitectura de partida
si quieres construir un **agente de reporting y alertas** que convierta la teoría de este
libro en un panel automatizado:

```
┌────────────────────────────────────────────────────────────┐
│                     AGENTE ADSENSE                          │
├────────────────────────────────────────────────────────────┤
│ FUENTES DE DATOS (APIs oficiales de Google)                 │
│  • AdSense Management API   → RPM, ingresos, viewability     │
│  • Google Analytics Data API (GA4) → sesiones, páginas/ses.  │
│  • Search Console API        → keywords, posiciones, CTR      │
│  • PageSpeed Insights API    → Core Web Vitals de campo       │
├────────────────────────────────────────────────────────────┤
│ LÓGICA (los KPIs y reglas de este libro)                    │
│  • Cuadro de mando mensual (Apéndice E)                      │
│  • Alertas: caída de RPM, caída de tráfico, CWV en rojo      │
│  • Oportunidades: keywords "striking distance" (pos. 8-20)   │
│  • RPM por país/dispositivo → sugerencias de enfoque         │
├────────────────────────────────────────────────────────────┤
│ SALIDA                                                      │
│  • Informe periódico (email/dashboard)                      │
│  • Recomendaciones accionables priorizadas por impacto       │
└────────────────────────────────────────────────────────────┘
```

**Funciones de alto valor para el agente (por prioridad):**
1. **Alerta de caída de ingresos/RPM** (algo se rompió: revisar).
2. **Detector de "striking distance"** (keywords en pos. 8-20 → empujar; máximo ROI SEO).
3. **Monitor de Core Web Vitals** (avisar cuando una plantilla/cambio rompe los CWV).
4. **Informe de RPM por país/dispositivo** (dónde enfocar contenido y layout).
5. **Recordatorio de actualización de contenido** (posts que pierden posiciones).

> Si quieres, este manual puede ser la **base de conocimiento** del agente (system prompt +
> lógica de recomendaciones), y el código puede consumir las APIs de arriba para pasar de
> "consejos" a "acciones automáticas". Dilo y montamos la estructura del proyecto.

---

## Cierre

Tienes en tus manos un sistema completo: **nicho rentable + contenido útil con E-E-A-T + SEO
+ tráfico de países con alto poder adquisitivo + optimización del RPM + salto a AdX/MCM +
diversificación**, todo sobre una base técnica sólida y sin arriesgar la cuenta.

No es un modelo de enriquecimiento rápido: es **construcción de un activo digital** que, con
consistencia durante 12-24 meses, puede convertirse en un negocio muy rentable y **vendible**.

La teoría ya la tienes. Ahora toca lo único que de verdad importa: **ejecutar con constancia.**

*Volver al [índice](../README.md).*
