# Requirements-Review – Repair-Café-App

**Datum:** 11.11.2026  
**Umfang:** Review der Zusammenhänge um Helferwahl/Zuweisung und Terminerinnerungen. Herangezogen wurden `anforderungen_fallstudie.md`, `user-stories.md`, `use-case-diagramm.md`, `personas.md` und `szenarien.md` in `docs/01-anforderungen/`.

## Erkenntnisse

### 1. Unterschiedliche SMS-Regelung

**Befund:** F-100 und AK-100-1 beschreiben eine aktivierbare Erinnerung; ReqMOB-N060 sagt, jede Person mit gebuchtem Termin erhalte eine SMS. UC-05/UC-06 binden UC-07 ein, und Sabines Szenario beschreibt SMS-Erinnerungen vor beiden Terminen. Damit ist nicht eindeutig, ob Erinnerungen von einer Aktivierung abhängen.

**Einordnung:** Widersprüchliche bzw. unterschiedlich konkrete Formulierungen. Das Team hat die Entscheidung zurückgestellt; welches Versandverhalten gilt, bleibt offen.

**Fundstellen:** `anforderungen_fallstudie.md` (F-100, ReqMOB-N060, AK-100-1); `use-case-diagramm.md` (UC-05 bis UC-07); `szenarien.md` (Abschnitt 3).

### 2. Helferwahl und Zuweisung

**Befund:** F-030 und UC-02s Hauptablauf lassen Sabine einen vorgeschlagenen Helfer auswählen; F-080 beschreibt eine Prüfung und Zuweisung durch den technischen Leiter. In UC-02 wird die Leitung im Ausnahmefall „kein passender Helfer“ informiert. US3 und Sabines Szenario zeigen die Auswahl durch Sabine.

**Klarstellung des Teams:** Die App schlägt Jonas vor; Martin prüft die Anfrage und weist sie Jonas zu. Sabine sieht, wer ihr hilft, und wählt anschließend einen von Jonas' freien Terminen. Damit sind Leitungszuweisung und Terminwahl im vorgesehenen Ablauf getrennte Schritte.

**Fundstellen:** `anforderungen_fallstudie.md` (F-030, F-080, AK-030-3); `user-stories.md` (US3, US7); `use-case-diagramm.md` (UC-02, Schritte 5 und 5e); `szenarien.md` (Interaktion, Helferauswahl).

### 3. Messkriterien für N-020

**Befund:** ReqMOB-N020 setzt höchstens 20 Minuten und mindestens 4 von 5 erfolgreichen Tests an. AK-N020-1 wiederholt die Erfolgsquote; AK-N020-2 ergänzt durchschnittlich höchstens 5 Minuten und höchstens 8 Minuten pro Person.

**Einordnung:** Mögliche Verbesserung: Das Verhältnis zwischen dem Zielwert der Anforderung und den strengeren Kriterien der Akzeptanztests ist nicht erläutert. Eine Teamentscheidung dazu liegt in diesem Review nicht vor.

**Fundstellen:** `anforderungen_fallstudie.md` (ReqMOB-N020, AK-N020-1, AK-N020-2).

## Klarstellungen und Änderungen

Das Team hat das Verhältnis von Helferwahl zu Zuweisung klargestellt. Die SMS-Regel wurde zurückgestellt und bleibt offen. Die Messkriterien für N-020 wurden nicht entschieden. Es wurden keine Requirements oder Akzeptanzkriterien geändert.
