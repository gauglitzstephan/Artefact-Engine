# B-Block – Operating Model (V1)
## Betrieb der Artefakt-Value-Engine (Solo → Small Core Team)

> **Zweck dieses Dokuments**
> Dieses Operating Model definiert, **wie gearbeitet wird**, nicht was gebaut wird.
> Es übersetzt die Zone-1-Foundation (A-Block) in einen **tragfähigen, konfliktarmen
> und skalierbaren Betriebsmodus**.
>
> Fokus: **Klarheit, geringe soziale Reibung, Schutz der Denkqualität**.

---

## 1) Operating-Prinzipien (nicht verhandelbar)

1. **Artefakte führen – Menschen folgen**
2. **Asynchron ist der Default**
3. **Entscheidungen sind Rollen-, nicht Personen-gebunden**
4. **Wenige parallele Initiativen (WIP-Limit)**
5. **Stabilität ist Erfolg, nicht Stillstand**

---

## 2) Betriebsmodi (explizit getrennt)

### Mode A – Solo-Betrieb (Default)

Ziel:
- Aufbau & Pflege der Artefakt-Autorität
- maximale Unabhängigkeit
- minimale Koordination

Eigenschaften:
- eine entscheidende Rolle
- keine Meetings
- keine impliziten Stellvertretungen

---

### Mode B – Small Core Team (2–4 Personen, optional)

Ziel:
- Durchsatz erhöhen
- Review-Qualität sichern
- Domänenwissen gezielt einbinden

Eigenschaften:
- klar abgegrenzte Rollen
- keine Linienorganisation
- keine Projektlogik

> **Regel:**
> Mode B wird bewusst aktiviert – nie schleichend.

---

## 3) Rollenmodell (funktional, nicht hierarchisch)

### 3.1 Governance Architect (GA)

**Verantwortung:**
- Bindung & Release von Artefakten
- Entscheidung über Changes
- Schutz der Zone-1-Integrität

**Exklusive Rechte:**
- Freeze / Re-Freeze
- Deprecation

> Default: **du**

---

### 3.2 Controls / Specification Engineer (CE)

**Verantwortung:**
- Strukturierung von Policies & Standards
- Policy-as-Code / formale Logik
- Konsistenzprüfungen

**Keine Rechte:**
- kein Freeze
- keine Scope-Entscheidungen

---

### 3.3 Domain Reviewer (DR)

**Verantwortung:**
- fachliche Plausibilität
- Risiko- & Realitätschecks

**Charakter:**
- temporär
- austauschbar
- asynchron

---

### 3.4 Evidence & Release Ops (optional)

**Verantwortung:**
- Pflege von Evidence
- Release Notes
- Registry-Konsistenz

---

## 4) Entscheidungsrechte (Decision Matrix)

| Entscheidung | GA | CE | DR |
|---|---|---|---|
| Accept / Reject Scope | ✔ | ✖ | ✖ |
| Freeze / Release | ✔ | ✖ | ✖ |
| Change Approve | ✔ | ✖ | ✖ |
| Struktur-Vorschläge | ✖ | ✔ | ✔ |
| Review-Kommentare | ✖ | ✔ | ✔ |

> **Regel:**
> Feedback ohne Entscheidungsrecht ist erlaubt.
> Entscheidungen ohne Rolle sind es nicht.

---

## 5) Arbeitsfluss (End-to-End)

1. Signal / Bedarf erkannt (Engine 1)
2. Qualifikation (Engine 2)
3. Arbeit in Zone 2
4. Review (asynchron)
5. Entscheidung durch GA
6. Freeze → Zone 1
7. Telemetrie beobachtet

---

## 6) Kommunikationsregeln

- Default: schriftlich, artefaktbezogen
- Keine Entscheidungsfindung in Chats
- Diskussionen enden in:
  - Decision
  - Defer
  - Reject

> **Artefakte beenden Gespräche.**

---

## 7) WIP- & Belastungsgrenzen

- Max. **2 aktive Artefakte** gleichzeitig
- Max. **1 Major Change** zur selben Zeit
- Review-Zyklen nicht stapeln

> **Überlastung ist ein Systemfehler, kein Leistungsproblem.**

---

## 8) Meeting-Policy

- Keine Regelmeetings
- Sync nur für:
  - Konfliktklärung
  - kritische Release-Entscheidungen

> **Wenn ein Meeting nötig ist, ist vorher etwas unklar geblieben.**

---

## 9) Qualitätsabsicherung (leichtgewichtig)

- Review-Checkliste (pro Artefakt)
- Red-Flag-Liste (Owner fehlt, Scope unklar, keine Evidence)
- Stop-Ship bei Red Flags

---

## 10) Eskalation & Schutzmechanismen

- Unklare Verantwortung → Arbeit pausieren
- Regelbruch → Artefakt zurück in Zone 2
- Dauerhafte Ausnahmen → Regel hinterfragen

---

## 11) Gültigkeit & Weiterentwicklung

- Dieses Operating Model gilt ab sofort.
- Änderungen nur über formalen Change-Prozess.
- Solo-Modus ist der stabile Default.

---

> **Ein gutes Operating Model verhindert Probleme,
> bevor sie menschlich werden.**
