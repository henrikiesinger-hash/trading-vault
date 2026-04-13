# Bot Architecture

## Files

| Datei | Beschreibung |
|-------|-------------|
| `main.py` | Einstiegspunkt, Scheduler, Telegram-Integration |
| `strategy.py` | SMC-Strategie-Logik, Scoring, Entry/Exit |
| `data.py` | Marktdaten-Abruf, OHLCV, Caching |
| `indicators.py` | Technische Indikatoren (EMA, RSI, ATR) |
| `config.py` | Konfiguration, API-Keys, Parameter |
| `CLAUDE.md` | Kontext-Datei für Claude Code |

## Sub-Agents

| Agent | Modell | Aufgabe |
|-------|--------|---------|
| strategy-agent | Opus | Strategie-Entwicklung & Optimierung |
| infra-agent | Sonnet | Infrastruktur, Deployment, DevOps |
| qa-agent | Sonnet | Testing, Code-Review, Qualitätssicherung |

## Deployment

| Parameter | Wert |
|-----------|------|
| Plattform | Railway |
| Web-Framework | Flask (Port 8080) |
| WSGI-Server | gunicorn |
| Scheduler | APScheduler (1-Minuten-Intervall) |
