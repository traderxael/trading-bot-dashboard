# Trading Bot Dashboard

> Axael Contreras · HTML + CSS + JS (sin dependencias)

Panel de control **standalone** para ver la actividad de tu bot de trading vía la API
de Binance. Un solo archivo, cero instalación, cero build.

## Qué hace

- 📈 Muestra datos de mercado en vivo desde la API pública de Binance
- 🔌 Se conecta directo a Binance — **no necesita API key** ni backend
- 📄 Un solo `index.html` — ábrelo y funciona
- 📱 Diseño responsive, se ve bien en escritorio y móvil

## Uso

```bash
# Opción 1: abrir directo en el navegador
open index.html

# Opción 2: servirlo local (recomendado para evitar CORS)
python -m http.server 8000
# luego abre http://localhost:8000
```

## Estructura

```
trading-bot-dashboard/
└── index.html    # todo el panel: HTML + CSS + JS
```

No hay build step ni `package.json` a propósito: es un archivo autocontenido.

## API usada

Endpoints públicos de Binance (sin autenticación):

- `/api/v3/ticker/24hr` — estadísticas de 24 h
- `/api/v3/klines` — velas para los gráficos

> ⚠️ Solo usa endpoints **públicos**: no expongas claves de API de Binance en este HTML.
> Para trading real, todo secret debe vivir en un backend, nunca en el frontend.

## Licencia

MIT — ver [LICENSE](LICENSE).
