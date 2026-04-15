# FTMO Compliance Rules — Bot-Relevant

> Quelle: FTMO Account Agreement (Order #23264598, Stand 23. Maerz 2026)
> Produkt: FTMO Challenge 1-Step, EUR 499
> Erstellt: 15. April 2026

-----

## Kritische Regeln (Verstoss = Konto-Verlust)

### 1. News-Sperre (Clause 5.15.3)

- Keine Trades 2 Minuten VOR und 2 Minuten NACH signifikanten Makro-News
- Gilt fuer das gehandelte Instrument (XAUUSD)
- News-Liste: siehe FTMO Wirtschaftskalender
- **Bot-Action: News-Filter bauen mit automatischer Trading-Sperre**

### 2. Trading Hours (Clause 5.15.2)

- Keine offenen Positionen ausserhalb der Trading Hours
- Ausnahme: 2-Stunden Roll-over Break erlaubt
- **Bot-Action: Session-Close Check — offene Trades vor Session-Ende schliessen oder warnen**

### 3. Simulated Trading Objectives (Clause 5.15.1 + 5.17)

- Alle Objectives muessen erfuellt werden (Profit Target, Max Loss, Max Daily Loss etc.)
- Verstoss = sofortige Kuendigung OHNE Reward-Anspruch
- **Bot-Action: Drawdown-Monitor mit Warnungen bei Annaeherung an Limits**

### 4. WICHTIG: Swing Account Ausnahme (Clause 5.16)

- Clauses 5.15.2 (Trading Hours) und 5.15.3 (News-Sperre) gelten NICHT fuer Swing Accounts
- **Status klären: Habe ich Swing oder Standard?**

-----

## Risk Management Rules (Clause 5.10)

### 5. Konsistente Positionsgroessen

- Keine deutlich groesseren Positionsgroessen als ueblich (5.10.1)
- Keine deutlich kleinere oder groessere Anzahl Trades als ueblich (5.10.2)
- **Bot-Action: Position Sizing konsistent halten, keine Spikes**

### 6. Kein kumulatives Exposure (5.10.3)

- Keine wiederholten Trades die zu hoeherem Risk per Trade Idea fuehren
- Gilt fuer XAUUSD und korrelierte Symbole
- **Bot-Action: Cooldown-System beibehalten, max 1 offener Trade**

-----

## Inaktivitaet und Drawdown (Clause 12.2.3)

### 7. Mindestens 1 Trade pro 30 Tage

- 30 Kalendertage ohne Trade = FTMO kann kuendigen
- **Bot-Action: Inaktivitaets-Warnung nach 20 Tagen ohne Trade**

### 8. Drawdown-Grenze

- Loss zwischen 8% und 10% des Initial Capital ueber 30+ Tage = Kuendigung moeglich
- **Bot-Action: Drawdown-Tracker mit Warnung bei 7% und Hard-Stop bei 9%**

-----

## Forbidden Trading Practices (Clause 5.9)

- Konkrete Liste ist auf der FTMO Website verlinkt (nicht im Vertrag selbst)
- FTMO bestimmt nach eigenem Ermessen was als Forbidden Practice gilt
- Liste kann jederzeit aktualisiert werden
- **Action: Forbidden Practices Liste von FTMO Website holen und hier dokumentieren**

-----

## Konsequenzen bei Verstoss (Clause 5.11)

FTMO kann bei Verstoss gegen Rules oder Risk Management:

- Max Leverage reduzieren
- Reward-Anspruch streichen (ganz oder teilweise)
- Trades stornieren oder aus der PnL entfernen
- Konto sofort kuendigen
- Alle verbundenen Konten kuendigen
- Trading-Plattform-Nutzung einschraenken

-----

## Bot-Feature Prioritaeten (abgeleitet)

|Prioritaet|Feature                          |FTMO Clause    |
|----------|---------------------------------|---------------|
|KRITISCH  |News-Filter (2 Min Sperre)       |5.15.3         |
|KRITISCH  |Session-Close Check              |5.15.2         |
|HOCH      |Drawdown-Monitor + Warnungen     |5.15.1 / 12.2.3|
|HOCH      |Forbidden Practices Liste pruefen|5.9            |
|MITTEL    |Inaktivitaets-Warnung            |12.2.3a        |
|MITTEL    |Position Sizing Konsistenz-Check |5.10           |
|KLÄREN    |Swing vs Standard Account        |5.16           |
