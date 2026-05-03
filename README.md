# VodaControl Landing

Landing publica de [VodaControl](https://vodacontrol.com) — plataforma de gestion para distribuidores Vodafone Empresas.

## Stack

- HTML estatico + CSS inline (sin build, sin dependencias)
- Fuentes Google Fonts (Inter + JetBrains Mono)
- Hospedado en GitHub Pages

## Deploy

Push a `main` y GitHub Pages publica automaticamente. El CNAME apunta a `vodacontrol.com`.

DNS:
- `vodacontrol.com` → GitHub Pages (A records de github.io)
- `vodacontrol.matizal.com` → portal de la app (VPS 91.134.43.229) — separado de esta landing.

## CTAs

- **Acceder** → `https://vodacontrol.matizal.com/login` (portal de la app)
- **Solicitar acceso** → `mailto:hola@fenixia.tech` con asunto y body precompletado

## Estructura

```
vodacontrol-landing/
├── index.html      # Pagina unica
├── favicon.svg     # Isotipo M-VodaControl (rojo Vodafone + barra negra)
├── CNAME           # vodacontrol.com (GitHub Pages)
└── README.md
```

## Producto detras

VodaControl es la rebrand de `app-vdf` (Laravel 13 + Inertia + React + Postgres). Esta landing es solo la cara publica; el codigo de la app vive en [`PedroFenixia/app-vdf`](https://github.com/PedroFenixia/app-vdf).
