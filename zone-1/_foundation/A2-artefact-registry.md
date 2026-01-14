# A2 – Artefakt-Registry & Naming Specification (V1)

## Operative Grundlage für Zone‑1‑Autorität

> Zweck dieses Dokuments
> 
> 
> Diese Spec definiert die **zentrale Registry**, das **Naming-/ID-System**
> 
> und die **Minimal-Metadaten**, mit denen Zone‑1‑Artefakte eindeutig,
> 
> auditierbar und langfristig beherrschbar werden.
> 
> **Designziel:** maximale Klarheit bei minimalem Overhead.
> 

---

## 1) Rolle der Artefakt-Registry

Die Artefakt-Registry ist:

- **das Inhaltsverzeichnis von Zone 1**
- **die einzige Quelle der Wahrheit**, welche Artefakte bindend sind
- **kein Wissensspeicher**, sondern ein Kontroll- und Navigationsinstrument

> Regel:
> 
> 
> Existiert ein Artefakt nicht in der Registry,
> 
> existiert es **nicht** als bindendes Objekt.
> 

---

## 2) Grundprinzipien

1. **Eindeutigkeit vor Eleganz**
2. **Maschinen- & menschenlesbar**
3. **Stabil über Zeit** (keine Umbenennungen aus Stilgründen)
4. **IDs ändern sich nie** – nur Status & Version
5. **Registry ist flach**, Artefakte tragen die Komplexität

---

## 3) Artefakt-ID-Schema

### 3.1 Aufbau

`<DOMAIN>-<TYPE>-<SEQUENCE>`

**Beispiele:**

- `GOV-CORE-001`
- `GOV-POL-004`
- `GOV-PAC-002`
- `RES-BLUE-007`

### 3.2 Felder

- **DOMAIN** – übergeordneter Wertbereich
    - `GOV` – Governance
    - `RES` – Research
    - `STD` – Standards
    - (erweiterbar, aber selten)
- **TYPE** – Artefaktklasse
    - `CORE` – Core Kits
    - `POL` – Policies (Text)
    - `PAC` – Policy-as-Code
    - `CHK` – Checklisten / Reviews
    - `AUD` – Audit / Evidence
    - `RUN` – Runbooks
    - `MAT` – Maturity Modelle
- **SEQUENCE** – laufende Nummer (000–999)

> Regel:
> 
> 
> Semantik steckt im Artefakt – nicht in der ID.
> 

---

## 4) Versionslogik (SemVer-light)

### 4.1 Versionstypen

- **MAJOR (X.0.0)**
    - Scope-Änderung
    - Regelbruch
- **MINOR (0.Y.0)**
    - neue Regeln
    - erweiterter Geltungsbereich
- **PATCH (0.0.Z)**
    - Klarstellungen
    - Bugfixes in Logik

### 4.2 Status

- `Draft` (Zone 2)
- `Frozen` (Zone 1 – bindend)
- `Deprecated` (Zone 1 – historisch)

> Regel:
> 
> 
> Nur **Frozen** Artefakte haben bindende Wirkung.
> 

---

## 5) Pflicht-Metadaten (Registry-Eintrag)

Jeder Registry-Eintrag enthält **exakt** diese Felder:

1. **Artefakt-ID**
2. **Titel (klar, nicht kreativ)**
3. **Artefakt-Typ**
4. **Kurzbeschreibung (1–2 Sätze)**
5. **Status**
6. **Version**
7. **Owner-Rolle**
8. **Scope** (für wen / was gültig)
9. **Legitimitätsquelle**
10. **Verknüpfte Artefakte** (optional)
11. **Release-Datum**
12. **Review-by-Datum**
13. **Change-Policy-Referenz**

> Fehlt ein Feld → kein Zone‑1‑Status.
> 

---

## 6) Registry-Formate (prinzipiell)

Erlaubte Formen:

- Markdown-Tabelle
- YAML / JSON
- einfache Datenbank-Tabelle

Nicht erlaubt:

- Freitextlisten
- persönliche Notizen
- implizite Verweise

> Tool-Auswahl ist nachrangig – Struktur ist verbindlich.
> 

---

## 7) Lifecycle-Regeln

### 7.1 Aufnahme in die Registry

Erlaubt nur wenn:

- Artefakt freigegeben (Freeze)
- alle Metadaten vorhanden
- Version vergeben

### 7.2 Änderung

- Änderung → neue Version
- alte Version bleibt referenzierbar

### 7.3 Deprecation

- Status auf `Deprecated`
- Begründung erforderlich
- Nachfolger (falls vorhanden) verlinken

---

## 8) Anti-Pattern (explizit verboten)

- IDs nachträglich ändern
- Artefakte ohne Registry-Eintrag binden
- Mehrere „aktuelle“ Versionen
- implizite Gültigkeit („gilt schon irgendwie“)

---

## 9) Minimal-Operational-Check

Die Registry funktioniert, wenn:

- du innerhalb von **30 Sekunden** beantworten kannst:
    - Welche Artefakte sind aktuell bindend?
    - Wem gehören sie?
    - Für wen gelten sie?

Wenn das nicht geht → Registry unzureichend.

---

## 10) Gültigkeit & Änderung

- Diese Spec gilt ab sofort.
- Änderungen nur über formalen Change-Prozess.

---

> Die Registry ist kein Bürokratie-Tool.Sie ist die Voraussetzung für Freiheit durch Klarheit.
>
