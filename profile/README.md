# Strev

**Software para entrenadores personales freelance.** Gestión clínica, programación inteligente y métricas que sirven — en una sola plataforma.

[Web](https://strev.app) · [Pricing](https://strev.app/pricing) · [Waitlist](https://strev.app/waitlist) · [hola@strev.app](mailto:hola@strev.app)

---

### Por qué existe Strev

Los entrenadores personales freelance gestionan 5–30 clientes con **Excel + WhatsApp + notas en papel**. Strev reemplaza ese stack con una plataforma construida alrededor del flujo real del entrenador.

- **Para EPs freelance, no para gimnasios.** Cada decisión de producto pesa en favor del entrenador individual.
- **Anamnesis primero.** El expediente clínico del cliente es el corazón del producto, no un módulo más.
- **Datos que sirven, no dashboards bonitos.** Si una métrica no cambia una decisión, no la mostramos.

### Core loop

```
Abrir app  →  Ver siguiente ejercicio  →  Registrar set  →  PR badge  →  Siguiente
```

Todo lo demás está construido para no añadir fricción a este flujo. Botones grandes, un tap para confirmar, feedback inmediato.

---

### Para quién

| | **Entrenador personal** | **Atleta independiente** |
|---|---|---|
| **Core** | Crea rutinas, asigna y personaliza por cliente sin duplicar | Registra sesiones en 1–2 taps con timer y PRs |
| **Gestión** | Dashboard con KPIs, adherencia y señales de estancamiento | Métricas de progreso, informe mensual exportable |
| **Pagos** | Cobra suscripciones con Stripe | Plan Athlete Pro con historial completo + IA |
| **Extra** | Anamnesis digital cifrada, página pública, vídeos demo por ejercicio | Análisis de técnica con IA de vídeo |

---

### Planes

**Entrenadores** — descuento anual ≈30% (3–4 meses gratis)

| Plan | Mensual | Anual | Clientes | IA/día | Vídeos | Nutrición | Branded |
|---|---|---|---|---|---|---|---|
| Free *(14d trial Pro)* | €0 | — | 3 | 0 | 0 | — | — |
| **Starter** | €29 | €240 | 8 | 3 | 10 | — | — |
| **Pro** | €59 | €490 | 18 | 8 | 50 | Básica | — |
| **Studio** | €119 | €990 | 35 | 20 | 250 | Avanzada | ✅ |
| **Enterprise** | Hablamos | — | >35 | Custom | ∞ | + IA | + white-label |

**Atletas** — Free (€0, 2 rutinas, 30d historial) · **Athlete Pro** €9/mes — rutinas ilimitadas, IA 5/día, historial completo.

> [!NOTE]
> Pricing v2 vigente desde ADR-0048 (2026-05-18). Lanzamiento de pago: 1 de junio de 2026. Cuentas creadas antes del lanzamiento mantienen Free indefinido.

---

### Repositorios

| Repo | Stack | Estado |
|---|---|---|
| [`strev-web`](https://github.com/StrevFit/strev-web) | React 19 · Vite 7 · Tailwind 4 | Beta cerrada |
| [`strev-api`](https://github.com/StrevFit/strev-api) | Node 22 · Express 5 · MongoDB · Mongoose | Beta cerrada |

> [!WARNING]
> Strev está en **beta cerrada** hasta el 1 de junio de 2026. La API y el modelo de datos pueden cambiar sin previo aviso. Para acceso anticipado: [hola@strev.app](mailto:hola@strev.app).

---

### Stack operativo

- **Backend** — Node 22 + Express 5 + MongoDB Atlas + Mongoose, Zod en boundaries, JWT cookie HttpOnly.
- **Frontend** — React 19 + Vite 7 + Tailwind 4 + Framer Motion, PWA con service worker.
- **Storage** — Cloudflare R2 (vídeos, signed URLs 60s TTL).
- **Cache & colas** — Upstash Redis (rate limiting, async video analysis).
- **Pagos** — Stripe Subscriptions.
- **Email** — Resend (dominio `hola@strev.app` verificado).
- **Observabilidad** — Sentry (errores) + BetterStack (uptime + logs).
- **GDPR** — anamnesis cifrada AES-256 (Art. 9 RGPD), datos en UE (Frankfurt).

---

Hecho en España. © Strev 2026.
