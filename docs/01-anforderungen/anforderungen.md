# Anforderungen – Repair-Café-App

Dieses Dokument enthält die Aufgaben 1 bis 4: funktionale Anforderungen, nicht-funktionale Anforderungen, Akzeptanzkriterien sowie Features und Roadmap.

Das Use-Case-Diagramm (Aufgabe 6) und der strukturierte Anwendungsfall (Aufgabe 7) stehen in `use-case-diagramm.md`.

## Inhalt

1. [Funktionale Anforderungen](#1-funktionale-anforderungen)
2. [Nicht-funktionale Anforderungen](#2-nicht-funktionale-anforderungen)
3. [Akzeptanzkriterien](#3-akzeptanzkriterien)
4. [Features und Roadmap](#4-features-und-roadmap)

---

## 1. Funktionale Anforderungen

**Schema:** Nach [Bedingung] muss das System [Akteur] die Möglichkeit bieten, [Funktion] auszuführen.
Abgeleitet aus User Stories (US1 bis US10), dem Anwendungsfalldiagramm und UC-02.

Alle Anforderungen haben die Version 1 und den Status „Entwurf".

| ID | Feature | Priorität | Anforderungsname | Beschreibung | Quelle |
|---|---|---|---|---|---|
| F-010 | Registrierung | Muss | Kurzregistrierung | Nach dem ersten Öffnen der App muss das System neuen Hilfesuchenden die Möglichkeit bieten, sich nur mit Name, Telefonnummer und/oder E-Mail-Adresse zu registrieren. | US1, UC-01 |
| F-020 | Reparaturanfrage | Muss | Defekt auswählen | Nach Auswahl der Gerätekategorie muss das System angemeldeten Hilfesuchenden die Möglichkeit bieten, den Defekt aus einer Liste typischer Fehlerbilder auszuwählen. | US2, UC-03 |
| F-030 | Terminbuchung | Muss | Diagnosetermin buchen | Nach Absenden einer Reparaturanfrage muss das System angemeldeten Hilfesuchenden die Möglichkeit bieten, einen vorgeschlagenen Helfer mit Bewertung auszuwählen und bei ihm einen freien Diagnosetermin zu buchen. | US3, UC-04, UC-05 |
| F-040 | Diagnose | Muss | Ersatzteil empfehlen | Nach Durchführung eines Diagnosetermins muss das System Helfern die Möglichkeit bieten, die Diagnose und eine Ersatzteilempfehlung mit optionalem Richtpreis zu erfassen. | US6, UC-08 |
| F-050 | Diagnose | Muss | Ersatzteilempfehlung einsehen | Nach Speichern einer Ersatzteilempfehlung durch den Helfer muss das System der Hilfesuchenden die Möglichkeit bieten, die Empfehlung in der App einzusehen. | US4, UC-02 |
| F-060 | Terminbuchung | Muss | Reparaturtermin buchen | Nach Markieren von „Ersatzteil vorhanden" muss das System Hilfesuchenden die Möglichkeit bieten, einen freien Reparaturtermin beim selben Helfer zu buchen. | US4, UC-06 |
| F-070 | Anfragenübersicht | Muss | Anfragen filtern | Nach Anmeldung als Helfer muss das System Helfern die Möglichkeit bieten, offene Anfragen nach Fachgebiet zu filtern und die zugehörigen Fotos anzusehen. | US5 |
| F-080 | Verwaltung | Muss | Anfrage zuweisen | Nach Eingang einer neuen Reparaturanfrage muss das System dem technischen Leiter die Möglichkeit bieten, die Anfrage zu prüfen und einem passenden Helfer zuzuweisen. | US7, UC-10 |
| F-090 | Reparaturanfrage | Soll | Typenschild-Foto hochladen | Nach Auswahl des Defekts muss das System angemeldeten Hilfesuchenden die Möglichkeit bieten, ein Foto des Typenschilds hochzuladen oder diesen Schritt zu überspringen. | US2, UC-03 |
| F-100 | Benachrichtigung | Soll | SMS-Erinnerung aktivieren | Nach Buchung eines Diagnose- oder Reparaturtermins muss das System Hilfesuchenden die Möglichkeit bieten, eine SMS-Erinnerung 24 Stunden vor dem Termin zu aktivieren. | UC-07 |
| F-110 | Verwaltung | Soll | Helferprofil pflegen | Nach Anmeldung als technischer Leiter muss das System dem technischen Leiter die Möglichkeit bieten, die Fähigkeiten jedes Helfers in dessen Profil anzulegen und zu bearbeiten. | US8, UC-11 |
| F-120 | Helfergewinnung | Kann | Neue Helfer einladen | Nach Eingabe einer gesuchten Fähigkeit muss das System der Mitgründerin die Möglichkeit bieten, registrierte Nutzer mit dieser Fähigkeit zu finden und als Helfer einzuladen. | US10, UC-13 |

---

## 2. Nicht-funktionale Anforderungen

Messbare Qualitätsziele mit Prüfbedingung. Der Geltungsbereich „Gesamtsystem" gilt für alle Features, sonst nur für die genannten Features aus Aufgabe 1.

Alle Anforderungen haben die Version 1.

### ReqMOB-N010 Große Schrift und Kontrast
- **Priorität:** Muss
- **Qualitätsmerkmal:** Barrierefreiheit (Eigenschaft: Benutzerfreundlichkeit)
- **Quelle:** US1, US2, UC-01, UC-02
- **Geltungsbereich:** Gesamtsystem (App für Hilfesuchende)
- **Beschreibung:** Alle Bildschirme müssen bei einer Systemschriftgröße von 200 % ohne abgeschnittene Inhalte lesbar sein und einen Textkontrast von mindestens 4,5:1 (WCAG 2.1 AA) einhalten. Prüfung mit einem automatischen Barrierefreiheits-Tool und manuell auf je einem Android- und iOS-Gerät.
- **Metrik:** Kontrastverhältnis (x:1), Schriftskalierung ohne Abschneiden (%)
- **Zielwert:** ≥ 4,5:1 und 200 %

### ReqMOB-N020 Anfrage ohne Hilfe abschließen
- **Priorität:** Muss
- **Qualitätsmerkmal:** Benutzbarkeit (Eigenschaft: Benutzerfreundlichkeit)
- **Quelle:** US2, US3, UC-02, UC-05
- **Geltungsbereich:** Reparaturanfrage, Terminbuchung
- **Beschreibung:** In einem Usability-Test mit 5 Personen ab 65 Jahren ohne Vorerfahrung mit der App müssen mindestens 4 Personen eine Reparaturanfrage inklusive Diagnosetermin ohne fremde Hilfe in höchstens 20 Minuten abschließen.
- **Metrik:** Bearbeitungszeit (Minuten), Erfolgsquote ohne Hilfe (Personen)
- **Zielwert:** ≤ 20 min, ≥ 4 von 5

### ReqMOB-N030 Antwortzeit Helfervorschläge
- **Priorität:** Kann
- **Qualitätsmerkmal:** Performance (Eigenschaft: Geschwindigkeit)
- **Quelle:** US3, UC-04
- **Geltungsbereich:** Terminbuchung
- **Beschreibung:** Bei 200 gleichzeitig aktiven Nutzern müssen mindestens 95 % der Helfervorschläge innerhalb von 2 Sekunden angezeigt werden. Prüfung per Lasttest mit simulierter 4G-Verbindung.
- **Metrik:** Antwortzeit auf Benutzereingabe (Sekunden, 95. Perzentil), ausgeführte Transaktionen/Sekunde
- **Zielwert:** ≤ 2 s bei 200 gleichzeitigen Nutzern

### ReqMOB-N040 DSGVO-konforme Datenhaltung
- **Priorität:** Muss
- **Qualitätsmerkmal:** Datenschutz (Eigenschaft: Datenschutz)
- **Quelle:** US1, UC-01
- **Geltungsbereich:** Gesamtsystem
- **Beschreibung:** Personenbezogene Daten (Name, Telefonnummer, Postleitzahl, Fotos) müssen ausschließlich auf Servern in der EU gespeichert werden. Auf Löschanfrage müssen alle Daten einer Person innerhalb von 30 Tagen vollständig gelöscht sein. Prüfung durch ein Datenschutz-Audit vor dem Release.
- **Metrik:** Anteil Daten auf EU-Servern (%), Dauer bis vollständige Löschung (Tage)
- **Zielwert:** 100 %, ≤ 30 Tage

### ReqMOB-N050 Rollenbasierter Datenzugriff
- **Priorität:** Muss
- **Qualitätsmerkmal:** Sicherheit (Eigenschaft: Sicherheit)
- **Quelle:** US5, US7, UC-10
- **Geltungsbereich:** Anfragenübersicht, Verwaltung
- **Beschreibung:** Die Telefonnummer einer Hilfesuchenden darf nur für den zugewiesenen Helfer und den technischen Leiter sichtbar sein. Prüfung durch Rollentests mit allen vier Rollen; in 100 % der Testfälle darf keine unberechtigte Rolle die Nummer sehen.
- **Metrik:** Quote unberechtigter Zugriffe in Rollentests (%)
- **Zielwert:** 0 %

### ReqMOB-N060 SMS-Erinnerung am Vortag
- **Priorität:** Kann
- **Qualitätsmerkmal:** Zuverlässigkeit (Eigenschaft: Zuverlässigkeit)
- **Quelle:** UC-07
- **Geltungsbereich:** Benachrichtigung
- **Beschreibung:** Jede Person mit gebuchtem Termin erhält am Tag vor dem Termin eine SMS-Erinnerung. Mindestens 99 % der Erinnerungen müssen höchstens 10 Minuten nach dem geplanten Versandzeitpunkt zugestellt sein. Messung über einen Monat anhand des Zustellprotokolls des SMS-Dienstes.
- **Metrik:** Quote für das Auftreten von Fehlern (nicht rechtzeitig zugestellte SMS, %)
- **Zielwert:** ≤ 1 % pro Monat

### ReqMOB-N080 Automatisch getesteter Code
- **Priorität:** Soll
- **Qualitätsmerkmal:** Wartbarkeit (Eigenschaft: Wartbarkeit)
- **Quelle:** US1 bis US10
- **Geltungsbereich:** Gesamtsystem
- **Beschreibung:** Mindestens 80 % des Backend-Codes sind durch automatische Tests abgedeckt. Die Tests laufen bei jeder Änderung automatisch mit.
- **Metrik:** Testabdeckung Backend-Code (%)
- **Zielwert:** ≥ 80 %

### ReqMOB-N090 Nutzbar am Laptop und auf der Website
- **Priorität:** Muss
- **Qualitätsmerkmal:** Benutzbarkeit (Eigenschaft: Portierbarkeit)
- **Quelle:** US9, US10, UC-12, UC-13
- **Geltungsbereich:** Gesamtsystem (Website und Laptop)
- **Beschreibung:** Die App muss auch als Website im Browser am Laptop vollständig nutzbar sein. Alle Funktionen müssen in den aktuellen Versionen von Chrome, Firefox, Edge und Safari ab einer Auflösung von 1366 × 768 Pixeln funktionieren. Prüfung durch Browsertests auf allen vier Browsern.
- **Metrik:** Anzahl der Zielsysteme (Browser), Anteil plattformabhängiger Anweisungen (%)
- **Zielwert:** 4 Browser, ≤ 5 % plattformabhängiger Code

### ReqMOB-N100 Hohe Verfügbarkeit
- **Priorität:** Soll
- **Qualitätsmerkmal:** Zuverlässigkeit (Eigenschaft: Verfügbarkeit)
- **Quelle:** US3, UC-05, UC-06
- **Geltungsbereich:** Gesamtsystem
- **Beschreibung:** Die App muss im Monatsmittel zu mindestens 99,5 % erreichbar sein; die durchschnittliche Zeit bis zu einer Fehlfunktion beträgt mindestens 30 Tage. Messung über ein Monitoring-Tool.
- **Metrik:** Wahrscheinlichkeit der Nichtverfügbarkeit (%), durchschnittliche Zeit bis zu einer Fehlfunktion (Tage)
- **Zielwert:** ≤ 0,5 %, MTTF ≥ 30 Tage

### ReqMOB-N110 Schneller Neustart ohne Datenverlust
- **Priorität:** Soll
- **Qualitätsmerkmal:** Zuverlässigkeit (Eigenschaft: Stabilität)
- **Quelle:** US2, UC-02
- **Geltungsbereich:** Reparaturanfrage, Terminbuchung
- **Beschreibung:** Nach einer Fehlfunktion ist das System innerhalb von 15 Minuten wieder verfügbar. Bereits abgeschickte Anfragen und Termine gehen dabei nicht verloren. Prüfung durch einen simulierten Serverausfall.
- **Metrik:** Zeit bis zum Neustart (Minuten), Wahrscheinlichkeit für Datenzerstörung bei Fehlfunktion (%)
- **Zielwert:** ≤ 15 min, 0 %

### ReqMOB-N120 Kleine App-Größe
- **Priorität:** Kann
- **Qualitätsmerkmal:** Performance (Eigenschaft: Größe)
- **Quelle:** US1, UC-01
- **Geltungsbereich:** App für Hilfesuchende
- **Beschreibung:** Die App darf auf dem Smartphone höchstens 50 MB Speicher belegen, damit sie auch auf älteren Geräten installiert werden kann. Prüfung über die Installationsgröße im App-Store-Build.
- **Metrik:** Speicherbedarf (Megabyte)
- **Zielwert:** ≤ 50 MB

### ReqMOB-N130 Kurze Einarbeitung für Helfer
- **Priorität:** Soll
- **Qualitätsmerkmal:** Benutzbarkeit (Eigenschaft: Benutzerfreundlichkeit)
- **Quelle:** US5, US7, UC-08, UC-10
- **Geltungsbereich:** Helfer- und Verwaltungsbereich
- **Beschreibung:** Neue ehrenamtliche Helfer können nach einer Einführung von höchstens 30 Minuten Anfragen annehmen und Termine bestätigen. Die Hilfe umfasst höchstens 10 Seiten. Prüfung mit 3 neuen Helfern.
- **Metrik:** Schulungsdauer (Minuten), Anzahl der Hilfeseiten
- **Zielwert:** ≤ 30 min, ≤ 10 Seiten

### Übersicht

| ID | Name | Qualitätsmerkmal | Priorität | Zielwert |
|---|---|---|---|---|
| ReqMOB-N010 | Große Schrift und Kontrast | Barrierefreiheit | Muss | ≥ 4,5:1 und 200 % |
| ReqMOB-N020 | Anfrage ohne Hilfe abschließen | Benutzbarkeit | Muss | ≤ 20 min, ≥ 4 von 5 |
| ReqMOB-N030 | Antwortzeit Helfervorschläge | Performance | Kann | ≤ 2 s bei 200 Nutzern |
| ReqMOB-N040 | DSGVO-konforme Datenhaltung | Datenschutz | Muss | 100 %, ≤ 30 Tage |
| ReqMOB-N050 | Rollenbasierter Datenzugriff | Sicherheit | Muss | 0 % |
| ReqMOB-N060 | SMS-Erinnerung am Vortag | Zuverlässigkeit | Kann | ≤ 1 % pro Monat |
| ReqMOB-N080 | Automatisch getesteter Code | Wartbarkeit | Soll | ≥ 80 % |
| ReqMOB-N090 | Nutzbar am Laptop und auf der Website | Benutzbarkeit | Muss | 4 Browser, ≤ 5 % |
| ReqMOB-N100 | Hohe Verfügbarkeit | Zuverlässigkeit | Soll | ≤ 0,5 %, MTTF ≥ 30 Tage |
| ReqMOB-N110 | Schneller Neustart ohne Datenverlust | Zuverlässigkeit | Soll | ≤ 15 min, 0 % |
| ReqMOB-N120 | Kleine App-Größe | Performance | Kann | ≤ 50 MB |
| ReqMOB-N130 | Kurze Einarbeitung für Helfer | Benutzbarkeit | Soll | ≤ 30 min, ≤ 10 Seiten |

> Hinweis: Im Board gibt es keine Anforderung ReqMOB-N070. Die Nummerierung springt von N060 auf N080.

---

## 3. Akzeptanzkriterien

Drei funktionale Anforderungen (F-010, F-030, F-100) und zwei nicht-funktionale Anforderungen (N-020, N-030) mit je drei bis vier prüfbaren Kriterien: Erfolgsfall, Fehlerfall oder alternativer Ablauf, Messkriterium und Testbedingung.

### F-010 Kurzregistrierung

#### AK-010-1 (funktional)
- **Ausformuliert:** Als Hilfesuchende möchte ich mich nur mit Name und Telefonnummer registrieren können, damit ich die App ohne lange Formulare sofort nutzen kann.
- **Akzeptanzkriterium:**
  - **Gegeben:** Die App wird zum ersten Mal geöffnet.
  - **Wenn:** Name „Sabine Müller" und Telefonnummer „0171 1234567" eingegeben und „Registrieren" getippt werden.
  - **Dann:** Das Konto wird angelegt und die Startseite erscheint innerhalb von 3 Sekunden, ohne weitere Pflichtfelder.
- **Testbedingung:** Manueller Test auf je einem Android- und iOS-Gerät mit neuen Testdaten.

#### AK-010-2 (funktional)
- **Ausformuliert:** Als Hilfesuchende möchte ich mich alternativ mit meiner E-Mail-Adresse registrieren können, damit ich meine Telefonnummer nicht angeben muss.
- **Akzeptanzkriterium:**
  - **Wenn:** Nur Name und E-Mail-Adresse ohne Telefonnummer angegeben werden.
  - **Dann:** Die Registrierung ist erfolgreich und eine Bestätigungs-E-Mail kommt innerhalb von 60 Sekunden an.
- **Testbedingung:** Test-Postfach, Zeitmessung ab Tippen auf „Registrieren".

#### AK-010-3 (funktional, Fehlerfall)
- **Ausformuliert:** Als Hilfesuchende möchte ich bei fehlenden oder ungültigen Kontaktdaten sofort einen klaren Hinweis sehen, damit ich meinen Fehler direkt korrigieren kann.
- **Akzeptanzkriterium:**
  - **Wenn:** Weder Telefonnummer noch E-Mail angegeben werden oder die Telefonnummer weniger als 6 Ziffern hat.
  - **Dann:** Es erscheint der Hinweis „Bitte gültige Telefonnummer oder E-Mail angeben" direkt am Feld, und es wird kein Konto angelegt.
- **Testbedingung:** Testfälle mit leerem Feld, „123" und „abc@".

#### AK-010-4 (funktional, Fehlerfall)
- **Ausformuliert:** Als Hilfesuchende möchte ich erfahren, wenn meine Nummer schon registriert ist, damit ich mich einfach anmelden kann und kein zweites Konto entsteht.
- **Akzeptanzkriterium:**
  - **Wenn:** Die Telefonnummer ist schon registriert.
  - **Dann:** Die App zeigt „Diese Nummer ist bereits registriert" mit einem Link zur Anmeldung. Es entsteht kein doppeltes Konto.
- **Testbedingung:** Vorab angelegtes Testkonto, Prüfung in der Datenbank.

### F-030 Diagnosetermin buchen

#### AK-030-1 (funktional, Erfolgsfall)
- **Ausformuliert:** Als Hilfesuchende möchte ich einen bewerteten Helfer und einen freien Termin wählen und eine Bestätigung erhalten, damit ich sicher weiß, wann mein Gerät angeschaut wird.
- **Akzeptanzkriterium:**
  - **Gegeben:** Eine Anfrage „Toaster heizt nicht" ist abgeschickt.
  - **Wenn:** Die Hilfesuchende einen vorgeschlagenen Helfer (mit Sternebewertung) und einen freien Termin wählt und bestätigt.
  - **Dann:** Der Termin ist gebucht, die Bestätigung erscheint in der App und kommt innerhalb von 60 Sekunden per SMS oder E-Mail. Der Termin steht im Kalender des Helfers.
- **Testbedingung:** Testumgebung mit 3 Helfern und je 5 freien Terminen.

#### AK-030-2 (funktional, Fehlerfall)
- **Ausformuliert:** Als Hilfesuchende möchte ich informiert werden, wenn mein gewählter Termin inzwischen vergeben ist, damit ich direkt einen anderen freien Termin wählen kann.
- **Akzeptanzkriterium:**
  - **Wenn:** Der gewählte Termin wurde gerade von einer anderen Person gebucht.
  - **Dann:** Die App meldet „Dieser Termin ist leider nicht mehr frei" und zeigt die aktualisierten Termine. Es gibt keine Doppelbuchung.
- **Testbedingung:** Zwei Testgeräte buchen gleichzeitig denselben Termin.

#### AK-030-3 (funktional, alternativer Ablauf)
- **Ausformuliert:** Als Hilfesuchende möchte ich, dass meine Anfrage auch ohne verfügbaren Helfer offen bleibt, damit jemand mein Gerät [Wortlaut im Board schwer lesbar] , sobald ein passender Helfer gefunden ist.
- **Akzeptanzkriterium:**
  - **Wenn:** Für die Gerätekategorie ist kein Helfer verfügbar.
  - **Dann:** Die App zeigt „Wir suchen einen passenden Helfer für Sie", die Anfrage bleibt offen und der technische Leiter wird benachrichtigt (F-080).
- **Testbedingung:** Gerätekategorie ohne zugeordneten Helfer.

#### AK-030-4 (funktional, Fehlerfall)
- **Ausformuliert:** Als Hilfesuchende möchte ich bei einem Verbindungsabbruch meine Auswahl behalten und es erneut versuchen können, damit ich nicht alles neu eingeben muss.
- **Akzeptanzkriterium:**
  - **Wenn:** Die Internetverbindung beim Bestätigen abbricht.
  - **Dann:** Die Auswahl bleibt erhalten, die App bietet „Erneut versuchen" an, und es wird kein unvollständiger Termin gespeichert.
- **Testbedingung:** Flugmodus während der Buchung aktivieren.

### F-100 SMS-Erinnerung aktivieren

#### AK-100-1 (funktional, Erfolgsfall)
- **Ausformuliert:** Als Hilfesuchende möchte ich 24 Stunden vor meinem Termin eine SMS mit allen wichtigen Angaben bekommen, damit ich den Termin nicht vergesse.
- **Akzeptanzkriterium:**
  - **Gegeben:** Ein Termin am Donnerstag um 15:00 Uhr ist gebucht.
  - **Wenn:** Die SMS-Erinnerung aktiviert wird.
  - **Dann:** Am Mittwoch zwischen 15:00 und 15:10 Uhr kommt eine SMS mit Datum, Uhrzeit, Ort und Name des Helfers.
- **Testbedingung:** Testtermin mit Testnummer, Zustellprotokoll des SMS-Dienstes.

#### AK-100-2 (funktional, alternativer Ablauf)
- **Ausformuliert:** Als Hilfesuchende möchte ich sehen, warum bei kurzfristigen Terminen keine Erinnerung möglich ist, damit ich nicht vergeblich auf eine SMS warte.
- **Akzeptanzkriterium:**
  - **Wenn:** Der Termin liegt weniger als 24 Stunden in der Zukunft.
  - **Dann:** Die Option ist ausgegraut mit dem Hinweis „Erinnerung erst ab 24 Stunden vor Termin möglich".
- **Testbedingung:** Termin für den gleichen Tag buchen.

#### AK-100-3 (funktional, alternativer Ablauf)
- **Ausformuliert:** Als Hilfesuchende möchte ich, dass sich die Erinnerung automatisch an abgesagte oder verschobene Termine anpasst, damit ich keine falschen Infos erhalte.
- **Akzeptanzkriterium:**
  - **Wenn:** Der Termin nach Aktivierung abgesagt oder verschoben wird.
  - **Dann:** Für den alten Termin wird keine Erinnerung gesendet, beim verschobenen Termin gilt die Erinnerung für das neue Datum.
- **Testbedingung:** Termin nach Aktivierung absagen bzw. verschieben.

#### AK-100-4 (funktional, Fehlerfall)
- **Ausformuliert:** Als Hilfesuchende möchte ich, dass auch bei SMS-Problemen zuverlässig erinnert wird, notfalls per E-Mail, damit ich meinen Termin trotzdem wahrnehme.
- **Akzeptanzkriterium:**
  - **Wenn:** Die SMS nicht zugestellt werden kann.
  - **Dann:** Das System versucht es nach 5 und 15 Minuten erneut und schickt danach eine E-Mail, falls eine Adresse hinterlegt ist.
- **Testbedingung:** Ungültige Testnummer beim SMS-Dienst.

### N-020 Anfrage ohne Hilfe abschließen

#### AK-N020-1 (nicht-funktional, Messkriterium)
- **Ausformuliert:** Als ältere Nutzerin ohne App-Erfahrung möchte ich eine Reparaturanfrage samt Terminbuchung ganz allein abschließen können, damit ich niemanden um Hilfe bitten muss.
- **Akzeptanzkriterium:** Mindestens 4 von 5 Testpersonen schließen eine Reparaturanfrage inklusive Diagnosetermin ohne fremde Hilfe ab.
- **Testbedingung:** 5 Personen ab 65 Jahren, ohne Vorerfahrung, eigenes Smartphone, keine Einweisung.

#### AK-N020-2 (nicht-funktional, Messkriterium)
- **Ausformuliert:** Als ältere Nutzerin möchte ich meine Anfrage in wenigen Minuten erledigen, damit mich die App weder überfordert noch unnötig Zeit kostet.
- **Akzeptanzkriterium:** Die Testpersonen brauchen dafür durchschnittlich höchstens 5 Minuten, keine Person länger als 8 Minuten.
- **Testbedingung:** Stoppuhr vom Öffnen der App bis zur Buchungsbestätigung.

#### AK-N020-3 (nicht-funktional, Messkriterium)
- **Ausformuliert:** Als ältere Nutzerin möchte ich mich in der App [Wortlaut im Board schwer lesbar], damit ich mich bei der Bedienung sicher fühle.
- **Akzeptanzkriterium:** Pro Person treten durchschnittlich höchstens 2 Fehlbedienungen auf (z. B. falscher Button, Zurück-Navigation aus Versehen).
- **Testbedingung:** Beobachtungsprotokoll, Moderator greift nicht ein.

#### AK-N020-4 (nicht-funktional, Messkriterium)
- **Ausformuliert:** Als ältere Nutzerin möchte ich nach der Buchung genau wissen, wann und wo mein Termin ist, damit ich pünktlich am richtigen Ort bin.
- **Akzeptanzkriterium:** Alle Testpersonen können nach dem Test Datum, Uhrzeit und Ort ihres gebuchten Termins richtig nennen.
- **Testbedingung:** Kurzinterview direkt nach dem Test.

### N-030 Antwortzeit Helfervorschläge

#### AK-N030-1 (nicht-funktional, Messkriterium)
- **Ausformuliert:** Als Hilfesuchende möchte ich passende Helfervorschläge innerhalb von 2 Sekunden sehen, damit ich nicht ungeduldig werde und abbreche.
- **Akzeptanzkriterium:** Bei 200 gleichzeitig aktiven Nutzern werden 95 % der Helfervorschläge innerhalb von 2 Sekunden und 99 % innerhalb von 4 Sekunden angezeigt.
- **Testbedingung:** Lasttest über 30 Minuten, simulierte 4G-Verbindung (100 ms Latenz), 500 Helfer in der Testdatenbank.

#### AK-N030-2 (nicht-funktional, Fehlerfall)
- **Ausformuliert:** Als Hilfesuchende möchte ich bei längerer Wartezeit sehen, dass die App arbeitet, und ohne Datenverlust erneut suchen können, damit ich nicht im Unklaren bleibe.
- **Akzeptanzkriterium:**
  - **Wenn:** Die Antwort länger als 1 Sekunde dauert.
  - **Dann:** Eine Ladeanzeige erscheint. Nach 15 Sekunden ohne Antwort zeigt die App „Bitte erneut versuchen", die Eingaben bleiben erhalten.
- **Testbedingung:** Künstliche Serververzögerung von 20 Sekunden.

#### AK-N030-3 (nicht-funktional, Stresstest)
- **Ausformuliert:** Als Hilfesuchende möchte ich, dass die App auch bei großem Andrang, etwa kurz vor einem Repair-Café, schnell bleibt, damit ich jederzeit buchen kann.
- **Akzeptanzkriterium:** Das System skaliert bis 1.000 gleichzeitige Nutzer linear: Die Antwortzeit im 95. Perzentil steigt höchstens auf 4 Sekunden, die Fehlerquote bleibt unter 1 %.
- **Testbedingung:** Stufenweiser Lasttest mit 200, 500 und 1.000 Nutzern.

---

## 4. Features und Roadmap

Zusammengehörige Anforderungen aus Aufgabe 1 und 2 sind zu Features gebündelt. Nicht-funktionale Anforderungen sind dem betroffenen Feature zugeordnet oder als übergreifend (ÜG) gekennzeichnet.

### Feature-Tabelle

| Nr. | Feature | Beschreibung | Funktionale Anforderungen | Nicht-funktionale Anforderungen | Quelle | Roadmap |
|---|---|---|---|---|---|---|
| FE-1 | Registrierung | Schneller Einstieg in die App ohne lange Formulare. | F-010 Kurzregistrierung | ReqMOB-N120 Kleine App-Größe | US1, UC-01 | Sofort |
| FE-2 | Reparaturanfrage stellen | Defekt ohne Fachbegriffe beschreiben, optional mit Foto des Typenschilds. | F-020 Defekt auswählen, F-090 Typenschild-Foto hochladen | ReqMOB-N020 Anfrage ohne Hilfe abschließen, ReqMOB-N110 Schneller Neustart ohne Datenverlust | US2, UC-02, UC-03 | Sofort |
| FE-3 | Terminbuchung | Diagnose- und Reparaturtermin bei einem bewerteten Helfer buchen. | F-030 Diagnosetermin buchen, F-060 Reparaturtermin buchen | ReqMOB-N030 Antwortzeit Helfervorschläge, ReqMOB-N020 Anfrage ohne Hilfe abschließen | US3, US4, UC-04, UC-05, UC-06 | Sofort |
| FE-4 | Diagnose und Ersatzteilempfehlung | Helfer erfasst Diagnose und Ersatzteil, die Hilfesuchende sieht die Empfehlung in der App. | F-040 Ersatzteil empfehlen, F-050 Ersatzteilempfehlung einsehen | – | US4, US6, UC-02, UC-08 | Sofort |
| FE-5 | Anfragensteuerung | Leitung weist Anfragen zu, Helfer filtern Anfragen nach Fachgebiet. | F-070 Anfragen filtern, F-080 Anfrage zuweisen | ReqMOB-N050 Rollenbasierter Datenzugriff, ReqMOB-N130 Kurze Einarbeitung für Helfer | US5, US7, UC-10 | Sofort |
| FE-6 | Terminerinnerung | SMS-Erinnerung 24 Stunden vor dem Termin. | F-100 SMS-Erinnerung aktivieren | ReqMOB-N060 SMS-Erinnerung am Vortag | UC-07 | Nächstes |
| FE-7 | Helferprofile | Fähigkeiten aller Helfer digital statt auf einer handschriftlichen Liste pflegen. | F-110 Helferprofil pflegen | – | US8, UC-11 | Nächstes |
| FE-8 | Helfergewinnung | Registrierte Nutzer mit gesuchten Fähigkeiten finden und als Helfer einladen. | F-120 Neue Helfer einladen | – | US10, UC-13 | Später |
| FE-9 | Café-Planung | Café-Termine planen. | noch offen | ReqMOB-N090 Nutzbar am Laptop und auf der Website | US9, UC-12 | Später |
| FE-10 | Ersatzteil-Shop mit Bezahlung | Ersatzteile direkt in der App kaufen und bezahlen. Bewusst ausgeschlossen: Sabine kauft das Teil selbst, Shop und Zahlung wären hoher Aufwand mit Haftungsfragen für ein Ehrenamtsprojekt. | keine | – | bewusst ausgeschlossen | Nie |
| ÜG | Übergreifend (Gesamtsystem) | Gilt für alle Features. | – | ReqMOB-N010 Große Schrift und Kontrast, ReqMOB-N040 DSGVO-konforme Datenhaltung, ReqMOB-N080 Automatisch getesteter Code, ReqMOB-N100 Hohe Verfügbarkeit | US1 bis US10 | – |
| FE-11 | Bewertung nach Reparatur | Nach Abschluss der Reparatur bewertet die Hilfesuchende die Gesamtleistung der App und jedes genutzte Feature, z. B. mit Sternen und optionalem Kommentar. | noch offen | – | noch offen | Später |

### Roadmap

#### Sofort – Erstes Release

- **FE-1 Registrierung:** Ohne Nutzerkonto lassen sich Anfragen und Termine keiner Person zuordnen. Das ist die Grundlage für alle weiteren Features.
- **FE-2 Reparaturanfrage stellen:** Das ist der Einstiegspunkt in den Kernprozess und der eigentliche Zweck der Plattform. Ohne Anfragen gibt es nichts zu terminieren oder zu diagnostizieren.
- **FE-3 Terminbuchung:** Sie verbindet die Anfrage mit einem konkreten Café-Termin und macht den Ablauf erst vollständig. Ohne sie bleibt die Plattform ein reines Formular.
- **FE-4 Diagnose und Ersatzteilempfehlung:** Das ist vermutlich das Alleinstellungsmerkmal gegenüber einem normalen Terminkalender. Es spart den Helfern Zeit und erhöht die Erfolgschance einer Reparatur.
- **FE-5 Anfragensteuerung:** Das Café muss eingehende Anfragen sortieren, annehmen oder ablehnen können, sonst entsteht schon beim Start ein Engpass. Es ist die Gegenstelle zu FE-2 auf der Organisationsseite.

#### Nächstes – Folgendes Release

- **FE-6 Terminerinnerung:** Der Kernprozess funktioniert auch ohne sie, sie senkt aber No-Shows. Das lohnt sich erst, wenn reale Buchungen vorliegen und sich der Effekt messen lässt.
- **FE-7 Helferprofile:** Sie verbessern die Zuordnung von Anfrage zu passender Hilfe, brauchen aber eine gewisse Zahl aktiver Helfer, um Mehrwert zu liefern. Im ersten Release lässt sich das noch manuell lösen.

#### Später – Sinnvoll, geringe Priorität

- **FE-9 Café-Planung und Auswertung:** Eine Auswertung ist erst sinnvoll, wenn genug Daten aus dem laufenden Betrieb vorliegen. Davor wäre sie leer und der Aufwand nicht gerechtfertigt.
- **FE-11 Bewertung nach Reparatur:** Bewertungen setzen abgeschlossene Reparaturen voraus und sind ein Qualitätsfeature, kein Muss für den Start. Sie bringen erst mit wachsender Nutzung echten Wert.

> Hinweis: FE-8 Helfergewinnung ist in der Feature-Tabelle mit „Später" eingeordnet, hat im Board aber keine eigene Karte in der Roadmap.

#### Nie – Bewusst nicht im Umfang

- **FE-10 Ersatzteil-Shop mit Bezahlung:** Zahlungsabwicklung, Haftung und Logistik machen aus der Vermittlungsplattform einen Händler und sprengen den Fokus. FE-4 empfiehlt Teile, verkaufen sollen sie andere.

### Begründung: FE-3 Terminbuchung ist „Sofort" (Core Function)

- **Nutzen für die Personas:** Die Buchung eines Diagnosetermins ist Sabines Kernziel aus dem Szenario. Ohne Termin bleibt die Anfrage folgenlos und die App bietet keinen Mehrwert. Jonas bekommt dadurch planbare Einsätze statt spontaner Anfragen.
- **Abhängigkeiten:** FE-3 baut auf FE-1 Registrierung und FE-2 Reparaturanfrage auf. Gleichzeitig ist es Voraussetzung für FE-4 Diagnose und FE-6 Terminerinnerung, die ohne gebuchten Termin nicht funktionieren.
- **Aufwand:** Mittel bis hoch. Kalender der Helfer, Schutz vor Doppelbuchung (AK-030-2) und die Antwortzeit aus N030 sind die aufwendigsten Teile, weil der gesamte Ablauf aus UC-02 daran hängt.
