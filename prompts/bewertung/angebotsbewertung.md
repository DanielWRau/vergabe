# Angebotsbewertung mit KI
## Systematische und nachvollziehbare Bewertung von Angeboten

### 🎯 Zweck
Strukturierte Bewertung eingegangener Angebote mit KI-Unterstützung für faire und transparente Vergabeentscheidungen.

### 🤖 KI-Prompt: Bewertungsmatrix erstellen

```
Erstelle eine strukturierte Bewertungsmatrix für die Angebotsbewertung.

**Ausschreibungskontext:**
- **Leistungsgegenstand:** [z.B. IT-System, Reinigung, Beratung]
- **Vergabeart:** [Öffentlich/Beschränkt/Verhandlung]
- **Auftragswert:** [Betrag]
- **Bewertungsmethode:** [Niedrigster Preis / Wirtschaftlichste Lösung]

**Anforderungen aus der Leistungsbeschreibung:**
[Hier die wichtigsten Anforderungen aus der Ausschreibung einfügen]

**Erstelle eine vollständige Bewertungsmatrix mit:**

## 1. Bewertungskriterien
### Preis (Gewichtung: ___%)
- Angebotspreis (netto)
- Lebenszykluskosten
- Optionale Leistungen

### Qualität (Gewichtung: ___%)
- Technische Leistungsfähigkeit
- Funktionalität und Features
- Qualitätsstandards

### Termine (Gewichtung: ___%)
- Lieferzeit/Projektdauer
- Meilenstein-Einhaltung
- Verfügbarkeit

### Service (Gewichtung: ___%)
- Support und Wartung
- Reaktionszeiten
- Dokumentation und Schulung

### Erfahrung (Gewichtung: ___%)
- Referenzprojekte
- Qualifikation des Teams
- Unternehmensstabilität

## 2. Bewertungsskala
Für jedes Kriterium:
- **5 Punkte:** Hervorragend (übertrifft Anforderungen deutlich)
- **4 Punkte:** Sehr gut (übertrifft Anforderungen)
- **3 Punkte:** Gut (erfüllt Anforderungen vollständig)
- **2 Punkte:** Ausreichend (erfüllt Mindestanforderungen)
- **1 Punkt:** Mangelhaft (erfüllt Anforderungen nicht)
- **0 Punkte:** Ungenügend (keine Angaben/völlig ungeeignet)

## 3. Bewertungsschema
**Gesamtbewertung = Σ (Kriterium × Gewichtung × Punkte)**

## 4. Ausschlusskriterien
- Formelle Mängel (fehlende Unterlagen)
- Fristversäumnis
- Nichteinhaltung von Mindestanforderungen
- Fehlende Nachweise (Referenzen, Zertifikate)

**Zusätzlich benötigt:**
- Detaillierte Bewertungsbögen für jeden Bieter
- Dokumentationsvorlage für Bewertungsentscheidungen
- Prüfschema für Plausibilität und Nachvollziehbarkeit
```

### 🔍 Spezialisierte Bewertungskriterien

**IT-Beschaffung:**
```
Ergänze spezifische IT-Kriterien:

### IT-Sicherheit (Gewichtung: ___%)
- Sicherheitskonzept und Zertifizierungen
- Datenschutz-Compliance (DSGVO)
- Backup und Disaster Recovery

### Integration (Gewichtung: ___%)
- Kompatibilität zu bestehenden Systemen
- API-Qualität und Dokumentation
- Migrationsfähigkeit

### Innovation (Gewichtung: ___%)
- Zukunftsfähigkeit der Lösung
- Update- und Upgrade-Pfad
- Technologische Aktualität
```

**Dienstleistungen:**
```
Ergänze spezifische Service-Kriterien:

### Personal (Gewichtung: ___%)
- Qualifikation und Zertifizierungen
- Verfügbarkeit und Vertretungsregelung
- Kontinuität des Personaleinsatzes

### Flexibilität (Gewichtung: ___%)
- Anpassung an veränderte Anforderungen
- Skalierbarkeit der Leistungen
- Reaktionsfähigkeit bei Störungen

### Nachhaltigkeit (Gewichtung: ___%)
- Umweltfreundliche Arbeitsweise
- Soziale Verantwortung
- Lokale Wertschöpfung
```

### 📊 KI-Prompt: Angebote bewerten

```
Bewerte die eingegangenen Angebote anhand der Bewertungsmatrix.

**Angebot [Bieter-Name]:**
[Hier die relevanten Angaben aus dem Angebot einfügen]

**Bewerte systematisch:**

1. **Formelle Prüfung:**
   - Vollständigkeit der Unterlagen
   - Fristgerechte Einreichung
   - Erfüllung der Teilnahmebedingungen
   - → Ergebnis: Zugelassen / Ausgeschlossen

2. **Eignungsprüfung:**
   - Fachliche Qualifikation
   - Wirtschaftliche Leistungsfähigkeit
   - Referenzen und Erfahrungen
   - → Ergebnis: Geeignet / Nicht geeignet

3. **Inhaltliche Bewertung:**
   Für jedes Bewertungskriterium:
   - Analyse der Angebotsangaben
   - Bewertung nach Punkteskala (0-5)
   - Begründung der Punktevergabe
   - Gewichtung anwenden

4. **Preisbewertung:**
   - Angemessenheit des Preises
   - Vollständigkeit der Preisangaben
   - Lebenszykluskosten berücksichtigen
   - Preis-Leistungs-Verhältnis

5. **Gesamtbewertung:**
   - Punktesumme berechnen
   - Ranking erstellen
   - Besonderheiten dokumentieren
   - Empfehlung für Zuschlag

**Ausgabe:** Strukturiertes Bewertungsprotokoll mit nachvollziehbarer Begründung aller Bewertungen.
```

### ⚖️ Fairness und Transparenz sicherstellen

**Qualitätsprüfung-Prompt:**
```
Prüfe die Angebotsbewertung auf Fairness und Nachvollziehbarkeit:

1. **Gleichbehandlung:**
   - Wurden alle Angebote nach gleichen Kriterien bewertet?
   - Sind die Bewertungsmaßstäbe konsistent angewendet?
   - Gibt es unbegründete Unterschiede in der Bewertung?

2. **Objektivität:**
   - Sind alle Bewertungen sachlich begründet?
   - Wurden persönliche Präferenzen ausgeschlossen?
   - Basieren Bewertungen auf nachprüfbaren Kriterien?

3. **Transparenz:**
   - Sind alle Bewertungsschritte dokumentiert?
   - Können Bewertungsentscheidungen nachvollzogen werden?
   - Sind die angewendeten Kriterien eindeutig?

4. **Rechtssicherheit:**
   - Entspricht die Bewertung den ausgeschriebenen Kriterien?
   - Wurden alle vergaberechtlichen Vorgaben beachtet?
   - Ist die Bewertung gerichtsfest dokumentiert?

Identifiziere potenzielle Schwachstellen und schlage Verbesserungen vor.
```

### 📋 Checkliste: Abgeschlossene Bewertung

- [ ] Alle Angebote formell geprüft
- [ ] Eignungsprüfung durchgeführt
- [ ] Bewertungsmatrix vollständig angewendet
- [ ] Alle Bewertungen begründet
- [ ] Preise plausibilisiert
- [ ] Gesamtranking erstellt
- [ ] Dokumentation vollständig
- [ ] Vier-Augen-Prinzip angewendet
- [ ] Rechtsprüfung durchgeführt
- [ ] Zuschlagsempfehlung formuliert

### 🔄 Nach der Bewertung

**Dokumentations-Prompt:**
```
Erstelle eine vollständige Bewertungsdokumentation:

1. **Bewertungsprotokoll** mit allen Einzelbewertungen
2. **Rangfolge** der Angebote mit Punktzahlen
3. **Begründung** der Zuschlagsentscheidung
4. **Ausschlussgründe** für nicht berücksichtigte Angebote
5. **Besonderheiten** und Auffälligkeiten
6. **Empfehlung** für das weitere Vorgehen

Format: Gerichtsfeste Dokumentation für die Vergabeakte.
```

---

*Hinweis: Bewertung durch mindestens zwei unabhängige Personen durchführen lassen.*