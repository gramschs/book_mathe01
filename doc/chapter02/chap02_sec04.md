# 2.4 Exponential- und Logarithmusfunktionen

Bevor wir unsere Kugelbahn um weitere komplexe Elemente erweitern, gönnen wir
uns eine wohlverdiente Pause. Während wir auf unseren heißen Kaffee oder Tee
warten, bis er trinkbar wird, können wir ein faszinierendes mathematisches
Phänomen beobachten: die Abkühlung folgt einem ganz bestimmten Muster und dieses
Muster führt uns zu einer neuen, wichtigen Klasse von Funktionen: den
Exponential- und Logarithmusfunktionen.

## Lernziele

```{admonition} Lernziele Exponential- und Logarithmusfunktion
:class: goals
* Sie kennen die **Exponentialfunktion** $f(x) = a^x$ und die **natürliche
  Exponentialfunktion** $f(x) = e^x$ mit der Eulerschen Zahl $e \approx
  2.718$.
* Sie können **exponentielles Wachstum** und **exponentiellen Zerfall** am
  Beispiel der Abkühlung erkennen und verstehen.
* Sie verstehen den **Logarithmus als Umkehrfunktion** der Exponentialfunktion
  und kennen die Definition: $y = \log_a(x) \Leftrightarrow a^y = x$.
* Sie können mit dem **natürlichen Logarithmus** $\ln(x)$ arbeiten und einfache
  **Exponentialgleichungen lösen**.
```

## Die abkühlende Tasse

Unsere Kugelbahn hat sich in den letzten Kapiteln immer weiter entwickelt. Wir
haben gerade Schienen, gekrümmte Bahnen und sogar Polynome höheren Grades
kennengelernt, um komplexe Höhenprofile zu beschreiben. Bevor wir aber die
nächsten aufwendigen Konstruktionen planen, gönnen wir uns eine wohlverdiente
Pause und bereiten uns eine Tasse Kaffee oder Tee zu.

Das Problem kennen wir alle: Frisch aufgebrühter Kaffee ist mit etwa 90°C viel
zu heiß zum Trinken. Wir müssen warten, bis er auf eine angenehme
Trinktemperatur von etwa 60-65°C abgekühlt ist. Aber wie lange dauert das
eigentlich? Und gibt es ein mathematisches Muster, das diesen Abkühlungsprozess
beschreibt? Beobachten wir die Temperatur unseres Kaffees über die Zeit:

BILD
Temperaturverlauf einer abkühlenden Tasse Kaffee
(Quelle: eigene Darstellung)

Wir stellen fest:

* In den ersten Minuten kühlt der Kaffee relativ schnell ab - von 90°C auf
  vielleicht 70°C in wenigen Minuten.
* Danach verlangsamt sich die Abkühlung zunehmend. Von 70°C auf 60°C dauert es
  schon deutlich länger.
* Je näher die Kaffeetemperatur an die Raumtemperatur (ca. 20°C) kommt, desto
  langsamer wird der Abkühlungsprozess.
* Die Temperatur nähert sich asymptotisch der Raumtemperatur an, erreicht sie
  aber theoretisch nie ganz.

Dieses Verhalten ist typisch für viele natürliche Prozesse: Die
Änderungsgeschwindigkeit (hier: wie schnell die Temperatur sinkt) ist
proportional zur aktuellen Differenz (hier: Temperaturunterschied zur Umgebung).
Je größer der Unterschied, desto schneller der Ausgleich. Der britische Physiker
Isaac Newton beschrieb dieses Phänomen bereits im 17. Jahrhundert. Das
Newton'sche Abkühlungsgesetz besagt:

Die Abkühlungsgeschwindigkeit eines Körpers ist proportional zur
Temperaturdifferenz zwischen dem Körper und seiner Umgebung.

Mathematisch ausgedrückt: Je heißer der Kaffee im Vergleich zur Raumtemperatur
ist, desto schneller kühlt er ab. Diese Art von Zusammenhang - wo die
Änderungsrate proportional zum aktuellen Wert ist - führt uns zu einer völlig
neuen Klasse von Funktionen: den Exponentialfunktionen. Und wenn wir dann die
Frage stellen "Wann genau kann ich meinen Kaffee trinken?", werden wir die
Logarithmusfunktion als Umkehrfunktion kennenlernen, die uns hilft, diese Frage
zu beantworten. Machen wir es uns also gemütlich und schauen uns an, welche
Mathematik in unserer Kaffeetasse steckt!

## Exponentialfunktion

* Die Eulersche Zahl $e \approx 2{,}71828...$
* Die Funktion $f(x) = e^x$
* Graph und grundlegende Eigenschaften
* Exponentielles Wachstum ($e^x$) vs. exponentieller Zerfall ($e^{-x}$)

## Modellierung: Die abkühlende Tasse

* Newton'sches Abkühlungsgesetz: $T(t) = T_{\text{Umgebung}} + (T_0 - T_{\text{Umgebung}}) \cdot e^{-kt}$
* Beispielrechnung mit konkreten Zahlen
* Graph der Abkühlungskurve

```{dropdown} Video "Exponentialfunktion zur Basis e" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/VpR358f1fMk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Wie unterscheiden sich Potenz- und Exponentialfunktionen?" von studiVEMINT
<iframe width="560" height="315" src="https://www.youtube.com/embed/yHwnMuNurjs?si=4UBNTd31CLTfH-oD"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" 
referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Logarithmusfunktion

### Motivation: Die Umkehrfrage

* Gegeben: Zieltemperatur (z.B. 65°C)
* Gesucht: Wie lange muss ich warten?
* Wir brauchen die Umkehrfunktion!

### Der natürliche Logarithmus

* Definition: $\ln(x)$ als Umkehrfunktion von $e^x$
* $y = \ln(x) \Leftrightarrow e^y = x$
* Graph der Logarithmusfunktion
* Grundlegende Eigenschaften

### Lösung: Wann kann ich meinen Kaffee trinken?

* Auflösen der Abkühlungsgleichung
* Beispielrechnung

```{dropdown} Video "Logarithmusfunktion zur Basis e" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/Ed98rKCSTXY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```
