# Vorlage für ein Skript

Diese Vorlage zeigt Kopf, Legende, ein Beispielkapitel und den Schluss mit Glossar. Platzhalter in eckigen Klammern ersetzen. Das Beispielkapitel behandelt „Wahrscheinlichkeit" nur zur Illustration des Rhythmus (Intuition, Definition, Mechanismus, Beispiel, Grenzfall, Zusammenfassung, Notizen).

---

## Dateikopf

```markdown
# [Titel des Themas]
*Lernskript auf Universitätsniveau, ohne Vorkenntnisse*

**Stand:** [Datum] · **Voraussetzungen:** keine · **Umfang:** [n] Kapitel

## Legende

| Kästchen | Bedeutung |
|---|---|
| 🟦 | Definition |
| 🟩 | Beispiel |
| 🟨 | Merksatz |
| 🟥 | Achtung / typischer Fehler |
| 🟧 | Herleitung / Mechanismus |
| 🟪 | Vertiefung (beim ersten Lesen überspringbar) |
| ⬜ | Lernziele / Zusammenfassung |
| 📝 | Notizen |

## Inhaltsverzeichnis

1. [Kapitel 1](#1-kapitel-1)
2. [Kapitel 2](#2-kapitel-2)
…
- [Gesamtzusammenfassung](#gesamtzusammenfassung)
- [Glossar](#glossar)
- [Quellen](#quellen)
```

---

## Beispielkapitel

```markdown
## 2 Wahrscheinlichkeit

> ⬜ **Lernziele**
>
> - Den Begriff Wahrscheinlichkeit definieren und von Häufigkeit unterscheiden
> - Wahrscheinlichkeiten einfacher Ereignisse berechnen
>
> **Voraussetzungen:** Kapitel 1 (Mengen und Ereignisse)

### 2.1 Worum geht es? (Intuition)

Wer eine Münze wirft, weiß vorher nicht, ob Kopf oder Zahl fällt. Trotzdem gibt es eine Regelmäßigkeit: Bei sehr vielen Würfen fällt etwa die Hälfte auf Kopf. Die Wahrscheinlichkeitsrechnung beschreibt solche Regelmäßigkeiten bei unsicherem Ausgang mathematisch.

### 2.2 Grundbegriffe

> 🟦 **Definition: Zufallsexperiment**
>
> Ein Vorgang, dessen Ausgang nicht sicher vorhersagbar ist, der aber unter gleichen Bedingungen beliebig oft wiederholt werden kann.

> 🟦 **Definition: Wahrscheinlichkeit**
>
> Eine Zahl $P(A)$ zwischen 0 und 1, die angibt, wie plausibel das Eintreten eines Ereignisses $A$ ist. 0 bedeutet unmöglich, 1 bedeutet sicher.

### 2.3 Wie berechnet man sie? (Mechanismus)

> 🟧 **Herleitung: Laplace-Wahrscheinlichkeit**
>
> Sind alle Ausgänge gleich wahrscheinlich, teilt man die Zahl der günstigen Ausgänge durch die Zahl aller möglichen:
> $$P(A) = \frac{\text{günstige Ausgänge}}{\text{mögliche Ausgänge}}$$

> 🟩 **Beispiel: Würfel**
>
> Wahrscheinlichkeit für eine gerade Zahl: günstig sind 2, 4, 6 (3 Ausgänge), möglich sind 6. Also $P = 3/6 = 0{,}5$.

### 2.4 Grenzfälle

> 🟥 **Achtung**
>
> Die Formel gilt nur bei gleich wahrscheinlichen Ausgängen. Bei einem gezinkten Würfel liefert sie falsche Ergebnisse.

> 📝 **Notizen**
>
> &nbsp;
>
> &nbsp;
>
> &nbsp;

### 2.5 Zusammenfassung

> ⬜ **Das Wichtigste aus Kapitel 2**
>
> - Wahrscheinlichkeit liegt immer zwischen 0 und 1.
> - Bei gleich wahrscheinlichen Ausgängen: günstige geteilt durch mögliche.
> - Prüfe immer erst, ob die Gleichverteilung wirklich gegeben ist.

> 📝 **Notizen zu Kapitel 2**
>
> &nbsp;
>
> &nbsp;
>
> &nbsp;
>
> &nbsp;
>
> &nbsp;
```

---

## Schluss

```markdown
## Gesamtzusammenfassung

Kurze Liste der zentralen Erkenntnisse aus allen Kapiteln, jeweils mit Kapitelverweis.

## Glossar

**Wahrscheinlichkeit** (Kap. 2): Zahl zwischen 0 und 1, die die Plausibilität eines Ereignisses angibt.
**Zufallsexperiment** (Kap. 2): Wiederholbarer Vorgang mit nicht sicher vorhersagbarem Ausgang.
…

## Quellen

- [Autor/Institution: Titel, Jahr, Link]
```
