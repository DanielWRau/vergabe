# Aufgaben: [VERGABE-PROJEKT]

**Eingabe**: Design-Dokumente aus `/specs/[###-projekt-name]/`
**Voraussetzungen**: plan.md (erforderlich), research.md, leistungsverzeichnis.md, verträge/

## Ausführungsablauf (main)
```
1. plan.md aus Projekt-Verzeichnis laden
   → Falls nicht gefunden: FEHLER "Kein Umsetzungsplan gefunden"
   → Extrahieren: Vergabe-Typ, rechtliche Vorgaben, Struktur
2. Optionale Design-Dokumente laden:
   → leistungsverzeichnis.md: Leistungselemente → Spezifikations-Aufgaben extrahieren
   → verträge/: Jede Datei → Vertrags-Test-Aufgabe
   → research.md: Entscheidungen → Setup-Aufgaben extrahieren
3. Aufgaben nach Kategorie generieren:
   → Setup: Projekt-Init, rechtliche Prüfung, Dokumentation
   → Tests: Vertrags-Tests, Integrations-Tests
   → Kern: Ausschreibung, Bewertung, Zuschlag
   → Integration: Bieter-Kommunikation, Vertragsmanagement
   → Finalisierung: Rechtsprüfung, Dokumentation, Archivierung
4. Aufgaben-Regeln anwenden:
   → Verschiedene Dokumente = [P] für parallel markieren
   → Gleiches Dokument = sequenziell (kein [P])
   → Tests vor Umsetzung (TDD)
5. Aufgaben sequenziell nummerieren (A001, A002...)
6. Abhängigkeits-Graph generieren
7. Parallel-Ausführungs-Beispiele erstellen
8. Aufgaben-Vollständigkeit validieren:
   → Alle Verträge haben Tests?
   → Alle Leistungselemente haben Spezifikationen?
   → Alle rechtlichen Vorgaben berücksichtigt?
9. Rückgabe: ERFOLG (Aufgaben bereit für Ausführung)
```

## Format: `[ID] [P?] Beschreibung`
- **[P]**: Kann parallel laufen (verschiedene Dateien, keine Abhängigkeiten)
- Exakte Datei-Pfade in Beschreibungen einschließen

## Pfad-Konventionen
- **Standard-Vergabe**: `vergabe/`, `unterlagen/` im Repository-Stamm
- **Komplexe Beschaffung**: `lose/`, `zentral/`
- **Rahmenvereinbarung**: `rahmen/`, `abrufe/`
- Unten gezeigte Pfade nehmen Standard-Vergabe an - anpassen basierend auf plan.md Struktur

## Phase 3.1: Setup
- [ ] A001 Projekt-Struktur laut Umsetzungsplan erstellen
- [ ] A002 Rechtliche Grundlagen-Prüfung für [Vergabe-Art] initialisieren
- [ ] A003 [P] Dokumentations-Vorlagen und Formatierung konfigurieren

## Phase 3.2: Tests Zuerst (TDD) ⚠️ MUSS VOR 3.3 ABGESCHLOSSEN WERDEN
**KRITISCH: Diese Tests MÜSSEN geschrieben werden und MÜSSEN fehlschlagen vor JEDER Umsetzung**
- [ ] A004 [P] Vertrags-Test für Rahmenvertrag in unterlagen/rechtsprüfung/test_rahmenvertrag.md
- [ ] A005 [P] Vertrags-Test für Leistungsbeschreibung in unterlagen/rechtsprüfung/test_leistung.md
- [ ] A006 [P] Integrations-Test Ausschreibungsverfahren in unterlagen/tests/test_ausschreibung.md
- [ ] A007 [P] Integrations-Test Bewertungsverfahren in unterlagen/tests/test_bewertung.md

## Phase 3.3: Kern-Umsetzung (NUR nach fehlschlagenden Tests)
- [ ] A008 [P] Leistungsverzeichnis in vergabe/ausschreibung/leistungsverzeichnis.md
- [ ] A009 [P] Ausschreibungstext in vergabe/ausschreibung/ausschreibung.md
- [ ] A010 [P] Bewertungsmatrix in vergabe/bewertung/bewertungsmatrix.xlsx
- [ ] A011 Bieter-Information in vergabe/ausschreibung/bieterinformation.md
- [ ] A012 Vergabe-Bekanntmachung in vergabe/ausschreibung/bekanntmachung.md
- [ ] A013 Rechtsprüfung und Freigabe-Vermerke
- [ ] A014 Angebots-Eingangs-Protokoll

## Phase 3.4: Integration
- [ ] A015 Bieter-Kommunikations-System mit vergabe/ausschreibung verknüpfen
- [ ] A016 Bewertungs-Workflow mit rechtlichen Vorgaben
- [ ] A017 Dokumentations-Automatisierung und Archivierung
- [ ] A018 Fristen-Management und Terminüberwachung

## Phase 3.5: Finalisierung
- [ ] A019 [P] Rechtsprüfungs-Tests in unterlagen/rechtsprüfung/final_review.md
- [ ] A020 Vollständigkeits-Prüfung (<10 Werktage für Einsprüche)
- [ ] A021 [P] Vergabe-Dokumentation aktualisieren
- [ ] A022 Doppel-Arbeiten eliminieren
- [ ] A023 Manuelle-Prüfung.md ausführen

## Abhängigkeiten
- Tests (A004-A007) vor Umsetzung (A008-A014)
- A008 blockiert A009, A015
- A016 blockiert A018
- Umsetzung vor Finalisierung (A019-A023)

## Parallel-Beispiel
```
# A004-A007 zusammen starten:
Task: "Vertrags-Test für Rahmenvertrag in unterlagen/rechtsprüfung/test_rahmenvertrag.md"
Task: "Vertrags-Test für Leistungsbeschreibung in unterlagen/rechtsprüfung/test_leistung.md"
Task: "Integrations-Test Ausschreibungsverfahren in unterlagen/tests/test_ausschreibung.md"
Task: "Integrations-Test Bewertungsverfahren in unterlagen/tests/test_bewertung.md"
```

## Notizen
- [P] Aufgaben = verschiedene Dateien, keine Abhängigkeiten
- Tests verifizieren dass sie fehlschlagen vor Umsetzung
- Nach jeder Aufgabe committen
- Vermeiden: vage Aufgaben, gleiche Datei-Konflikte

## Aufgaben-Generierungs-Regeln
*Angewendet während main() Ausführung*

1. **Aus Verträgen**:
   - Jede Vertrags-Datei → Vertrags-Test-Aufgabe [P]
   - Jede Klausel → Umsetzungs-Aufgabe
   
2. **Aus Leistungsverzeichnis**:
   - Jedes Leistungselement → Spezifikations-Erstellungs-Aufgabe [P]
   - Beziehungen → Service-Layer-Aufgaben
   
3. **Aus Benutzer-Geschichten**:
   - Jede Geschichte → Integrations-Test [P]
   - Schnellstart-Szenarien → Validierungs-Aufgaben

4. **Reihenfolge**:
   - Setup → Tests → Ausschreibung → Bewertung → Zuschlag → Finalisierung
   - Abhängigkeiten blockieren parallele Ausführung

## Validierungs-Checkliste
*GATE: Durch main() vor Rückgabe geprüft*

- [ ] Alle Verträge haben entsprechende Tests
- [ ] Alle Leistungselemente haben Spezifikations-Aufgaben
- [ ] Alle Tests kommen vor Umsetzung
- [ ] Parallele Aufgaben sind wirklich unabhängig
- [ ] Jede Aufgabe spezifiziert exakten Datei-Pfad
- [ ] Keine Aufgabe modifiziert gleiche Datei wie andere [P] Aufgabe

## Vergabe-Spezifische Validierung

### Rechtliche Compliance
- [ ] UVgO/VgV-Vorschriften in allen Phasen berücksichtigt
- [ ] Mindest-Fristen für Ausschreibung und Angebots-Abgabe eingehalten
- [ ] Gleichbehandlungs-Grundsatz in Bewertungs-Aufgaben verankert
- [ ] Transparenz-Anforderungen in Dokumentations-Aufgaben integriert

### Verfahrens-Vollständigkeit
- [ ] Markt-Erkundung vor Ausschreibung geplant
- [ ] Bieter-Information vollständig und verständlich
- [ ] Bewertungs-Kriterien objektiv und nachvollziehbar
- [ ] Einspruchs-Verfahren und Fristen dokumentiert
- [ ] Vergabe-Akten-Führung systematisch organisiert

### Qualitäts-Sicherung
- [ ] Vier-Augen-Prinzip bei kritischen Entscheidungen
- [ ] Rechtsprüfung in mehreren Phasen integriert
- [ ] Kosten-Nutzen-Bewertung dokumentiert
- [ ] Nach-Kalkulations-Prüfung bei auffälligen Angeboten
- [ ] Vertragsmanagement-Übergabe geplant