# Vergabe-Spezifikation: [PROJEKT-NAME]

**Vergabe-ID**: `[###-projekt-name]`  
**Erstellt**: [DATUM]  
**Status**: Entwurf  
**Eingabe**: Beschaffungsbedarf: "$ARGUMENTS"

## Ausführungsablauf (Hauptprozess)
```
1. Beschaffungsbedarf aus Eingabe analysieren
   → Falls leer: FEHLER "Kein Beschaffungsbedarf angegeben"
2. Schlüsselaspekte aus Beschreibung extrahieren
   → Identifizieren: Leistung, Budget, Zeitrahmen, Qualitätsanforderungen
3. Für jeden unklaren Aspekt:
   → Markieren mit [KLÄRUNGSBEDARF: spezifische Frage]
4. Benutzerszenarien & Vergabeverfahren festlegen
   → Falls kein klarer Ablauf erkennbar: FEHLER "Vergabeverfahren nicht bestimmbar"
5. Funktionale Anforderungen generieren
   → Jede Anforderung muss prüfbar sein
   → Mehrdeutige Anforderungen markieren
6. Zentrale Leistungselemente identifizieren (falls Dienstleistung)
7. Review-Checkliste durchlaufen
   → Falls [KLÄRUNGSBEDARF]: WARNUNG "Spezifikation hat Unklarheiten"
   → Falls Implementierungsdetails gefunden: FEHLER "Technische Details entfernen"
8. Rückgabe: ERFOLG (Spezifikation bereit für Planung)
```

---

## ⚡ Schnell-Leitfaden
- ✅ Fokus auf WAS benötigt wird und WARUM
- ❌ Vermeiden WIE umzusetzen (keine Anbieter-Vorgaben, Marken, detaillierte Technik)
- 👥 Geschrieben für Auftraggeber und Bieter, nicht für Techniker

### Abschnitts-Anforderungen
- **Pflichtabschnitte**: Müssen für jede Vergabe ausgefüllt werden
- **Optionale Abschnitte**: Nur einbeziehen wenn relevant für die Vergabe
- Wenn ein Abschnitt nicht zutrifft, komplett entfernen (nicht als "N/A" stehen lassen)

### Für KI-Generierung
Bei Erstellung dieser Spezifikation aus einem Benutzer-Prompt:
1. **Alle Mehrdeutigkeiten markieren**: Verwende [KLÄRUNGSBEDARF: spezifische Frage] für jede Annahme
2. **Nicht raten**: Falls der Prompt etwas nicht spezifiziert (z.B. "IT-System" ohne Budget), markieren
3. **Wie ein Prüfer denken**: Jede vage Anforderung sollte an der "prüfbar und eindeutig" Checkliste scheitern
4. **Häufige unterspecifizierte Bereiche**:
   - Nutzertypen und Berechtigungen
   - Budget- und Kostenvorgaben
   - Leistungs- und Qualitätsziele
   - Zeitliche Abläufe und Meilensteine
   - Integrations- und Schnittstellen-Anforderungen
   - Rechtliche/Compliance-Vorgaben

---

## Benutzerszenarien & Vergabe *(Pflicht)*

### Hauptszenario
[Beschreibung des zentralen Beschaffungsbedarfs in einfacher Sprache]

### Vergabeverfahren-Szenarien
1. **Gegeben** [Ausgangslage], **Wenn** [Maßnahme], **Dann** [erwartetes Ergebnis]
2. **Gegeben** [Ausgangslage], **Wenn** [Maßnahme], **Dann** [erwartetes Ergebnis]

### Grenzfälle
- Was passiert wenn [Grenzfall-Bedingung]?
- Wie wird [Problemszenario] behandelt?

## Anforderungen *(Pflicht)*

### Funktionale Anforderungen
- **FA-001**: System MUSS [spezifische Fähigkeit, z.B. "Rechnungen automatisch prüfen"]
- **FA-002**: System MUSS [spezifische Fähigkeit, z.B. "Berichte in PDF-Format exportieren"]  
- **FA-003**: Nutzer MÜSSEN [Hauptinteraktion, z.B. "Daten ohne Schulung eingeben können"]
- **FA-004**: System MUSS [Datenverarbeitung, z.B. "Eingaben binnen 24h verarbeiten"]
- **FA-005**: System MUSS [Verhalten, z.B. "alle Änderungen protokollieren"]

*Beispiel für Markierung unklarer Anforderungen:*
- **FA-006**: System MUSS Nutzer authentifizieren via [KLÄRUNGSBEDARF: Authentifizierungsmethode nicht spezifiziert - Passwort, SSO, Chipkarte?]
- **FA-007**: System MUSS Daten aufbewahren für [KLÄRUNGSBEDARF: Aufbewahrungsdauer nicht angegeben]

### Zentrale Leistungselemente *(einbeziehen falls Dienstleistung)*
- **[Element 1]**: [Was repräsentiert es, Schlüsselattribute ohne Implementierung]
- **[Element 2]**: [Was repräsentiert es, Beziehungen zu anderen Elementen]

---

## Review & Abnahme-Checkliste
*GATE: Automatische Prüfungen während Hauptausführung*

### Inhaltliche Qualität
- [ ] Keine Implementierungsdetails (Programmiersprachen, Frameworks, APIs)
- [ ] Fokus auf Nutzerwert und Geschäftsbedarf
- [ ] Für Nicht-Techniker geschrieben
- [ ] Alle Pflichtabschnitte ausgefüllt

### Anforderungs-Vollständigkeit
- [ ] Keine [KLÄRUNGSBEDARF] Markierungen verbleiben
- [ ] Anforderungen sind prüfbar und eindeutig  
- [ ] Erfolgskriterien sind messbar
- [ ] Umfang ist klar abgegrenzt
- [ ] Abhängigkeiten und Annahmen identifiziert

---

## Ausführungs-Status
*Aktualisiert durch Hauptprozess während Verarbeitung*

- [ ] Beschaffungsbedarf analysiert
- [ ] Schlüsselkonzepte extrahiert
- [ ] Mehrdeutigkeiten markiert
- [ ] Benutzerszenarien definiert
- [ ] Anforderungen generiert
- [ ] Elemente identifiziert
- [ ] Review-Checkliste bestanden

---