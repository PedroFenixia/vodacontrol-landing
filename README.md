# VodaControl Landing

Landing publica de [VodaControl](https://vodacontrol.com) — plataforma de gestion para distribuidores Vodafone Empresas.

## Stack

Pack autocontenido (HTML+JS+fuentes embebidas, ~1.8 MB) generado desde un proyecto Claude. Hospedado en GitHub Pages.

## Deploy

Push a `main` y GitHub Pages publica automaticamente. El CNAME apunta a `vodacontrol.com`.

DNS:

- `vodacontrol.com` → GitHub Pages (A records 185.199.x.153 + AAAA 2606:50c0:8000-8003::153)
- `vodacontrol.matizal.com` → portal de la app (VPS 91.134.43.229) — separado de esta landing.

## Estructura

```text
vodacontrol-landing/
├── index.html          # Landing autocontenida
├── brand/              # Iconos + isotipo
│   ├── isotipo.svg
│   ├── icon_16.png
│   ├── icon_32.png
│   ├── icon_180.png    # apple-touch-icon
│   ├── icon_192.png
│   └── icon_512.png
├── CNAME               # vodacontrol.com (GitHub Pages)
├── .nojekyll           # GitHub Pages no procesa Jekyll
├── README.md           # Este archivo
└── README.deploy.md    # Notas del bundler original (form, A/B variants)
```

## Producto detras

VodaControl es la rebrand de `app-vdf` (Laravel 13 + Inertia + React + Postgres). Esta landing es solo la cara publica; el codigo de la app vive en [`PedroFenixia/app-vdf`](https://github.com/PedroFenixia/app-vdf).

Pendiente: conectar el formulario de contacto (ahora es solo UI). Ver `README.deploy.md` para opciones (Formspree, webhook CRM, backend propio).
