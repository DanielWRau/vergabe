# Öffentliche Ausschreibung: Vorbereitung
## Systematische Vorbereitung einer öffentlichen Ausschreibung

### 🎯 Anwendungsbereich
- Auftragswert: über 25.000 EUR (UVgO) bzw. über EU-Schwellenwerten (VgV)
- Standard-Vergabeverfahren für die meisten Beschaffungen
- Maximale Transparenz und Wettbewerb

---

## 📋 Phase 1: Projektvorbereitung (Woche 1-2)

### Schritt 1.1: Vergabe-Spezifikation prüfen

**Checkliste:**
- [ ] [Vergabe-Spezifikation](../../templates/vergabe-spezifikation.md) liegt vollständig vor
- [ ] Alle KLÄRUNGSBEDARFE sind beseitigt
- [ ] Budget und Zeitrahmen sind realistisch
- [ ] Stakeholder haben freigegeben

**KI-Prompt: Spezifikation für öffentliche Ausschreibung prüfen**
```
Prüfe diese Vergabe-Spezifikation für eine öffentliche Ausschreibung:

[Spezifikation hier einfügen]

Bewerte speziell:
1. **Wettbewerbsfähigkeit**: Können mehrere Anbieter bieten?
2. **Standardisierung**: Ist die Leistung ausreichend standardisiert?
3. **Beschreibbarkeit**: Lässt sich alles vorab eindeutig beschreiben?
4. **Vergleichbarkeit**: Sind eingeh. Angebote objektiv vergleichbar?
5. **Marktreife**: Gibt es etablierte Marktlösungen?

Falls NEIN bei mehreren Punkten: Empfehle beschränkte Ausschreibung oder Verhandlungsverfahren.
```

### Schritt 1.2: Rechtliche Grundlagen klären

**Vergabeart bestimmen:**
- [ ] Auftragswert ermittelt (netto, Gesamtlaufzeit)
- [ ] Schwellenwert-Prüfung: Unterschwellig (UVgO) oder Oberschwellig (VgV)?
- [ ] EU-weite Bekanntmachung erforderlich?

**KI-Prompt: Verfahrensart und Fristen bestimmen**
```
Bestimme das korrekte Vergabeverfahren:

**Auftragsdaten:**
- Auftraggeber: [z.B. Stadt, Behörde, Stadtwerke]
- Leistungsart: [Lieferung/Dienstleistung/Bauleistung]
- Geschätzter Auftragswert: [Betrag] EUR netto
- Vertragslaufzeit: [Jahre] Jahre
- Optionen/Verlängerungen: [ja/nein, Details]

**Analysiere:**
1. Welche Vergabeordnung gilt? (UVgO/VgV/SektVO)
2. Ist öffentliche Ausschreibung zulässig und sinnvoll?
3. Welche Mindestfristen gelten?
4. Ist EU-weite Bekanntmachung erforderlich?
5. Welche besonderen Vorschriften sind zu beachten?

**Ausgabe:** Klare Verfahrensempfehlung mit Begründung und Fristenplan.
```

### Schritt 1.3: Marktanalyse durchführen

**KI-Prompt: Marktanalyse für öffentliche Ausschreibung**
```
Führe eine Marktanalyse für diese öffentliche Ausschreibung durch:

**Leistungsgegenstand:** [aus Spezifikation]
**Geschätzter Auftragswert:** [Betrag]
**Region:** [geografische Eingrenzung]

**Analysiere:**
1. **Anbieterstruktur:**
   - Wie viele potenzielle Bieter gibt es?
   - Regionale vs. überregionale Anbieter
   - KMU vs. Großunternehmen

2. **Marktbedingungen:**
   - Übliche Preisstrukturen
   - Technische Standards
   - Verfügbarkeiten und Lieferzeiten

3. **Wettbewerbsintensität:**
   - Ist ausreichend Wettbewerb zu erwarten?
   - Gibt es Marktführer oder Monopolstrukturen?
   - Markteintrittsbarrieren für neue Anbieter?

4. **Risiken:**
   - Marktkonzentration
   - Technologiewandel
   - Kapazitätsengpässe

**Empfehlung:** Geeignetheit für öffentliche Ausschreibung mit Begründung.
```

---

## 📄 Phase 2: Ausschreibungsunterlagen erstellen (Woche 3-4)

### Schritt 2.1: Leistungsbeschreibung formulieren

**Verwende:** [Prompt für Leistungsbeschreibung](../../prompts/ausschreibung/leistungsbeschreibung.md)

**Besonderheiten öffentliche Ausschreibung:**
- Vollständige Beschreibung aller Anforderungen
- Keine nachträglichen Änderungen möglich
- Objektive, prüfbare Kriterien
- "Oder gleichwertig" bei Markenbezug

### Schritt 2.2: Bewertungskriterien festlegen

**KI-Prompt: Bewertungskriterien für öffentliche Ausschreibung**
```
Erstelle Bewertungskriterien für eine öffentliche Ausschreibung:

**Kontext:** [Leistungsgegenstand und Anforderungen]

**Entscheide zuerst:**
1. **Zuschlagskriterium:**
   - Niedrigster Preis (bei standardisierten Leistungen)
   - Wirtschaftlichste Lösung (bei komplexeren Anforderungen)

2. **Falls "Wirtschaftlichste Lösung":**
   
   **Bewertungskriterien mit Gewichtung:**
   - Preis: ___% (meist 40-60%)
   - Qualität: ___% 
   - Service: ___%
   - Nachhaltigkeit: ___%
   - [weitere Kriterien]: ___%
   
   **Für jedes Kriterium definiere:**
   - Eindeutige Bewertungsmaßstäbe
   - Messbare Indikatoren
   - Punkteskala (z.B. 0-5 Punkte)
   - Gewichtungsfaktoren

3. **Eignungsanforderungen:**
   - Fachliche Eignung
   - Wirtschaftliche Leistungsfähigkeit
   - Technische Leistungsfähigkeit
   - Zuverlässigkeit

**Wichtig:** Alle Kriterien müssen vorab in der Bekanntmachung angekündigt werden!
```

### Schritt 2.3: Vergabeunterlagen zusammenstellen

**Standard-Dokumente:**
- [ ] Bekanntmachung
- [ ] Vergabeunterlagen/Ausschreibungstext
- [ ] Leistungsbeschreibung
- [ ] Vertragsbedingungen (AGB, bes. Vertragsbedingungen)
- [ ] Bietererklärungen und Nachweise
- [ ] Formblätter für Angebote

---

## 📅 Phase 3: Zeitplanung und Fristen (Woche 4)

### KI-Prompt: Zeitplan für öffentliche Ausschreibung

```
Erstelle einen detaillierten Zeitplan für diese öffentliche Ausschreibung:

**Rahmendaten:**
- Vergabeordnung: [UVgO/VgV]
- Geschätzter Auftragswert: [Betrag]
- Gewünschter Projektstart: [Datum]
- Besonderheiten: [z.B. Ortsbesichtigung, komplexe Leistung]

**Berechne Mindestfristen:**

1. **Veröffentlichung bis Angebotsabgabe:**
   - UVgO: mindestens 10 Kalendertage
   - VgV: mindestens 30 Kalendertage (bei EU-weiter Bekanntmachung)
   - Verlängerung bei: Ortsbesichtigung (+5 Tage), umfangreichen Unterlagen

2. **Prüfungs- und Bewertungszeit:**
   - Formelle Prüfung: 2-3 Werktage
   - Fachliche Bewertung: 5-10 Werktage (je nach Komplexität)
   - Interne Abstimmung: 2-3 Werktage

3. **Zuschlag und Vertragsschluss:**
   - Zuschlagsentscheidung: 2 Werktage
   - Wartepflicht (Standstill): 10 Kalendertage (nur VgV)
   - Vertragsunterzeichnung: 3-5 Werktage

**Erstelle Rückwärtsplanung** vom gewünschten Projektstart.

**Pufferzeiten einplanen** für:
- Rückfragen von Bietern
- Nachforderung von Unterlagen
- Interne Freigabeprozesse
- Rechtsprüfung
```

---

## ✅ Abschluss Phase 1-3: Freigabe zur Veröffentlichung

### Finale Prüfung vor Veröffentlichung

**Checkliste:**
- [ ] Leistungsbeschreibung vollständig und eindeutig
- [ ] Bewertungskriterien objektiv und verhältnismäßig
- [ ] Fristen korrekt berechnet
- [ ] Alle erforderlichen Unterlagen erstellt
- [ ] Rechtliche Prüfung durchgeführt
- [ ] Interne Freigaben eingeholt
- [ ] Vergabeplattform vorbereitet

### 🚀 Nächste Schritte

1. **Veröffentlichung:** → [02-durchfuehrung.md](02-durchfuehrung.md)
2. **Bieterkommunikation:** → [03-bieter-betreuung.md](03-bieter-betreuung.md)
3. **Angebotsbewertung:** → [04-bewertung.md](04-bewertung.md)

---

*Geschätzte Bearbeitungszeit: 3-4 Wochen*  
*Erforderliche Ressourcen: Vergabeexperte, Fachexperte, Jurist*