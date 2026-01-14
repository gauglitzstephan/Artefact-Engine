# A4 – Change & Freeze Workflow (V1)

# Mechanische Bindung statt emotionaler Entscheidung

> Zweck dieses Dokuments
> 
> 
> Diese Spec definiert den **verbindlichen Prozess**, wie Artefakte
> 
> von Arbeit (Zone 2) zu Bindung (Zone 1) gelangen – und wie sie geändert werden.
> 
> Ziel ist es, **Entscheidungsdruck zu reduzieren**, Bindung zu objektivieren
> 
> und spätere Automatisierung vorzubereiten.
> 

---

## 1) Design-Prinzip

> Bindung ist ein Zustand, kein Gefühl.
> 

Der Workflow sorgt dafür, dass:

- niemand „aus dem Bauch heraus“ bindet
- niemand Bindung vermeidet, weil sie emotional schwer ist
- Änderungen **kontrolliert**, nicht diskutiert, stattfinden

---

## 2) Artefakt-Zustände (State Machine)

### Zustände

- **Draft** (Zone 2)
- **Review** (Zone 2)
- **Frozen** (Zone 1 – bindend)
- **Deprecated** (Zone 1 – historisch)

> Regel:
> 
> 
> Nur der Zustand **Frozen** hat bindende Wirkung.
> 

---

## 3) Freeze Workflow (Zone 2 → Zone 1)

### 3.1 Freeze Trigger

Ein Artefakt darf eingefroren werden, wenn:

- Scope klar definiert ist
- alle Pflicht-Metadaten (A2) vorhanden sind
- Review abgeschlossen ist
- offene Fragen explizit geschlossen **oder** bewusst ausgeschlossen sind

---

### 3.2 Freeze Checklist (verbindlich)

Vor jedem Freeze müssen folgende Fragen mit **Ja** beantwortet sein:

1. Ist der Geltungsbereich eindeutig?
2. Ist klar, **was nicht** geregelt wird?
3. Gibt es einen Owner (Rolle)?
4. Ist die Legitimitätsquelle benannt?
5. Sind Ausnahmen geregelt?
6. Ist klar, wie Änderungen erfolgen?
7. Ist die Version vergeben?

> Ein einziges „Nein“ → kein Freeze.
> 

---

### 3.3 Freeze Aktion

- Status → `Frozen`
- Version festlegen
- Registry-Eintrag aktualisieren
- Release Notes erstellen
- Artefakt in Zone 1 verschieben

---

## 4) Change Workflow (Zone 1 → Zone 2 → Zone 1)

### 4.1 Change Trigger

Änderungen dürfen **nur** angestoßen werden durch:

- neue regulatorische Anforderungen
- Incidents / Near Misses
- neue Use-Case-Klassen
- Ablauf eines Review-by-Datums

> „Wäre doch besser“ ist kein Change-Grund.
> 

---

### 4.2 Change Request (CR)

Jede Änderung startet mit einem **formalen CR**:

Pflichtfelder:

- Referenziertes Artefakt (ID)
- Änderungsgrund
- Impact-Einschätzung (Scope, Risiko)
- Dringlichkeit (Low/Medium/High)
- Vorschlag: Patch / Minor / Major

---

### 4.3 Change Evaluation

Bewertung entlang von:

- Economic Asymmetry
- Risiko-Reduktion
- Entscheidungsdichte
- Rückwärtskompatibilität

**Entscheidung:**

- Approve
- Defer
- Reject

---

### 4.4 Umsetzung

- Artefakt → Zone 2 (neue Version)
- Anpassungen durchführen
- Review
- neuer Freeze (siehe Abschnitt 3)

> Bis zum neuen Freeze bleibt die alte Version gültig.
> 

---

## 5) Deprecation Workflow

### 5.1 Deprecation Trigger

- Artefakt wird ersetzt
- Scope ist nicht mehr relevant
- Governance-Strategie ändert sich

---

### 5.2 Deprecation Aktion

- Status → `Deprecated`
- Begründung dokumentieren
- Nachfolge-Artefakt verlinken (falls vorhanden)
- Artefakt bleibt lesbar, aber nicht bindend

---

## 6) Review-by-Datum & Verfall

> Nichts ist für immer gültig.
> 

Jedes Frozen Artefakt benötigt:

- ein Review-by-Datum
- eine der drei Entscheidungen:
    - Re-Freeze
    - Change
    - Deprecate

---

## 7) Psychologischer Schutz (explizit)

Der Workflow ist absichtlich:

- mechanisch
- repetitiv
- unromantisch

> Er schützt vor Entscheidungsangst und Perfektionismus.
> 

---

## 8) Anti-Pattern (verboten)

- informelle Änderungen
- „nur kurz anpassen“
- parallele gültige Versionen
- Diskussion statt CR

---

## 9) Minimaler Funktionstest

Der Workflow funktioniert, wenn:

- du ein Artefakt einfrieren kannst, ohne neu zu diskutieren
- du Änderungen anstoßen kannst, ohne Schuldgefühl
- Stabilität der Normalfall ist

---

## 10) Gültigkeit & Änderung

- Diese Spec gilt ab sofort.
- Änderungen nur über formalen Change-Prozess.

---

> Freeze ist kein Stillstand.Freeze ist kontrollierte Verantwortung.
>
