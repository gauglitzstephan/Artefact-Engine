# A3 – Repositories & Speicherorte (V1)

# Zone-bewusstes Information Layout

> Zweck dieses Dokuments
> 
> 
> Diese Spec definiert, **wo Informationen physisch/technisch liegen**,
> 
> wie sie voneinander **getrennt**, **referenziert** und **bewegt** werden.
> 
> Ziel ist **Stabilität, Auditierbarkeit und mentale Entlastung** –
> 
> nicht Tool-Optimierung.
> 

---

## 1) Grundprinzip

> Zonen sind keine Denkmodelle – sie sind Speicherregime.
> 

Jede Zone hat:

- einen **eigenen Speicherort**
- eigene **Zugriffsregeln**
- eigene **Lebensdauer-Logik**

**Regel:**

> Inhalte dürfen Zonen wechseln, aber niemals gleichzeitig in mehreren liegen.
> 

---

## 2) Übersicht: Zonen → Speicher

| Zone | Zweck | Speichercharakter | Bindung |
| --- | --- | --- | --- |
| Zone 1 | Autorität & Bindung | stabil, versioniert | bindend |
| Zone 2 | Arbeit & Qualität | strukturiert, flüchtig | nicht bindend |
| Zone 3 | Exploration & Denken | frei, chaotisch erlaubt | niemals bindend |

---

## 3) Zone 1 – Repository für bindende Artefakte

### 3.1 Zweck

- **Single Source of Truth** für alles Bindende
- Grundlage für Audit, Review, Vertrauen

### 3.2 Inhalt (exklusiv)

- Frozen Artefakte (Policies, Core Kits, Standards)
- Registry (A2)
- Release Notes
- Change Logs
- Evidence Packs
- Deprecated Artefakte (read-only)

### 3.3 Struktur (konzeptionell)

```
/zone-1
  /registry
  /artefacts
    /GOV-CORE-001
      v1.0.0/
      v1.1.0/
    /GOV-POL-002
  /releases
  /audit

```

> Regel:
> 
> 
> Kein Draft, keine TODOs, keine Diskussionen in Zone 1.
> 

---

### 3.4 Zugriffsregeln

- Schreibzugriff: **nur über formalen Change/Release-Prozess**
- Lesen: erlaubt
- Löschen: nicht erlaubt (nur Deprecation)

---

## 4) Zone 2 – Workbench Repository

### 4.1 Zweck

- Ort für **qualitative Arbeit** ohne Bindungsdruck
- Vorbereitung für Zone-1-Releases

### 4.2 Inhalt

- Draft-Specs
- Reviews
- Red-Team-Notizen
- Vergleichsanalysen
- offene Entscheidungen (explizit markiert)

### 4.3 Struktur (konzeptionell)

```
/zone-2
  /drafts
  /reviews
  /analysis
  /pending-decisions

```

---

### 4.4 Lebensdauer-Regel

> Nichts in Zone 2 ist dauerhaft.
> 

Jedes Objekt braucht:

- Ziel: Release → Zone 1 **oder**
- Ablaufdatum → Archiv / Löschung

---

## 5) Zone 3 – Exploration Space

### 5.1 Zweck

- Denken ohne Konsequenz
- Kreativität ohne Rechtfertigung

### 5.2 Inhalt

- Ideen
- Skizzen
- Fragen
- persönliche Notizen
- Inspirationsmaterial

### 5.3 Regeln

- keine Strukturpflicht
- keine Vollständigkeit
- keine Review-Pflicht

> Zone 3 darf chaotisch sein.
> 

---

## 6) Übergänge zwischen Repositories

### 6.1 Zone 3 → Zone 2

- freiwillig
- ohne formalen Prozess
- Ziel: Arbeit beginnen

---

### 6.2 Zone 2 → Zone 1

Nur über:

- vollständige Spezifikation
- Review abgeschlossen
- Registry-Eintrag
- Release & Freeze

---

### 6.3 Zone 1 → Zone 2

Nur über:

- Change Request
- Impact-Bewertung
- alte Version bleibt gültig

---

## 7) Referenzierungsregeln

- Zone 1 darf **auf Zone 2/3 verweisen**, aber nur als Kontext
- Zone 2 darf **nie** implizit Zone-1-Autorität beanspruchen
- Links ersetzen keine Releases

---

## 8) Anti-Pattern (explizit verboten)

- Drafts in Zone 1
- „Final_v3_really_final.md“
- Entscheidungen in Chat-Logs
- Tool-abhängige Verweise ohne Artefakt-ID

---

## 9) Minimaler Funktionscheck

Das Layout funktioniert, wenn:

- du nachts sagen kannst, **wo die Wahrheit liegt**
- du Drafts löschen kannst, ohne Angst
- ein externer Prüfer Zone 1 versteht

---

## 10) Gültigkeit & Änderung

- Diese Spec gilt ab sofort.
- Änderungen nur über formalen Change-Prozess.

---

> Information ist nur dann wertvoll,wenn klar ist, wo sie nicht hingehört.
>
