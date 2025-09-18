# Umsetzungsplan: [VERGABE-PROJEKT]

**Branch**: `[###-projekt-name]` | **Datum**: [DATUM] | **Spezifikation**: [link]
**Eingabe**: Vergabe-Spezifikation aus `/specs/[###-projekt-name]/spec.md`

## Ausführungsablauf (/plan Befehl-Umfang)
```
1. Vergabe-Spezifikation aus Eingabe-Pfad laden
   → Falls nicht gefunden: FEHLER "Keine Vergabe-Spezifikation unter {pfad}"
2. Vergabe-Kontext ausfüllen (nach KLÄRUNGSBEDARF suchen)
   → Vergabe-Typ aus Kontext erkennen (Lieferung=Produkt+Logistik, Dienstleistung=Service+SLA)
   → Struktur-Entscheidung basierend auf Vergabe-Typ setzen
3. Rechtsprüfung-Abschnitt basierend auf UVgO/VgV-Vorgaben ausfüllen
4. Rechtsprüfung-Abschnitt evaluieren
   → Falls Verstöße vorhanden: In Komplexitäts-Tracking dokumentieren
   → Falls keine Rechtfertigung möglich: FEHLER "Ansatz zuerst vereinfachen"
   → Fortschritts-Tracking aktualisieren: Erste Rechtsprüfung
5. Phase 0 ausführen → research.md
   → Falls KLÄRUNGSBEDARF verbleibt: FEHLER "Unklarheiten beheben"
6. Phase 1 ausführen → Verträge, Leistungsverzeichnis.md, Schnellstart.md
7. Rechtsprüfung-Abschnitt neu evaluieren
   → Falls neue Verstöße: Design überarbeiten, zurück zu Phase 1
   → Fortschritts-Tracking aktualisieren: Post-Design Rechtsprüfung
8. Phase 2 planen → Aufgaben-Generierungs-Ansatz beschreiben (NICHT tasks.md erstellen)
9. STOPP - Bereit für /tasks Befehl
```

**WICHTIG**: Der /plan Befehl STOPPT bei Schritt 7. Phase 2-4 werden durch andere Befehle ausgeführt:
- Phase 2: /tasks Befehl erstellt tasks.md
- Phase 3-4: Umsetzungs-Ausführung (manuell oder über Tools)

## Zusammenfassung
[Aus Vergabe-Spezifikation extrahieren: Hauptbedarf + Vergabe-Ansatz aus Recherche]

## Vergabe-Kontext
**Vergabe-Art**: [z.B. Öffentliche Ausschreibung, Beschränkte Ausschreibung, Verhandlungsverfahren oder KLÄRUNGSBEDARF]  
**Schwellenwert**: [z.B. Unterschwellig, Oberschwellig oder KLÄRUNGSBEDARF]  
**Budget-Rahmen**: [z.B. bis 50.000€, 50-100.000€, über 100.000€ oder KLÄRUNGSBEDARF]  
**Zeitrahmen**: [z.B. 3 Monate, 6 Monate, 12 Monate oder KLÄRUNGSBEDARF]  
**Bieter-Zielgruppe**: [z.B. Lokale KMU, Bundesweite Anbieter, EU-weit oder KLÄRUNGSBEDARF]
**Vergabe-Typ**: [Lieferung/Dienstleistung/Bauleistung - bestimmt Dokument-Struktur]  
**Bewertungs-Verfahren**: [z.B. Niedrigster Preis, Wirtschaftlichste Lösung oder KLÄRUNGSBEDARF]  
**Rechtliche Besonderheiten**: [z.B. Datenschutz, Compliance, Nachhaltigkeit oder N/A]  
**Bieter-Anforderungen**: [z.B. Referenzen, Zertifizierungen, Kapazitäten oder KLÄRUNGSBEDARF]

## Rechtsprüfung
*GATE: Muss vor Phase 0 Recherche bestehen. Neu prüfen nach Phase 1 Design.*

**UVgO/VgV-Konformität**:
- [ ] Vergabe-Art rechtlich zulässig für Budget und Leistung
- [ ] Mindest-Verfahrensdauer eingehalten (UVgO: mind. 10 Tage)
- [ ] Gleichbehandlungsgrundsatz beachtet
- [ ] Transparenz-Anforderungen erfüllt

**EU-Recht (falls oberschwellig)**:
- [ ] EU-weite Bekanntmachung erforderlich
- [ ] Mindestfristen nach EU-Richtlinien
- [ ] Vergabe-Kriterien objektiv und nachvollziehbar

## Projekt-Struktur

### Dokumentation (dieses Projekt)
```
specs/[###-projekt]/
├── plan.md              # Diese Datei (/plan Befehl Ausgabe)
├── research.md          # Phase 0 Ausgabe (/plan Befehl)
├── leistungsverzeichnis.md   # Phase 1 Ausgabe (/plan Befehl)
├── schnellstart.md      # Phase 1 Ausgabe (/plan Befehl)
├── verträge/           # Phase 1 Ausgabe (/plan Befehl)
└── tasks.md            # Phase 2 Ausgabe (/tasks Befehl - NICHT durch /plan erstellt)
```

### Vergabe-Dokumente (Repository-Stamm)
```
# Option 1: Standard-Vergabe (DEFAULT)
vergabe/
├── ausschreibung/
├── bewertung/
├── verträge/
└── dokumentation/

unterlagen/
├── rechtsprüfung/
├── marktanalyse/
└── protokolle/

# Option 2: Komplexe Beschaffung (wenn "mehrteilig" + "verschiedene Lose" erkannt)
lose/
├── los1-lieferung/
│   ├── ausschreibung/
│   ├── bewertung/
│   └── verträge/
└── los2-dienstleistung/
    ├── ausschreibung/
    ├── bewertung/
    └── verträge/

zentral/
├── rechtsprüfung/
├── gesamtbewertung/
└── projektmanagement/

# Option 3: Rahmenvereinbarung (wenn "langfristig" oder "Abrufverträge" erkannt)
rahmen/
├── ausschreibung/
└── bedingungen/

abrufe/
└── [einzelabruf-spezifisch]
```

**Struktur-Entscheidung**: [DEFAULT auf Option 1 außer Vergabe-Kontext deutet auf komplexe/Rahmen-Beschaffung hin]

## Phase 0: Übersicht & Recherche
1. **Unbekannte aus Vergabe-Kontext extrahieren**:
   - Für jeden KLÄRUNGSBEDARF → Recherche-Aufgabe
   - Für jede rechtliche Vorgabe → Best-Practice-Aufgabe
   - Für jede Markt-Integration → Muster-Aufgabe

2. **Recherche-Agenten generieren und aussenden**:
   ```
   Für jede Unbekannte im Vergabe-Kontext:
     Aufgabe: "Recherchiere {Unbekannte} für {Vergabe-Kontext}"
   Für jede Rechts-Wahl:
     Aufgabe: "Finde Best Practices für {Rechtsbereich} in {Domäne}"
   ```

3. **Erkenntnisse konsolidieren** in `research.md` mit Format:
   - Entscheidung: [was gewählt wurde]
   - Begründung: [warum gewählt]
   - Betrachtete Alternativen: [was sonst evaluiert]

**Ausgabe**: research.md mit allen KLÄRUNGSBEDARF gelöst

## Phase 1: Design & Verträge
*Voraussetzungen: research.md vollständig*

1. **Leistungselemente aus Vergabe-Spezifikation extrahieren** → `leistungsverzeichnis.md`:
   - Leistungsname, Spezifikation, Bewertungskriterien
   - Qualitäts-Regeln aus Anforderungen
   - Liefer-/Service-Level-Übergänge falls zutreffend

2. **Vertragsmuster aus funktionalen Anforderungen generieren**:
   - Für jede Nutzer-Aktion → Vertragsklausel
   - Standard-Vergabe-Muster verwenden (VOB/VOL/VOF)
   - Ausgabe OpenAPI/Vertrags-Schema nach `/verträge/`

3. **Vertrags-Tests aus Verträgen generieren**:
   - Eine Test-Datei pro Vertragsklausel
   - Request/Response-Schemas bestätigen
   - Tests müssen fehlschlagen (noch keine Umsetzung)

4. **Test-Szenarien aus Benutzer-Geschichten extrahieren**:
   - Jede Geschichte → Integrations-Test-Szenario
   - Schnellstart-Test = Geschichts-Validierungs-Schritte

**Ausgabe**: leistungsverzeichnis.md, /verträge/*, fehlschlagende Tests, schnellstart.md

## Phase 2: Aufgaben-Planung Ansatz
*Dieser Abschnitt beschreibt was der /tasks Befehl tun wird - NICHT während /plan ausführen*

**Aufgaben-Generierungs-Strategie**:
- Lade `templates/vergabe-tasks-template.md` als Basis
- Generiere Aufgaben aus Phase 1 Design-Docs (Verträge, Leistungsverzeichnis, Schnellstart)
- Jeder Vertrag → Vertrags-Test-Aufgabe [P]
- Jedes Leistungselement → Spezifikations-Erstellungs-Aufgabe [P] 
- Jede Benutzer-Geschichte → Integrations-Test-Aufgabe
- Umsetzungs-Aufgaben um Tests zum Bestehen zu bringen

**Reihenfolge-Strategie**:
- TDD-Reihenfolge: Tests vor Umsetzung 
- Abhängigkeits-Reihenfolge: Rechtsprüfung vor Ausschreibung vor Bewertung
- [P] markieren für parallele Ausführung (unabhängige Dateien)

**Geschätzte Ausgabe**: 15-25 nummerierte, geordnete Aufgaben in tasks.md

**WICHTIG**: Diese Phase wird durch den /tasks Befehl ausgeführt, NICHT durch /plan

## Phase 3+: Zukünftige Umsetzung
*Diese Phasen sind außerhalb des Umfangs des /plan Befehls*

**Phase 3**: Aufgaben-Ausführung (/tasks Befehl erstellt tasks.md)  
**Phase 4**: Umsetzung (tasks.md ausführen entsprechend rechtlichen Prinzipien)  
**Phase 5**: Validierung (Tests laufen, schnellstart.md ausführen, Rechtsprüfungs-Validierung)

## Komplexitäts-Tracking
*NUR ausfüllen falls Rechtsprüfung Verstöße hat die gerechtfertigt werden müssen*

| Verstoß | Warum Nötig | Einfachere Alternative Abgelehnt Weil |
|---------|------------|-------------------------------------|
| [z.B. Verhandlungsverfahren] | [aktueller Bedarf] | [warum öffentliche Ausschreibung unzureichend] |
| [z.B. Lose-Aufteilung] | [spezifisches Problem] | [warum Gesamt-Vergabe unzureichend] |

## Fortschritts-Tracking
*Diese Checkliste wird während Ausführungsablauf aktualisiert*

**Phasen-Status**:
- [ ] Phase 0: Recherche vollständig (/plan Befehl)
- [ ] Phase 1: Design vollständig (/plan Befehl)
- [ ] Phase 2: Aufgaben-Planung vollständig (/plan Befehl - nur Ansatz beschreiben)
- [ ] Phase 3: Aufgaben generiert (/tasks Befehl)
- [ ] Phase 4: Umsetzung vollständig
- [ ] Phase 5: Validierung bestanden

**Gate-Status**:
- [ ] Erste Rechtsprüfung: BESTANDEN
- [ ] Post-Design Rechtsprüfung: BESTANDEN
- [ ] Alle KLÄRUNGSBEDARF behoben
- [ ] Komplexitäts-Abweichungen dokumentiert

---
*Basierend auf UVgO v2.1.1 - Siehe `/memory/uvgo.md`*