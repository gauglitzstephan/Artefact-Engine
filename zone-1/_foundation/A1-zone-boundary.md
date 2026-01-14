# A1 – Zone‑1 Boundary Specification (V1)

# Bindungsraum der Artefakt‑Value‑Engine

> Zweck dieses Dokuments
> 
> 
> Diese Spec definiert **klar und operativ**, was in **Zone 1** gehört – und was **niemals**.
> 
> Sie ist die Grundlage für Stabilität, Auditierbarkeit und mentale Entlastung.
> 
> **Regel:** Alles, was hier definiert ist, gilt **ohne Ausnahme**, solange diese Spec nicht formal geändert wird.
> 

---

## 1) Zonenmodell (Überblick)

### Zone 1 – **Bindung & Autorität**

- formale Entscheidungen
- gültige Regeln
- veröffentlichte Artefakte
- auditierbare Versionen

### Zone 2 – **Workbench / WIP**

- Entwürfe
- Reviews
- Zwischenstände
- strukturierte Arbeit

### Zone 3 – **Exploration / Denken**

- Ideen
- Skizzen
- Hypothesen
- ungebundene Gedanken

> Grundregel:
> 
> 
> Kein Objekt darf gleichzeitig in mehr als **einer Zone** existieren.
> 

---

## 2) Zone 1 – Was gehört hinein (In‑Scope)

### 2.1 Artefakt‑Typen (verbindlich)

Zone 1 enthält **ausschließlich** Artefakte mit **bindender Wirkung**:

- Governance Core Kits
- Policies (Text + Policy‑as‑Code)
- Standards & Regelwerke
- Review‑ & Decision‑Frameworks
- Audit‑ & Evidence‑Packs
- Incident‑ & Exception‑Runbooks
- Maturity‑Modelle (freigegeben)
- Release Notes & Change Logs
- formale Entscheidungen (Accept / Reject / Deprecate)

---

### 2.2 Pflicht‑Metadaten für jedes Zone‑1‑Artefakt

Jedes Artefakt **muss** folgende Informationen enthalten:

1. **Artefakt‑ID** (eindeutig)
2. **Artefakt‑Typ**
3. **Version** (SemVer oder äquivalent)
4. **Status** (Frozen / Deprecated)
5. **Scope** (Geltungsbereich)
6. **Owner‑Rolle** (keine Personennamen)
7. **Legitimitätsquelle** (Regulatorik, Standard, Mandat etc.)
8. **Decision / Binding‑Logik** (was wird gebunden?)
9. **Evidence‑Links** (Begründung, Nachweise)
10. **Change‑Mechanik** (wie änderbar?)

> Fehlt eines dieser Felder → Artefakt darf nicht in Zone 1 liegen.
> 

---

## 3) Zone 1 – Was **niemals** hinein darf (Out‑of‑Scope)

### Verboten in Zone 1

- Rohideen oder Skizzen
- persönliche Notizen
- explorative Gedanken
- unfertige Entwürfe
- offene Fragen
- TODO‑Listen
- Brainstormings
- Diskussionen ohne Entscheidung
- Tool‑Experimente
- Pro/Contra‑Abwägungen ohne Binding

> Merksatz:
> 
> 
> *Wenn etwas noch gedacht, diskutiert oder ausprobiert wird – gehört es nicht in Zone 1.*
> 

---

## 4) Übergangsregeln zwischen den Zonen

### 4.1 Zone 3 → Zone 2 (Exploration → Arbeit)

Erlaubt, wenn:

- ein Gedanke strukturiert wird
- ein Artefakt‑Entwurf entsteht
- ein Review vorbereitet wird

**Kein formaler Prozess nötig.**

---

### 4.2 Zone 2 → Zone 1 (WIP → Bindung)

**Nur erlaubt über formalen Prozess:**

Pflicht:

- vollständige Metadaten
- Review abgeschlossen
- Entscheidung explizit dokumentiert
- Release‑Version vergeben
- Freeze erklärt

> Ohne Release & Freeze kein Zone‑1‑Eintrag.
> 

---

### 4.3 Zone 1 → Zone 2 (Change / Revision)

Nur über **Change Request**:

- Änderungsgrund
- Impact‑Einschätzung
- betroffene Artefakte
- Entscheidung (Approve / Reject)

Bis zur Freigabe bleibt die alte Version **gültig**.

---

## 5) Psychologischer Schutz (wichtig)

Diese Zonierung ist **kein Bürokratie‑Instrument**, sondern ein **mentaler Schutzmechanismus**:

- Zone 1 = Ruhe, Klarheit, Verlässlichkeit
- Zone 2 = Fokus, Arbeit, Qualität
- Zone 3 = Freiheit, Spiel, Denken

> Probleme entstehen fast immer durch Vermischung der Zonen.
> 

---

## 6) Minimal‑Check zur Selbstkontrolle

Bei jedem Objekt stelle dir **eine** Frage:

> „Hat dieses Objekt das Recht, Verhalten zu binden?“
> 
- Ja → Zone 1
- Vielleicht / noch nicht → Zone 2
- Nein → Zone 3

---

## 7) Gültigkeit & Änderung dieser Spec

- Diese Spec gilt ab **sofort**.
- Änderungen nur über formalen Change‑Prozess.
- Jede Lockerung der Regeln muss explizit begründet werden.

---

> Zone 1 ist kein Wissensspeicher.Zone 1 ist ein Ort der Verantwortung.
>
