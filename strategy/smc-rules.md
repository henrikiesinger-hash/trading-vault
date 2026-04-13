# SMC Trading Rules

## Entry Conditions

Alle Bedingungen müssen erfüllt sein, bevor ein Trade eröffnet wird:

| # | Bedingung | Details |
|---|-----------|---------|
| 1 | **Session** | London–NY Session: 07:00–21:00 UTC |
| 2 | **H1 Trend** | EMA 50/200 bestätigt Trendrichtung |
| 3 | **H1 nicht choppy** | Kein Seitwärtsmarkt auf H1 |
| 4 | **M15 Order Block** | Preis befindet sich in der OB-Zone auf M15 |
| 5 | **Score ≥ 6.0/10** | Mindest-Score aus dem Scoring-System |

## Scoring-System

| Kriterium | Punkte |
|-----------|--------|
| Trend Alignment | +2.0 |
| Structure Match | +1.0 bis +2.0 |
| Break of Structure (BOS) | +2.0 |
| At Order Block | +1.5 |
| Liquidity Sweep | +0.5 |
| Premium/Discount Zone | +0.5 |
| RSI Confirmation | +0.5 |
| **Maximum** | **9.0** |

> Ein Trade wird nur ausgeführt, wenn der Gesamt-Score **≥ 6.0** beträgt.

## Risk Management

| Parameter | Wert |
|-----------|------|
| Stop-Loss | 8–12 Punkte (ATR-basiert) |
| Minimum Risk-Reward | 2:1 |
| Cooldown nach WIN | 24 Candles |
| Cooldown nach LOSS | 48 Candles |
