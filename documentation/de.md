<!-- ELUCENIA technical documentation · probabilidade-pos-teste · de · no clinical/professional/rights approval -->

# Nachtestwahrscheinlichkeit (Satz von Bayes)

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/probabilidade-pos-teste)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Vortestwahrscheinlichkeit (Prävalenz oder klinische Schätzung)

`pre`

% · Bereich: 0,1–99,9

### Likelihood-Ratio des Ergebnisses (LR+ bei positiv, LR− bei negativ)

`rv`

Bereich: 0,001–1000

## Fassung der Methode

Bayes-Odds: Fagan 1975; Prätest-Odds×LR, Posttestumrechnung; Deeks–Altman 2004 LR

## Dokumentierte Formel

Prätest-Odds = p / (1 − p) · Posttest-Odds = Prätest-Odds × LR · Posttestwahrscheinlichkeit = Posttest-Odds / (1 + Posttest-Odds).

Die Odds-Form des Satzes von Bayes wird im Fagan-Nomogramm grafisch gelöst.

## Grenzen und Population

Die Vortestwahrscheinlichkeit muss die untersuchte Population und den klinischen Kontext abbilden; der Likelihood-Quotient muss zum Test und zur Ergebniskategorie passen. Wahrscheinlichkeit und Odds sind unterschiedliche Größen: Bei der Aktualisierung werden die Odds mit dem Likelihood-Quotienten multipliziert und erst dann in eine Wahrscheinlichkeit zurückgerechnet. Prädiktive Werte variieren mit der Prävalenz und sind nicht automatisch zwischen Studien und Einrichtungen übertragbar. Die Berechnung aktualisiert eine Schätzung; sie bestätigt oder schließt eine Krankheit nicht allein aus.

## Referenzen

- [Fagan TJ. Nomogram for Bayes's theorem. N Engl J Med, 1975.](https://doi.org/10.1056/NEJM197507312930513)

- [Deeks JJ, Altman DG. Diagnostic tests 4: likelihood ratios. BMJ, 2004.](https://doi.org/10.1136/bmj.329.7458.168)

- [Deeks/Altman2004,Diagnostic tests4:likelihood ratios](https://pmc.ncbi.nlm.nih.gov/articles/PMC478236/)

- [Fagan1975](https://doi.org/10.1056/NEJM197507313930513)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026
