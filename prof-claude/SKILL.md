---
name: skript-ersteller
description: Erstellt aus einem beliebigen Thema ein vollständiges Lernskript auf Universitätsniveau als Markdown-Datei – beginnt bei Null, definiert jeden Fachbegriff vor der ersten Nutzung, arbeitet mit farbigen Kästchen (Definition, Beispiel, Merksatz, Achtung) und Notizfeldern und endet mit Glossar und Zusammenfassung. Immer verwenden, wenn der Nutzer ein Skript, Lernskript, Vorlesungsskript, eine Lernunterlage, "Thema von Grund auf erklärt" oder "Uni-Skript zu X" haben will, auch wenn er das Wort "Skript" nicht benutzt, sondern z. B. sagt "erklär mir X von Grund auf und ausführlich zum Mitlernen".
---

# Skript-Ersteller

Ziel: Ein Lernskript, mit dem eine Person ohne Vorwissen ein Thema bis auf Universitätsniveau durcharbeiten kann. Das Skript ist ein Nachschlage- und Lehrwerk zugleich, also vollständig statt kurz, und aufbauend statt sprunghaft. Der Nutzer will lernen und mitschreiben, nicht überfliegen.

## Ablauf

1. **Thema und Rahmen klären.** Aus der Anfrage ableiten: Thema, Vorwissen (Standard: keines), Zielniveau (Standard: Universität, Bachelor-Grundlagen bis solide Vertiefung), Sprache (die des Nutzers). Nur nachfragen, wenn das Thema so mehrdeutig ist, dass ein falscher Zuschnitt das ganze Skript entwertet. Sonst Annahmen in einem Satz nennen und loslegen.

2. **Wissensbasis sichern.** Bei Themen, die sich ändern (Technik, Recht, Medizin-Leitlinien, Normen, Versionen) zuerst recherchieren und die Quellen sammeln. Bei stabilem Stoff reicht eigenes Wissen. Unsicheres als unsicher markieren, nichts erfinden. Zahlen, Formeln und Rechenbeispiele nachrechnen.

3. **Abhängigkeiten ordnen.** Alle nötigen Konzepte auflisten und so sortieren, dass jedes Konzept nur auf bereits erklärte aufbaut. Das ist der Kern von „bei Null beginnen": Wo Grundlagen fehlen, kommt ein Grundlagenkapitel davor, auch wenn das Thema selbst „fortgeschritten" klingt. Gliederung (Kapitel, Unterkapitel) festlegen und dem Nutzer nicht zur Freigabe vorlegen, sondern direkt umsetzen.

4. **In Etappen schreiben.** Lange Skripte entstehen kapitelweise: Datei mit Kopf, Legende und Inhaltsverzeichnis anlegen, dann jedes Kapitel anhängen. Ein einziger Riesenschritt verliert Qualität gegen Ende. Vorlage und Beispielkapitel: `references/vorlage.md` lesen, bevor das erste Kapitel geschrieben wird.

5. **Glossar und Gesamtzusammenfassung** am Ende schreiben, wenn der Text steht (dann sind alle Begriffe bekannt).

6. **Prüfen** (siehe Checkliste unten), korrigieren, Datei ausliefern.

## Aufbau des Skripts

Reihenfolge der Datei:

1. Titel, Untertitel, Datum, Zielgruppe/Voraussetzungen (meist „keine")
2. **Legende** der Kästchen (Tabelle, siehe unten)
3. Inhaltsverzeichnis
4. Kapitel 1 … n
5. Gesamtzusammenfassung (die wichtigsten Punkte des ganzen Skripts, kurz)
6. **Glossar**
7. Quellen / weiterführende Literatur (nur, wenn echte Quellen genutzt wurden)

### Aufbau jedes Kapitels

Jedes Kapitel folgt der Logik „einfach → komplex" und enthält diese Bausteine in dieser Reihenfolge, wobei Unterkapitel je nach Größe den gleichen Rhythmus wiederholen:

1. **Lernziele** und **Voraussetzungen** (Verweis auf frühere Kapitel)
2. **Intuition**: Worum geht es und wozu braucht man das? Ein Alltagsbild oder Problem, bevor Formalismus kommt.
3. **Begriffe und Definitionen**: jeder neue Fachbegriff in einem Definitionskästchen, bevor er im Fließtext verwendet wird
4. **Mechanismus**: Wie und warum funktioniert es? Schrittweise herleiten, nicht nur behaupten
5. **Beispiel**: mindestens ein durchgerechnetes oder konkretes Beispiel pro Konzept
6. **Grenzfälle und typische Fehler**: Ausnahmen, Missverständnisse, Gültigkeitsbereich
7. **Zusammenfassung** des Kapitels (kurze Stichpunkte)
8. **Notizen**-Feld

### Fachbegriffe und Fremdwörter

Regel: Kein Fachbegriff und kein Fremdwort wird benutzt, bevor es erklärt ist. Das gilt auch für Abkürzungen. Beim ersten Auftreten steht der Begriff **fett** mit sofortiger Erklärung (Definitionskästchen oder Halbsatz in Klammern, je nach Gewicht). Danach darf er frei verwendet werden. Jeder so eingeführte Begriff kommt zusätzlich ins Glossar. Wenn ein Begriff notgedrungen vor seiner vollständigen Definition fallen muss, eine kurze Arbeitsdefinition geben und mit „→ siehe Kapitel X" auf die genaue verweisen.

## Farbige Kästchen

Reines Markdown kennt keine Farben. Deshalb werden die Kästchen als Blockquotes mit farbigem Emoji-Quadrat als Kopf gebaut. Das rendert in praktisch jedem Markdown-Viewer (GitHub, VS Code, Obsidian, Typora) gleich. Diese Legende steht am Anfang des Skripts:

| Kästchen | Verwendung |
|---|---|
| 🟦 | Definition eines Begriffs |
| 🟩 | Beispiel, Rechenbeispiel, Anwendung |
| 🟨 | Merksatz, Kernaussage, Formel zum Auswendiglernen |
| 🟥 | Achtung: typischer Fehler, Falle, Ausnahme |
| 🟧 | Herleitung, Mechanismus, Beweisidee |
| 🟪 | Vertiefung, Exkurs (kann beim ersten Lesen übersprungen werden) |
| ⬜ | Lernziele und Kapitelzusammenfassung |
| 📝 | Notizen (leeres Feld zum Selbstausfüllen) |

Format eines Kästchens:

```markdown
> 🟦 **Definition: Begriff**
>
> Erklärung in ein bis drei Sätzen.
```

Kästchen sparsam und gezielt einsetzen: Pro Bildschirmseite höchstens zwei bis drei, sonst verlieren sie ihre Signalwirkung. Fließtext trägt die Erklärung, Kästchen heben das Wichtige heraus.

## Platz für Notizen

Ein echter Seitenrand ist in Markdown nicht darstellbar. Als Ersatz folgt auf jedes Unterkapitel ein leeres Notizfeld, das im Editor direkt beschriftet werden kann, und am Kapitelende ein größeres:

```markdown
> 📝 **Notizen**
>
> &nbsp;
>
> &nbsp;
>
> &nbsp;
```

Für das Kapitelende fünf statt drei `&nbsp;`-Zeilen. Dem Nutzer in der Abschlussnachricht kurz sagen, dass ein echter Rand nur über eine HTML- oder PDF-Variante geht, und anbieten, diese zu erzeugen.

## Glossar

Eigener Abschnitt am Ende, alphabetisch sortiert, ein Eintrag pro Begriff:

```markdown
**Begriff** (Kap. 2): Knappe, präzise Erklärung. Gegebenenfalls Synonym oder englischer Fachbegriff in Klammern.
```

Das Glossar enthält alle im Skript eingeführten Fachbegriffe, Fremdwörter und Abkürzungen, auch solche, die nur in Kästchen oder Klammern erklärt wurden. Die Kapitelangabe verweist auf die Stelle der Einführung.

## Schreibstil

Sachlich, präzise und klar, wie ein gutes Vorlesungsskript, nicht wie ein Blogbeitrag. Vollständige Sätze, kein Füllmaterial, keine Wiederholungen außer in den Zusammenfassungen. Formeln in LaTeX-Schreibweise (`$…$`, `$$…$$`), wenn das Thema es verlangt, mit jeder Variablen erklärt. Tabellen nur für echte Vergleiche, Listen nur für echte Aufzählungen, sonst Prosa.

## Checkliste vor der Auslieferung

- Vollständigkeit: Ist das Thema in Breite und Tiefe abgedeckt, die ein Uni-Skript dazu hätte? Fehlen Grundlagen, auf denen spätere Kapitel stillschweigend aufbauen?
- Reihenfolge: Wird irgendwo ein Begriff oder Konzept benutzt, das erst später erklärt wird?
- Begriffe: Stichprobe der Fachwörter im Text gegen die Definitionen und das Glossar prüfen, in beide Richtungen.
- Zahlen und Formeln: Beispiele nachgerechnet, Aussagen mit Quellen abgeglichen.
- Format: Legende vorhanden, Kästchen einheitlich, Notizfelder da, Inhaltsverzeichnis stimmt mit den Überschriften überein.

## Auslieferung

Die Datei als `skript-<thema-kurzname>.md` schreiben und dem Nutzer senden. In der Abschlussnachricht nur wenige Sätze: Umfang (Kapitelzahl), getroffene Annahmen, offene Unsicherheiten. Den Inhalt des Skripts nicht im Chat wiederholen.
