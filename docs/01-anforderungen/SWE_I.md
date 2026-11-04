# Reparaturfee – Software Engineering Projekt (SWE I)

> Kaputt ist nicht das Ende, hier helfen viele Hände.

Export des Miro-Boards (Übungsblatt 1 und 2) als Markdown. Die Reihenfolge folgt dem inhaltlichen Ablauf: Personas → Szenario → User Stories → Anwendungsfälle → Anforderungen → Akzeptanzkriterien → Features und Roadmap.

## Inhalt

- [Personas](#personas)
- [Szenario](#szenario-sabines-kaffeemaschine-bekommt-ein-zweites-leben)
- [Aufgabe 5: User Stories](#aufgabe-5-user-stories)
- [Aufgabe 6: Anwendungsfalldiagramm](#aufgabe-6-anwendungsfalldiagramm)
- [Aufgabe 7: Anwendungsfall detailliert](#aufgabe-7-anwendungsfall-detailliert)
- [Aufgabe 1: Funktionale Anforderungen](#aufgabe-1-funktionale-anforderungen)
- [Aufgabe 2: Nicht-funktionale Anforderungen](#aufgabe-2-nicht-funktionale-anforderungen)
- [Aufgabe 3: Akzeptanzkriterien](#aufgabe-3-akzeptanzkriterien)
- [Aufgabe 4: Features und Roadmap](#aufgabe-4-features-und-roadmap)

## Personas

### Persona 1: Sabine, die Hilfesuchende

**Nutzergruppe:** Menschen mit defekten Geräten, die über die App Hilfe suchen.

**Demografische Daten**

| Merkmal | Angabe |
|---|---|
| Name | Sabine Weber |
| Alter | 67 |
| Beruf | Rentnerin, ehemals Buchhalterin |
| Wohnort | Freiburg, Stadtteil Wiehre |
| Familienstand | verwitwet, zwei erwachsene Kinder |
| Bildung | kaufmännische Ausbildung |
| Einkommen | ca. 1.600 € Rente im Monat |

**Verhalten in der Vergangenheit**

- Hat ein Repair Café einmal über die Lokalzeitung entdeckt
- Fragt bei Problemen zuerst Kinder oder Nachbarn
- Nutzt WhatsApp und E-Mail, sonst kaum Apps
- Hat Geräte schon weggeworfen, weil die Reparatur zu teuer war

**Ziele**

- Kaffeemaschine und Nähmaschine weiter nutzen
- Geld sparen und Müll vermeiden
- Selbstständig Hilfe organisieren, ohne die Kinder zu fragen
- Neue Leute im Viertel kennenlernen

**Qualitätswahrnehmung**

- Freundliche, geduldige Helfer zählen mehr als Tempo
- Verlässliche Termine ohne kurzfristige Absagen
- Transparenz: Was wurde repariert, hält es?
- Kompliziertes Registrieren schreckt sie ab

**Bedürfnisse**

- Einfache Bedienung mit großer Schrift
- Persönlicher Kontakt zu vertrauenswürdigen Helfern
- Klare Infos zu Ablauf, Ort und Kosten
- Erinnerung an vereinbarte Termine

**Probleme & Herausforderungen**

- Neue Geräte sind teuer, das Budget ist knapp
- Unsicher im Umgang mit Apps und Online-Formularen
- Kann den Defekt technisch nicht beschreiben
- Weiß nicht, welche Ersatzteile sie braucht und wo sie sie bekommt

### Persona 2: Jonas, der studentische Reparatur-Helfer

**Nutzergruppe:** Ehrenamtliche Helfer, die über die App Reparaturen anbieten.

**Demografische Daten**

| Merkmal | Angabe |
|---|---|
| Name | Jonas Keller |
| Alter | 25 |
| Beruf | Masterstudent Elektrotechnik, Werkstudent in einem Ingenieurbüro |
| Wohnort | Freiburg, Stadtteil Stühlinger, in einer WG |
| Familienstand | ledig, in einer Beziehung |
| Bildung | Bachelor Elektrotechnik, aktuell im Master |
| Einkommen | ca. 1.100 € im Monat aus Werkstudentenjob und BAföG |
| Interessen | hat Spaß am Tüfteln und Reparieren, lebt umweltbewusst und achtet auf Nachhaltigkeit |

**Verhalten in der Vergangenheit**

- Hilft seit 2 Jahren regelmäßig im Repair Café, angeworben von Martin
- Repariert für Kommilitonen Laptops, Handys und Kopfhörer
- Organisiert sich bisher über WhatsApp-Gruppen
- Liest Reparaturanleitungen auf iFixit und schaut Tutorials

**Ziele**

- Sein Wissen sinnvoll weitergeben
- Elektroschrott in der Stadt reduzieren
- Mehr Reparaturen in weniger Zeit schaffen
- Andere zum Selbstreparieren ermutigen

**Qualitätswahrnehmung**

- Schnelle, übersichtliche App ohne Werbung
- Vollständige Anfragen mit Fotos und Modell
- Verbindliche Terminbestätigung durch Nutzer
- Datenschutz und klare Regeln zur Haftung

**Bedürfnisse**

- Anfragen nach eigenem Fachgebiet filtern
- Termine flexibel neben Vorlesungen und Prüfungen planen
- Vorab genug Infos und Fotos zum Defekt
- Praxiserfahrung und Anerkennung, z. B. als Nachweis für den Lebenslauf

**Probleme & Herausforderungen**

- In der Prüfungsphase kaum Zeit für Reparaturen
- Ungenaue Beschreibungen kosten Zeit
- Unsicher bei Haftung und älteren Geräten ohne Unterlagen
- Nutzer erscheinen nicht zum Termin

### Persona 3: Rosa, die Mitgründerin

**Nutzergruppe:** Mitgründerin des Repair Cafés, die Stadt, Ehrenamtliche und Technik-Helfer zusammenbringt.

**Demografische Daten**

| Merkmal | Angabe |
|---|---|
| Name | Rosa Müller |
| Alter | 52 |
| Beruf | früher Verwaltungsangestellte im Umweltamt der Stadt Freiburg, heute Mitgründerin des Repair Cafés |
| Wohnort | Freiburg, Stadtteil Vauban |
| Familienstand | verheiratet, zwei Kinder (17 und 20) |
| Bildung | Studium Verwaltungswissenschaften |
| Einkommen | ca. 2.300 € netto im Monat |
| Interessen | Umweltschutz und nachhaltiger Konsum, die Gemeinschaft und Nachbarschaft im Stadtteil stärken |

**Verhalten in der Vergangenheit**

- Hat über ihre Arbeit bei der Stadt Kontakte zu Ämtern, Vereinen und Förderprogrammen
- Hat das Repair Café gemeinsam mit dem Elektromeister Martin gegründet
- Organisiert Räume und Fördergelder über die Stadt
- Lässt technische Fragen bisher immer von Martin klären

**Ziele**

- Gezielt nach Helfern mit fehlenden Fähigkeiten suchen und sie gewinnen
- Ein festes Team aus Technik-Experten und Ehrenamtlichen aufbauen
- Ihre Verbindung zur Stadt nutzen, um das Café langfristig zu sichern
- Wirkung des Cafés sichtbar machen

**Qualitätswahrnehmung**

- Alles an einem Ort, auch am Laptop nutzbar
- Zuverlässige Daten und DSGVO-Konformität
- Kostenlos oder sehr günstig für Vereine
- Einfach genug für alle Ehrenamtlichen

**Bedürfnisse**

- Neue Helfer finden, z. B. über Stadt, Hochschule und Vereine
- Eine technikaffine Person an ihrer Seite, die Geräte und Reparaturen einschätzen kann
- Direkter Draht zu den ehrenamtlichen Helfern
- Zahlen und Erfolge, um sie der Stadt zu zeigen

**Probleme & Herausforderungen**

- Kennt sich mit Technik und Reparaturen kaum aus
- Kann nicht beurteilen, welcher Helfer für welches Gerät passt
- Ehrenamtliche sind schwer zu erreichen und zu halten
- Infos verstreut auf Excel, E-Mail und WhatsApp

### Persona 4: Martin, der technische Mitgründer

**Nutzergruppe:** Technische Leitung des Repair Cafés, die Ehrenamtliche koordiniert und Reparaturen fachlich begleitet.

**Demografische Daten**

| Merkmal | Angabe |
|---|---|
| Name | Martin Hoffmann |
| Alter | 58 |
| Beruf | Elektromeister mit eigenem kleinen Betrieb, Mitgründer und technische Leitung des Repair Cafés |
| Wohnort | Freiburg, Stadtteil Herdern |
| Familienstand | verheiratet, eine erwachsene Tochter |
| Bildung | Meister im Elektrotechniker-Handwerk |
| Einkommen | ca. 3.800 € netto im Monat |

**Verhalten in der Vergangenheit**

- Hat das Repair Café vor 6 Jahren mit Rosa gegründet
- Hat Jonas und weitere Helfer selbst angeworben und eingearbeitet
- Beantwortet technische Fragen per Telefon und WhatsApp
- Führt eine handschriftliche Liste mit Fähigkeiten der Helfer

**Ziele**

- Anfragen automatisch an passende Helfer weitergeben
- Wissen im Team teilen, damit nicht alles an ihm hängt
- Neue Ehrenamtliche schneller einarbeiten
- Rosa bei technischen Entscheidungen entlasten

**Qualitätswahrnehmung**

- Klare Fehlerangaben mit Foto und Modellnummer
- Sicherheitshinweise bei gefährlichen Geräten
- Helferprofile mit geprüften Fähigkeiten
- Funktioniert zuverlässig, auch auf dem Handy in der Werkstatt

**Bedürfnisse**

- Überblick, welcher Helfer welche Geräte reparieren kann
- Anfragen vorab fachlich prüfen und einschätzen
- Schneller Kontakt zu allen Ehrenamtlichen
- Sichere Abläufe bei Elektrogeräten

**Probleme & Herausforderungen**

- Alle technischen Fragen landen bei ihm
- Neue Helfer brauchen Einarbeitung und Sicherheitsregeln
- Wenig Zeit neben dem eigenen Betrieb
- Haftung bei fehlerhaften Reparaturen ist unklar

## Szenario: Sabines Kaffeemaschine bekommt ein zweites Leben

**Kernfunktion:** Reparaturanfrage stellen, Diagnosetermin und Reparaturtermin vereinbaren. **Persona:** Sabine Weber (67).

**Beteiligte Personas:** Hauptpersona Sabine Weber (67), Hilfesuchende. Beteiligt: Jonas Keller (studentischer Helfer).

### Ausgangssituation

Es ist Montagmorgen in Freiburg. Sabine will sich wie jeden Tag einen Kaffee machen, doch ihre Kaffeemaschine pumpt kein Wasser mehr und brummt nur laut. Die Maschine ist acht Jahre alt und ein Geschenk ihres verstorbenen Mannes. Eine neue kostet über 300 €, das sprengt ihr Budget. Ihre Nachbarin erzählt ihr von der Repair-Café-App. Ihre Tochter hilft ihr am Telefon, die App zu installieren.

### Interaktion mit der App (UC-02)

Beim ersten Öffnen kann Sabine eine große Schrift wählen. Sie registriert sich nur mit Name, Telefonnummer und Postleitzahl. Sie tippt auf „Gerät reparieren lassen“ und wählt „Küchengerät“ und „Kaffeemaschine“. Statt Fachbegriffe zu verlangen, zeigt die App typische Probleme zur Auswahl. Sabine wählt „Pumpt kein Wasser“ und „Macht laute Geräusche“. Ein Beispielbild zeigt ihr, wo das Typenschild sitzt, und sie lädt ein Foto hoch. Die App schlägt Jonas vor, Masterstudent der Elektrotechnik mit 4,9 Sternen. Sabine bucht bei ihm einen Diagnosetermin am Samstag um 11 Uhr im Stadtteiltreff und bringt die Maschine selbst mit. Beim Diagnosetermin öffnet Jonas die Maschine und stellt fest, dass ein Schlauch verkalkt ist. Er trägt die Diagnose in der App ein und empfiehlt einen neuen Schlauch, optional mit einem Richtpreis von etwa 6 €. Sabine bekommt die Empfehlung direkt aufs Handy. Sabine kauft den Schlauch selbst im Haushaltswarengeschäft, markiert in der App „Ersatzteil vorhanden“ und bucht beim selben Helfer einen Reparaturtermin für den nächsten Café-Tag.

### Ergebnis

Vor beiden Terminen erinnert sie eine SMS. Beim Reparaturtermin baut Jonas den neuen Schlauch ein und zeigt ihr, wie sie die Maschine entkalkt. Sabine bewertet Jonas mit fünf Sternen. Sie trinkt ihren Kaffee wieder zu Hause und ist stolz, dass sie alles selbst organisiert hat.

### Zusammenfassung

| Aspekt | Inhalt |
|---|---|
| Übergeordnetes Ziel | Ihr defektes Gerät fachkundig prüfen und günstig reparieren lassen, ohne auf andere angewiesen zu sein |
| Was zur Zielerreichung nötig ist | Einfache Registrierung, geführte Fehlerbeschreibung, Foto-Upload, Helfersuche, Diagnosetermin, Ersatzteilempfehlung, Reparaturtermin, Erinnerung |
| Problem mit dem bestehenden System | Repair Cafés sind kaum bekannt, Infos über Flyer und Mundpropaganda, lange Warteschlangen, Ersatzteile fehlen oft am Reparaturtag |
| Mögliche Problemlösungen | Barrierearme App mit großer Schrift, Fehlerauswahl statt Fachbegriffe, getrennter Diagnose- und Reparaturtermin, digitale Ersatzteilempfehlung, Helferprofile mit Bewertungen, SMS-Erinnerung |

## Aufgabe 5: User Stories

Format: Als \[Rolle\] \[möchte / will / muss\] ich \[etwas tun\], damit \[Grund\]. Basierend auf den Personas Sabine, Jonas, Rosa und Martin.

| ID | User Story | Persona | Priorität |
|---|---|---|---|
| US1 | Als Hilfesuchende möchte ich mich nur mit Name, Telefonnummer und Postleitzahl registrieren, damit ich ohne komplizierte Formulare starten kann. | Sabine | Hoch |
| US2 | Als Hilfesuchende möchte ich den Defekt über eine Auswahl typischer Probleme beschreiben, damit ich keine Fachbegriffe kennen muss. | Sabine | Hoch |
| US3 | Als Hilfesuchende möchte ich zuerst einen Diagnosetermin bei einem bewerteten Helfer buchen, damit ein Fachkundiger feststellt, was am Gerät kaputt ist. | Sabine | Hoch |
| US4 | Als Hilfesuchende möchte ich nach der Diagnose eine Ersatzteilempfehlung aufs Handy bekommen, damit ich das Teil selbst kaufen und danach einen Reparaturtermin buchen kann. | Sabine | Hoch |
| US5 | Als ehrenamtlicher Helfer möchte ich Anfragen nach meinem Fachgebiet filtern und Fotos vorab sehen, damit ich mich vorbereiten und gezielt helfen kann. | Jonas | Hoch |
| US6 | Als ehrenamtlicher Helfer möchte ich nach der Diagnose ein Ersatzteil empfehlen und optional einen Richtpreis angeben, damit die Person das richtige Teil kauft. | Jonas | Hoch |
| US7 | Als technischer Leiter muss ich neue Anfragen fachlich prüfen und einem passenden Helfer zuweisen können, damit jedes Gerät von der richtigen Person repariert wird. | Martin | Hoch |
| US8 | Als technischer Leiter möchte ich die Fähigkeiten aller Helfer in Profilen pflegen, damit ich keine handschriftliche Liste mehr führen muss. | Martin | Mittel |
| US9 | Als Mitgründerin möchte ich Café-Termine planen und Auswertungen zu Reparaturen exportieren, damit ich der Stadt den Erfolg zeigen und Fördergelder sichern kann. | Rosa | Mittel |
| US10 | Als Mitgründerin möchte ich nach neuen Helfern mit bestimmten Fähigkeiten suchen und sie einladen, damit genug Ehrenamtliche für alle Anfragen da sind. | Rosa | Hoch |

**Analyse:** US1 bis US4 bilden den Kern des Szenarios mit Sabine. US4 und US6 hängen direkt zusammen: Erst die Diagnose von Jonas macht Ersatzteilkauf und Reparaturtermin möglich. US10 sichert, dass genug Helfer für alle Anfragen da sind.

## Aufgabe 6: Anwendungsfalldiagramm

**Systemgrenze:** Repair-Café-App. Im Miro-Diagramm zeigen gestrichelte Pfeile «include»-Beziehungen. Fokus auf die 13 wichtigsten Anwendungsfälle (UC-01 bis UC-13). Das Diagramm selbst (Pfeile und Layout) ist nur im Miro-Board enthalten, hier stehen Akteure und Anwendungsfälle.

**Akteure**

- Hilfesuchende (Sabine)
- Helfer (Jonas)
- Technischer Leiter (Martin)
- Mitgründerin (Rosa)
- «System» SMS-Dienst

**Anwendungsfälle**

- **UC-01** Registrieren
- **UC-02** Reparaturanfrage stellen
- **UC-03** Defekt beschreiben und Foto hochladen
- **UC-04** Helfer auswählen
- **UC-05** Diagnosetermin buchen
- **UC-06** Reparaturtermin buchen
- **UC-07** Terminerinnerung senden
- **UC-08** Diagnose stellen und Ersatzteil empfehlen
- **UC-09** Verfügbarkeit eintragen
- **UC-10** Anfrage prüfen und zuweisen
- **UC-11** Helferprofile verwalten
- **UC-12** Café-Termine planen und auswerten
- **UC-13** Neue Helfer suchen und gewinnen

## Aufgabe 7: Anwendungsfall detailliert

Strukturierter Anwendungsfall, abgeleitet aus dem Szenario „Sabines Kaffeemaschine bekommt ein zweites Leben“.

### UC-02 Reparaturanfrage stellen, Diagnose- und Reparaturtermin buchen

| Aspekt | Inhalt |
|---|---|
| Primärer Akteur | Hilfesuchende (Sabine) |
| Sekundäre Akteure | Helfer (Jonas), SMS-Dienst |
| Ziel | Das Gerät ist diagnostiziert, die Hilfesuchende hat die Ersatzteile selbst gekauft und einen bestätigten Reparaturtermin. |
| Vorbedingungen | App ist installiert, Nutzerin ist registriert und angemeldet. Mindestens ein Helfer mit freiem Zeitfenster ist im Umkreis verfügbar. |
| Nachbedingung | Anfrage, Diagnose mit Ersatzteilempfehlung und beide Termine sind gespeichert, der Helfer ist informiert, Erinnerungen sind geplant. |
| Beteiligte Systeme | Repair-Café-App (Mobil-App), Backend mit Datenbank für Anfragen, Helfer und Termine, SMS-Dienst für Erinnerungen, Kartendienst für die Umkreissuche, Bildspeicher für Fotos. |

**Hauptablauf**

1. Nutzerin wählt „Gerät reparieren lassen“.
2. System fragt die Gerätekategorie ab, Nutzerin wählt „Küchengerät“ und „Kaffeemaschine“.
3. System zeigt typische Fehlerbilder, Nutzerin wählt passende Probleme aus.
4. System fordert ein Foto vom Typenschild an, Nutzerin lädt es hoch.
5. System schlägt passende Helfer mit Bewertungen vor, Nutzerin wählt einen aus.
6. Nutzerin bucht einen Diagnosetermin.
7. Beim Diagnosetermin prüft der Helfer das Gerät und erfasst die Diagnose sowie eine Empfehlung für das benötigte Ersatzteil, optional mit Richtpreis.
8. System schickt der Nutzerin die Ersatzteilempfehlung.
9. Nutzerin kauft das Ersatzteil selbst und markiert „Ersatzteil vorhanden“.
10. System bietet freie Reparaturtermine beim selben Helfer an.
11. Nutzerin bucht den Reparaturtermin.
12. System speichert den Termin, benachrichtigt den Helfer und plant eine SMS-Erinnerung.

**Alternativer Ablauf**

- 4a. Kein Typenschild auffindbar: Nutzerin überspringt das Foto und beschreibt das Gerät frei.
- 7a. Kein Ersatzteil nötig: Der Helfer repariert direkt beim Diagnosetermin, Schritte 8 bis 12 entfallen.

**Ausnahmen**

- 5e. Kein passender Helfer verfügbar: Anfrage kommt auf eine Warteliste, der technische Leiter wird informiert.
- 7e. Reparatur lohnt sich nicht: Helfer vermerkt das, System schlägt Recycling oder Entsorgung vor.
- 9e. Ersatzteil nicht erhältlich: Nutzerin meldet das, Helfer schlägt eine Alternative vor.

## Aufgabe 1: Funktionale Anforderungen

Schema: Nach \[Bedingung\] muss das System \[Akteur\] die Möglichkeit bieten, \[Funktion\] auszuführen. Abgeleitet aus User Stories (US1 bis US10), dem Anwendungsfalldiagramm und UC-02.

Alle Anforderungen: Version 1, Status Entwurf.

| ID | Feature | Priorität | Anforderungsname | Beschreibung | Quelle |
|---|---|---|---|---|---|
| F-010 | Registrierung | Muss | Kurzregistrierung | Nach dem ersten Öffnen der App muss das System neuen Hilfesuchenden die Möglichkeit bieten, sich nur mit Name, Telefonnummer und/ oder Emailadresse zu registrieren. | US1, UC-01 |
| F-020 | Reparaturanfrage | Muss | Defekt auswählen | Nach Auswahl der Gerätekategorie muss das System angemeldeten Hilfesuchenden die Möglichkeit bieten, den Defekt aus einer Liste typischer Fehlerbilder auszuwählen. | US2, UC-03 |
| F-030 | Terminbuchung | Muss | Diagnosetermin buchen | Nach Absenden einer Reparaturanfrage muss das System angemeldeten Hilfesuchenden die Möglichkeit bieten, einen vorgeschlagenen Helfer mit Bewertung auszuwählen und bei ihm einen freien Diagnosetermin zu buchen. | US3, UC-04, UC-05 |
| F-040 | Diagnose | Muss | Ersatzteil empfehlen | Nach Durchführung eines Diagnosetermins muss das System Helfern die Möglichkeit bieten, die Diagnose und eine Ersatzteilempfehlung mit optionalem Richtpreis zu erfassen. | US6, UC-08 |
| F-050 | Diagnose | Muss | Ersatzteilempfehlung einsehen | Nach Speichern einer Ersatzteilempfehlung durch den Helfer muss das System der Hilfesuchenden die Möglichkeit bieten, die Empfehlung in der App einzusehen. | US4, UC-02 |
| F-060 | Terminbuchung | Muss | Reparaturtermin buchen | Nach Markieren von „Ersatzteil vorhanden“ muss das System Hilfesuchenden die Möglichkeit bieten, einen freien Reparaturtermin beim selben Helfer zu buchen. | US4, UC-06 |
| F-070 | Anfragenübersicht | Muss | Anfragen filtern | Nach Anmeldung als Helfer muss das System Helfern die Möglichkeit bieten, offene Anfragen nach Fachgebiet zu filtern und die zugehörigen Fotos anzusehen. | US5 |
| F-080 | Verwaltung | Muss | Anfrage zuweisen | Nach Eingang einer neuen Reparaturanfrage muss das System dem technischen Leiter die Möglichkeit bieten, die Anfrage zu prüfen und einem passenden Helfer zuzuweisen. | US7, UC-10 |
| F-090 | Reparaturanfrage | Soll | Typenschild-Foto hochladen | Nach Auswahl des Defekts muss das System angemeldeten Hilfesuchenden die Möglichkeit bieten, ein Foto des Typenschilds hochzuladen oder diesen Schritt zu überspringen. | US2, UC-03 |
| F-100 | Benachrichtigung | Soll | SMS-Erinnerung aktivieren | Nach Buchung eines Diagnose- oder Reparaturtermins muss das System Hilfesuchenden die Möglichkeit bieten, eine SMS-Erinnerung 24 Stunden vor dem Termin zu aktivieren. | UC-07 |
| F-110 | Verwaltung | Soll | Helferprofil pflegen | Nach Anmeldung als technischer Leiter muss das System dem technischen Leiter die Möglichkeit bieten, die Fähigkeiten jedes Helfers in dessen Profil anzulegen und zu bearbeiten. | US8, UC-11 |
| F-120 | Helfergewinnung | Kann | Neue Helfer einladen | Nach Eingabe einer gesuchten Fähigkeit muss das System der Mitgründerin die Möglichkeit bieten, registrierte Nutzer mit dieser Fähigkeit zu finden und als Helfer einzuladen. | US10, UC-13 |

## Aufgabe 2: Nicht-funktionale Anforderungen

Messbare Qualitätsziele mit Prüfbedingung. Geltungsbereich „Gesamtsystem“ gilt für alle Features, sonst nur für die genannten Features aus Aufgabe 1.

### ReqMOB-N010 – Große Schrift und Kontrast

- **Priorität:** Muss
- **Qualitätsmerkmal:** Barrierefreiheit
- **Eigenschaft:** Benutzerfreundlichkeit
- **Geltungsbereich:** Gesamtsystem (App für Hilfesuchende)
- **Quelle:** US1, US2, UC-01, UC-02
- **Beschreibung:** Alle Bildschirme müssen bei einer Systemschriftgröße von 200 % ohne abgeschnittene Inhalte lesbar sein und einen Textkontrast von mindestens 4,5:1 (WCAG 2.1 AA) einhalten. Prüfung mit einem automatischen Barrierefreiheits-Tool und manuell auf je einem Android- und iOS-Gerät.
- **Metrik:** Kontrastverhältnis (x:1), Schriftskalierung ohne Abschneiden (%)
- **Zielwert:** ≥ 4,5:1 und 200 %

### ReqMOB-N020 – Anfrage ohne Hilfe abschließen

- **Priorität:** Muss
- **Qualitätsmerkmal:** Benutzbarkeit
- **Eigenschaft:** Benutzerfreundlichkeit
- **Geltungsbereich:** Reparaturanfrage, Terminbuchung
- **Quelle:** US2, US3, UC-02, UC-05
- **Beschreibung:** In einem Usability-Test mit 5 Personen ab 65 Jahren ohne Vorerfahrung mit der App müssen mindestens 4 Personen eine Reparaturanfrage inklusive Diagnosetermin ohne fremde Hilfe in höchstens 20 Minuten abschließen.
- **Metrik:** Bearbeitungszeit (Minuten), Erfolgsquote ohne Hilfe (Personen)
- **Zielwert:** ≤ 20 min, ≥ 4 von 5

### ReqMOB-N030 – Antwortzeit Helfervorschläge

- **Priorität:** Kann
- **Qualitätsmerkmal:** Performance
- **Eigenschaft:** Geschwindigkeit
- **Geltungsbereich:** Terminbuchung
- **Quelle:** US3, UC-04
- **Beschreibung:** Bei 200 gleichzeitig aktiven Nutzern müssen mindestens 95 % der Helfervorschläge innerhalb von 2 Sekunden angezeigt werden. Prüfung per Lasttest mit simulierter 4G-Verbindung.
- **Metrik:** Antwortzeit auf Benutzereingabe (Sekunden, 95. Perzentil), ausgeführte Transaktionen/Sekunde
- **Zielwert:** ≤ 2 s bei 200 gleichzeitigen Nutzern

### ReqMOB-N040 – DSGVO-konforme Datenhaltung

- **Priorität:** Muss
- **Qualitätsmerkmal:** Datenschutz
- **Eigenschaft:** Datenschutz
- **Geltungsbereich:** Gesamtsystem
- **Quelle:** US1, UC-01
- **Beschreibung:** Personenbezogene Daten (Name, Telefonnummer, Postleitzahl, Fotos) müssen ausschließlich auf Servern in der EU gespeichert werden. Auf Löschanfrage müssen alle Daten einer Person innerhalb von 30 Tagen vollständig gelöscht sein. Prüfung durch ein Datenschutz-Audit vor dem Release.
- **Metrik:** Anteil Daten auf EU-Servern (%), Dauer bis vollständige Löschung (Tage)
- **Zielwert:** 100 %, ≤ 30 Tage

### ReqMOB-N050 – Rollenbasierter Datenzugriff

- **Priorität:** Muss
- **Qualitätsmerkmal:** Sicherheit
- **Eigenschaft:** Sicherheit
- **Geltungsbereich:** Anfragenübersicht, Verwaltung
- **Quelle:** US5, US7, UC-10
- **Beschreibung:** Die Telefonnummer einer Hilfesuchenden darf nur für den zugewiesenen Helfer und den technischen Leiter sichtbar sein. Prüfung durch Rollentests mit allen vier Rollen; in 100 % der Testfälle darf keine unberechtigte Rolle die Nummer sehen.
- **Metrik:** Quote unberechtigter Zugriffe in Rollentests (%)
- **Zielwert:** 0 %

### ReqMOB-N060 – SMS-Erinnerung am Vortag

- **Priorität:** Kann
- **Qualitätsmerkmal:** Zuverlässigkeit
- **Eigenschaft:** Zuverlässigkeit
- **Geltungsbereich:** Benachrichtigung
- **Quelle:** UC-07
- **Beschreibung:** Jede Person mit gebuchtem Termin erhält am Tag vor dem Termin eine SMS-Erinnerung. Mindestens 99 % der Erinnerungen müssen höchstens 10 Minuten nach dem geplanten Versandzeitpunkt zugestellt sein. Messung über einen Monat anhand des Zustellprotokolls des SMS-Dienstes.
- **Metrik:** Quote für das Auftreten von Fehlern (nicht rechtzeitig zugestellte SMS, %)
- **Zielwert:** ≤ 1 % pro Monat

### ReqMOB-N080 – Automatisch getesteter Code

- **Priorität:** Soll
- **Qualitätsmerkmal:** Wartbarkeit
- **Eigenschaft:** Wartbarkeit
- **Geltungsbereich:** Gesamtsystem
- **Quelle:** US1 bis US10
- **Beschreibung:** Mindestens 80 % des Backend-Codes sind durch automatische Tests abgedeckt. Die Tests laufen bei jeder Änderung automatisch mit.
- **Metrik:** Testabdeckung Backend-Code (%)
- **Zielwert:** ≥ 80 %

### ReqMOB-N090 – Nutzbar am Laptop und auf der Website

- **Priorität:** Muss
- **Qualitätsmerkmal:** Benutzbarkeit
- **Eigenschaft:** Portierbarkeit
- **Geltungsbereich:** Gesamtsystem (Website und Laptop)
- **Quelle:** US9, US10, UC-12, UC-13
- **Beschreibung:** Die App muss auch als Website im Browser am Laptop vollständig nutzbar sein. Alle Funktionen müssen in den aktuellen Versionen von Chrome, Firefox, Edge und Safari ab einer Auflösung von 1366 x 768 Pixeln funktionieren. Prüfung durch Browsertests auf allen vier Browsern.
- **Metrik:** Anzahl der Zielsysteme (Browser), Anteil plattformabhängiger Anweisungen (%)
- **Zielwert:** 4 Browser, ≤ 5 % plattformabhängiger Code

### ReqMOB-N100 – Hohe Verfügbarkeit

- **Priorität:** Soll
- **Qualitätsmerkmal:** Zuverlässigkeit
- **Eigenschaft:** Verfügbarkeit
- **Geltungsbereich:** Gesamtsystem
- **Quelle:** US3, UC-05, UC-06
- **Beschreibung:** Die App muss im Monatsmittel zu mindestens 99,5 % erreichbar sein; die durchschnittliche Zeit bis zu einer Fehlfunktion beträgt mindestens 30 Tage. Messung über ein Monitoring-Tool.
- **Metrik:** Wahrscheinlichkeit der Nichtverfügbarkeit (%), durchschnittliche Zeit bis zu einer Fehlfunktion (Tage)
- **Zielwert:** ≤ 0,5 %, MTTF ≥ 30 Tage

### ReqMOB-N110 – Schneller Neustart ohne Datenverlust

- **Priorität:** Soll
- **Qualitätsmerkmal:** Zuverlässigkeit
- **Eigenschaft:** Stabilität
- **Geltungsbereich:** Reparaturanfrage, Terminbuchung
- **Quelle:** US2, UC-02
- **Beschreibung:** Nach einer Fehlfunktion ist das System innerhalb von 15 Minuten wieder verfügbar. Bereits abgeschickte Anfragen und Termine gehen dabei nicht verloren. Prüfung durch einen simulierten Serverausfall.
- **Metrik:** Zeit bis zum Neustart (Minuten), Wahrscheinlichkeit für Datenzerstörung bei Fehlfunktion (%)
- **Zielwert:** ≤ 15 min, 0 %

### ReqMOB-N120 – Kleine App-Größe

- **Priorität:** Kann
- **Qualitätsmerkmal:** Performance
- **Eigenschaft:** Größe
- **Geltungsbereich:** App für Hilfesuchende
- **Quelle:** US1, UC-01
- **Beschreibung:** Die App darf auf dem Smartphone höchstens 50 MB Speicher belegen, damit sie auch auf älteren Geräten installiert werden kann. Prüfung über die Installationsgröße im App-Store-Build.
- **Metrik:** Speicherbedarf (Megabyte)
- **Zielwert:** ≤ 50 MB

### ReqMOB-N130 – Kurze Einarbeitung für Helfer

- **Priorität:** Soll
- **Qualitätsmerkmal:** Benutzbarkeit
- **Eigenschaft:** Benutzerfreundlichkeit
- **Geltungsbereich:** Helfer- und Verwaltungsbereich
- **Quelle:** US5, US7, UC-08, UC-10
- **Beschreibung:** Neue ehrenamtliche Helfer können nach einer Einführung von höchstens 30 Minuten Anfragen annehmen und Termine bestätigen. Die Hilfe umfasst höchstens 10 Seiten. Prüfung mit 3 neuen Helfern.
- **Metrik:** Schulungsdauer (Minuten), Anzahl der Hilfeseiten
- **Zielwert:** ≤ 30 min, ≤ 10 Seiten

## Aufgabe 3: Akzeptanzkriterien

Drei funktionale (F-010, F-030, F-100) und zwei nicht-funktionale Anforderungen (N-020, N-030) mit je drei bis vier prüfbaren Kriterien: Erfolgsfall, Fehlerfall oder alternativer Ablauf, Messkriterium und Testbedingung.

### F-010 Kurzregistrierung (Funktional)

| Nr. | Aspekt | Ausformuliert | Akzeptanzkriterium | Testbedingung |
|---|---|---|---|---|
| AK-010-1 |  | Als Hilfesuchende möchte ich mich nur mit Name und Telefonnummer registrieren können, damit ich die App ohne lange Formulare sofort nutzen kann. | Gegeben: Die App wird zum ersten Mal geöffnet. Wenn: Name „Sabine Müller“ und Telefonnummer „0171 1234567“ eingegeben und „Registrieren“ getippt werden. Dann: Das Konto ist angelegt und die Startseite erscheint innerhalb von 3 Sekunden, ohne weitere Pflichtfelder. | Manueller Test auf je einem Android- und iOS-Gerät mit neuen Testdaten |
| AK-010-2 |  | Als Hilfesuchende möchte ich mich alternativ mit meiner E-Mail-Adresse registrieren können, damit ich meine Telefonnummer nicht angeben muss. | Wenn: Nur Name und E-Mail-Adresse ohne Telefonnummer angegeben werden. Dann: Die Registrierung ist erfolgreich und eine Bestätigungs-E-Mail kommt innerhalb von 60 Sekunden an. | Test-Postfach, Zeitmessung ab Tippen auf „Registrieren“ |
| AK-010-3 | Fehlerfall | Als Hilfesuchende möchte ich bei fehlenden oder ungültigen Kontaktdaten sofort einen klaren Hinweis am Feld sehen, damit ich meinen Fehler direkt korrigieren kann. | Wenn: Weder Telefonnummer noch E-Mail angegeben werden oder die Telefonnummer weniger als 6 Ziffern hat. Dann: Es erscheint der Hinweis „Bitte gültige Telefonnummer oder E-Mail angeben“ direkt am Feld, und es wird kein Konto angelegt. | Testfälle mit leerem Feld, „123“ und „abc@“ |
| AK-010-4 | Fehlerfall | Als Hilfesuchende möchte ich erfahren, wenn meine Nummer schon registriert ist, damit ich mich einfach anmelden kann und kein zweites Konto entsteht. | Wenn: Die Telefonnummer ist schon registriert. Dann: Die App zeigt „Diese Nummer ist bereits registriert“ mit einem Link zur Anmeldung. Es entsteht kein doppeltes Konto. | Vorab angelegtes Testkonto, Prüfung in der Datenbank |

### F-030 Diagnosetermin buchen (Funktional)

| Nr. | Aspekt | Ausformuliert | Akzeptanzkriterium | Testbedingung |
|---|---|---|---|---|
| AK-030-1 | Erfolgsfall | Als Hilfesuchende möchte ich einen bewerteten Helfer und einen freien Termin wählen und eine Bestätigung erhalten, damit ich sicher weiß, wann mein Gerät angeschaut wird. | Gegeben: Eine Anfrage „Toaster heizt nicht“ ist abgeschickt. Wenn: Die Hilfesuchende einen vorgeschlagenen Helfer (mit Sternebewertung) und einen freien Termin wählt und bestätigt. Dann: Der Termin ist gebucht, die Bestätigung erscheint in der App und kommt innerhalb von 60 Sekunden per SMS oder E-Mail. Der Termin steht im Kalender des Helfers. | Testumgebung mit 3 Helfern und je 5 freien Terminen |
| AK-030-2 | Fehlerfall | Als Hilfesuchende möchte ich informiert werden, wenn mein gewählter Termin inzwischen vergeben ist, damit ich direkt einen anderen freien Termin wählen kann. | Wenn: Der gewählte Termin wurde gerade von einer anderen Person gebucht. Dann: Die App meldet „Dieser Termin ist leider nicht mehr frei“ und zeigt die aktualisierten Termine. Es gibt keine Doppelbuchung. | Zwei Testgeräte buchen gleichzeitig denselben Termin |
| AK-030-3 | Alternativer Ablauf | Als Hilfesuchende möchte ich, dass meine Anfrage auch ohne verfügbaren Helfer offen bleibt, damit sich jemand um mein Gerät kümmert, sobald ein passender Helfer gefunden ist. | Wenn: Für die Gerätekategorie ist kein Helfer verfügbar. Dann: Die App zeigt „Wir suchen einen passenden Helfer für Sie“, die Anfrage bleibt offen und der technische Leiter wird benachrichtigt (F-080). | Gerätekategorie ohne zugeordneten Helfer |
| AK-030-4 | Fehlerfall | Als Hilfesuchende möchte ich bei einem Verbindungsabbruch meine Auswahl behalten und es erneut versuchen können, damit ich nicht alles neu eingeben muss. | Wenn: Die Internetverbindung beim Bestätigen abbricht. Dann: Die Auswahl bleibt erhalten, die App bietet „Erneut versuchen“ an, und es wird kein unvollständiger Termin gespeichert. | Flugmodus während der Buchung aktivieren |

### F-100 SMS-Erinnerung aktivieren (Funktional)

| Nr. | Aspekt | Ausformuliert | Akzeptanzkriterium | Testbedingung |
|---|---|---|---|---|
| AK-100-1 | Erfolgsfall | Als Hilfesuchende möchte ich 24 Stunden vor meinem Termin eine SMS mit allen wichtigen Angaben bekommen, damit ich den Termin nicht vergesse. | Gegeben: Ein Termin am Donnerstag um 15:00 Uhr ist gebucht. Wenn: Die SMS-Erinnerung aktiviert wird. Dann: Am Mittwoch zwischen 15:00 und 15:10 Uhr kommt eine SMS mit Datum, Uhrzeit, Ort und Name des Helfers. | Testtermin mit Testnummer, Zustellprotokoll des SMS-Dienstes |
| AK-100-2 | Alternativer Ablauf | Als Hilfesuchende möchte ich sehen, warum bei kurzfristigen Terminen keine Erinnerung möglich ist, damit ich nicht vergeblich auf eine SMS warte. | Wenn: Der Termin liegt weniger als 24 Stunden in der Zukunft. Dann: Die Option ist ausgegraut mit dem Hinweis „Erinnerung erst ab 24 Stunden vor dem Termin möglich“. | Termin für den gleichen Tag buchen |
| AK-100-3 | Alternativer Ablauf | Als Hilfesuchende möchte ich, dass sich die Erinnerung automatisch an abgesagte oder verschobene Termine anpasst, damit ich keine falschen Infos erhalte. | Wenn: Der Termin nach Aktivierung abgesagt oder verschoben wird. Dann: Für den alten Termin wird keine SMS verschickt, beim verschobenen Termin gilt die Erinnerung für das neue Datum. | Termin nach Aktivierung absagen bzw. verschieben |
| AK-100-4 | Fehlerfall | Als Hilfesuchende möchte ich auch bei SMS-Problemen zuverlässig erinnert werden, notfalls per E-Mail, damit ich meinen Termin trotzdem wahrnehme. | Wenn: Die SMS nicht zugestellt werden kann. Dann: Das System versucht es nach 5 und 15 Minuten erneut und schickt danach eine E-Mail, falls eine Adresse hinterlegt ist. | Ungültige Testnummer beim SMS-Dienst |

### N-020 Anfrage ohne Hilfe abschließen (Nicht-funktional)

| Nr. | Aspekt | Ausformuliert | Akzeptanzkriterium | Testbedingung |
|---|---|---|---|---|
| AK-N020-1 | Messkriterium | Als ältere Nutzerin ohne App-Erfahrung möchte ich eine Reparaturanfrage samt Termin ganz allein abschließen können, damit ich niemanden um Hilfe bitten muss. | Mindestens 4 von 5 Testpersonen schließen eine Reparaturanfrage inklusive Diagnosetermin ohne fremde Hilfe ab. | 5 Personen ab 65 Jahren, ohne Vorerfahrung, eigenes Smartphone, keine Einweisung |
| AK-N020-2 | Messkriterium | Als ältere Nutzerin möchte ich meine Anfrage in wenigen Minuten erledigen, damit mich die App weder überfordert noch unnötig Zeit kostet. | Die Testpersonen brauchen dafür durchschnittlich höchstens 5 Minuten, keine Person länger als 8 Minuten. | Stoppuhr vom Öffnen der App bis zur Buchungsbestätigung |
| AK-N020-3 | Messkriterium | Als ältere Nutzerin möchte ich mich in der App kaum vertippen oder verirren, damit ich mich bei der Bedienung sicher fühle. | Pro Person treten durchschnittlich höchstens 2 Fehlbedienungen auf (z. B. falscher Button, Zurück-Navigation aus Versehen). | Beobachtungsprotokoll, Moderator greift nicht ein |
| AK-N020-4 | Messkriterium | Als ältere Nutzerin möchte ich nach der Buchung genau wissen, wann und wo mein Termin ist, damit ich pünktlich am richtigen Ort bin. | Alle Testpersonen können nach dem Test Datum, Uhrzeit und Ort ihres gebuchten Termins richtig nennen. | Kurzinterview direkt nach dem Test |

### N-030 Antwortzeit Helfervorschläge (Nicht-funktional)

| Nr. | Aspekt | Ausformuliert | Akzeptanzkriterium | Testbedingung |
|---|---|---|---|---|
| AK-N030-1 | Messkriterium | Als Hilfesuchende möchte ich passende Helfervorschläge innerhalb von 2 Sekunden sehen, damit ich nicht ungeduldig werde und abbreche. | Bei 200 gleichzeitig aktiven Nutzern werden 95 % der Helfervorschläge innerhalb von 2 Sekunden und 99 % innerhalb von 4 Sekunden angezeigt. | Lasttest über 30 Minuten, simulierte 4G-Verbindung (100 ms Latenz), 500 Helfer in der Testdatenbank |
| AK-N030-2 | Fehlerfall | Als Hilfesuchende möchte ich bei längerer Wartezeit sehen, dass die App arbeitet, und ohne Datenverlust erneut suchen können, damit ich nicht im Unklaren bleibe. | Wenn: Die Antwort länger als 1 Sekunde dauert. Dann: Eine Ladeanzeige erscheint. Nach 15 Sekunden ohne Antwort zeigt die App „Bitte erneut versuchen“, die Eingaben bleiben erhalten. | Künstliche Serververzögerung von 20 Sekunden |
| AK-N030-3 | Stresstest | Als Hilfesuchende möchte ich, dass die App auch bei großem Andrang, etwa kurz vor einem Repair-Café, schnell bleibt, damit ich jederzeit buchen kann. | Das System skaliert bis 1.000 gleichzeitige Nutzer linear: Die Antwortzeit im 95. Perzentil steigt höchstens auf 4 Sekunden, die Fehlerquote bleibt unter 1 %. | Stufenweiser Lasttest mit 200, 500 und 1.000 Nutzern |

## Aufgabe 4: Features und Roadmap

Zusammengehörige Anforderungen aus Aufgabe 1 und 2 als Features gebündelt. Nicht-funktionale Anforderungen sind dem betroffenen Feature zugeordnet oder als übergreifend gekennzeichnet.

| Nr. | Feature | Beschreibung | Funktionale Anforderungen | Nicht-funktionale Anforderungen | Quelle | Roadmap |
|---|---|---|---|---|---|---|
| FE-1 | Registrierung | Schneller Einstieg in die App ohne lange Formulare. | F-010 Kurzregistrierung | ReqMOB-N120 Kleine App-Größe | US1, UC-01 | Sofort |
| FE-2 | Reparaturanfrage stellen | Defekt ohne Fachbegriffe beschreiben, optional mit Foto des Typenschilds. | F-020 Defekt auswählen, F-090 Typenschild-Foto hochladen | ReqMOB-N020 Anfrage ohne Hilfe abschließen, ReqMOB-N110 Schneller Neustart ohne Datenverlust | US2, UC-02, UC-03 | Sofort |
| FE-3 | Terminbuchung | Diagnose- und Reparaturtermin bei einem bewerteten Helfer buchen. | F-030 Diagnosetermin buchen, F-060 Reparaturtermin buchen | ReqMOB-N030 Antwortzeit Helfervorschläge, ReqMOB-N020 Anfrage ohne Hilfe abschließen | US3, US4, UC-04, UC-05, UC-06 | Sofort |
| FE-4 | Diagnose und Ersatzteilempfehlung | Helfer erfasst Diagnose und Ersatzteil, die Hilfesuchende sieht die Empfehlung in der App. | F-040 Ersatzteil empfehlen, F-050 Ersatzteilempfehlung einsehen |  | US4, US6, UC-02, UC-08 | Sofort |
| FE-5 | Anfragensteuerung | Leitung weist Anfragen zu, Helfer filtern Anfragen nach Fachgebiet. | F-070 Anfragen filtern, F-080 Anfrage zuweisen | ReqMOB-N050 Rollenbasierter Datenzugriff, ReqMOB-N130 Kurze Einarbeitung für Helfer | US5, US7, UC-10 | Sofort |
| FE-6 | Terminerinnerung | SMS-Erinnerung 24 Stunden vor dem Termin. | F-100 SMS-Erinnerung aktivieren | ReqMOB-N060 SMS-Erinnerung am Vortag | UC-07 | Nächstes |
| FE-7 | Helferprofile | Fähigkeiten aller Helfer digital statt auf einer handschriftlichen Liste pflegen. | F-110 Helferprofil pflegen |  | US8, UC-11 | Nächstes |
| FE-8 | Helfergewinnung | Registrierte Nutzer mit gesuchten Fähigkeiten finden und als Helfer einladen. | F-120 Neue Helfer einladen |  | US10, UC-13 | Später |
| FE-9 | Café-Planung und Auswertung | Café-Termine planen und Reparaturstatistiken für die Stadt exportieren. Funktionale Anforderungen werden noch abgeleitet. | noch offen | ReqMOB-N090 Nutzbar am Laptop und auf der Website | US9, UC-12 | Später |
| FE-10 | Ersatzteil-Shop mit Bezahlung | Ersatzteile direkt in der App kaufen und bezahlen. Bewusst ausgeschlossen: Sabine kauft das Teil selbst, Shop und Zahlung wären hoher Aufwand mit Haftungsfragen für ein Ehrenamtsprojekt. | keine |  | bewusst ausgeschlossen | Nie |
| ÜG | Übergreifend (Gesamtsystem) | Gilt für alle Features. |  | ReqMOB-N010 Große Schrift und Kontrast, ReqMOB-N040 DSGVO-konforme Datenhaltung, ReqMOB-N080 Automatisch getesteter Code, ReqMOB-N100 Hohe Verfügbarkeit | US1 bis US10 |  |

### Roadmap

**Sofort** (Erstes Release)

- **FE-1** Registrierung
- **FE-2** Reparaturanfrage stellen
- **FE-3** Terminbuchung
- **FE-4** Diagnose und Ersatzteilempfehlung
- **FE-5** Anfragensteuerung

**Nächstes** (Folgendes Release)

- **FE-6** Terminerinnerung
- **FE-7** Helferprofile

**Später** (Sinnvoll, geringe Priorität)

- **FE-8** Helfergewinnung
- **FE-9** Café-Planung und Auswertung

**Nie** (Bewusst nicht im Umfang)

- **FE-10** Ersatzteil-Shop mit Bezahlung

### Begründung: FE-3 Terminbuchung ist „Sofort“

**Nutzen für die Personas:** Die Buchung eines Diagnosetermins ist Sabines Kernziel aus dem Szenario. Ohne Termin bleibt die Anfrage folgenlos und die App bietet keinen Mehrwert. Jonas bekommt dadurch planbare Einsätze statt spontaner Anfragen.

**Abhängigkeiten:** FE-3 baut auf FE-1 Registrierung und FE-2 Reparaturanfrage auf. Gleichzeitig ist es Voraussetzung für FE-4 Diagnose und FE-6 Terminerinnerung, die ohne gebuchten Termin nicht funktionieren.

**Aufwand:** Mittel bis hoch. Kalender der Helfer, Schutz vor Doppelbuchung (AK-030-2) und die Antwortzeit aus N030 sind die aufwendigsten Teile. Der Aufwand lohnt sich, weil der gesamte Ablauf aus UC-02 daran hängt.
