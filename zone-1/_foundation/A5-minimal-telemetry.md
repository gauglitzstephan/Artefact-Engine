# A5 – Minimal-Telemetrie & Health Checks (V1)

# Sehen ohne Steuern · Messen ohne Optimierungszwang

> Zweck dieses Dokuments
> 
> 
> Diese Spec definiert eine **bewusst minimale Telemetrie**,
> 
> die frühzeitig Drift, Überlastung und Systemfehler sichtbar macht,
> 
> **ohne** Optimierungsdruck, KPI-Fatigue oder Mikromanagement zu erzeugen.
> 
> Telemetrie dient hier **der Stabilität**, nicht der Performance.
> 

---

## 1) Grundprinzipien (nicht verhandelbar)

1. **Telemetrie ≠ Optimierung**
2. **Jede Metrik braucht einen Zweck und ein Kill-Kriterium**
3. **Beobachten vor Eingreifen**
4. **Ausnahmen sind Signale, keine Fehler**
5. **Stabilität misst man über Zeit, nicht punktuell**

> Regel:
> 
> 
> Wenn eine Metrik keine Entscheidung auslösen *könnte*, wird sie nicht erhoben.
> 

---

## 2) Was Telemetrie hier leisten darf – und was nicht

### Darf

- schleichende Probleme sichtbar machen
- Übersteuerung verhindern
- blinde Flecken reduzieren
- Review-Zyklen informieren

### Darf nicht

- permanenten Verbesserungsdruck erzeugen
- Ranking oder Zielvereinbarungen treiben
- individuelle Leistung bewerten

---

## 3) Telemetrie-Domänen (vollständig, aber schlank)

Es gibt **genau vier** Telemetrie-Domänen:

1. **Stabilität**
2. **Bindung & Disziplin**
3. **Drift & Ausnahmen**
4. **Systemlast**

Keine weiteren Domänen ohne formalen Change.

---

## 4) Kernmetriken (Minimalset)

### 4.1 Stabilität

- **# Frozen Artefakte** (Trend, nicht Ziel)
- **Ø Zeit seit letztem Review**
- **# Deprecated Artefakte** (Trend)

**Signal:**

- viele alte Artefakte → möglicher Drift

---

### 4.2 Bindung & Disziplin

- **% Entscheidungen mit Artefakt-Bindung**
- **# informelle Änderungen (soll = 0)**
- **# parallele gültige Versionen (soll = 0)**

**Signal:**

- Anstieg → Regelbruch oder Überforderung

---

### 4.3 Drift & Ausnahmen

- **# Change Requests / Zeitraum**
- **# genehmigte Ausnahmen**
- **Ø Zeit bis Re-Freeze nach Change**

**Signal:**

- viele Ausnahmen → Regel zu streng oder falsch geschnitten

---

### 4.4 Systemlast

- **# parallele aktive Artefakte**
- **# offene Reviews**
- **# offene CRs**

**Signal:**

- Anstieg → Überlastung, nicht Ineffizienz

---

## 5) Kill-Kriterien (entscheidend)

Jede Metrik ist **temporär**.

Beispiele:

- Wenn eine Metrik **3 Review-Zyklen** keine neuen Erkenntnisse liefert → entfernen
- Wenn eine Metrik **nur Neugier befriedigt** → entfernen
- Wenn eine Metrik Verhalten verzerrt → entfernen

> Telemetrie darf sterben.
> 

---

## 6) Review-Rhythmus (bewusst langsam)

- **Kein Daily / Weekly Monitoring**
- Telemetrie-Review **nur**:
    - vor einem geplanten Review-Zyklus
    - nach Incidents
    - bei systemischem Unwohlsein

> Normalzustand ist Nicht-Beobachtung.
> 

---

## 7) Darstellung & Zugriff

- aggregiert
- trendbasiert
- kein Echtzeit-Dashboard

Formate:

- einfache Tabelle
- monatliche Snapshot-Notiz

---

## 8) Anti-Pattern (explizit verboten)

- Zielwerte („wir müssen unter X bleiben“)
- Optimierungs-OKRs
- Metriken ohne Besitzer
- Dashboards aus Neugier

---

## 9) Minimaler Health Check (Selbsttest)

Das System ist gesund, wenn:

- Stabilität der Default ist
- Änderungen selten und begründet sind
- Telemetrie *keinen* Handlungsdruck erzeugt

---

## 10) Gültigkeit & Änderung

- Diese Spec gilt ab sofort.
- Änderungen nur über formalen Change-Prozess.

---

> Telemetrie ist ein Frühwarnsystem.Kein Gaspedal.
>
