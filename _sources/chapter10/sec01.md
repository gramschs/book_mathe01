---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  main_language: python
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.14.7
---

# 10.1 Ableitungen

Die Differentialrechnung ist ein zentrales Thema der Analysis. Mit Hilfe der
Differentialrechnung wird untersucht, wie sich Funktionen verändern. In diesem
Kapitel werden die dazu nötigen Begriffe eingeführt. Zunächst geht es um
Veränderungen in einem Bereich (mittlere Änderungsrate, Differenzenquotient und
Steigung einer Sekante) und dann um punktuelle Veränderungen (momentane
Änderungsrate, Differentialquotienten, Steigung einer Tangente, Ableitung).

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie wissen, was die **mittlere Änderungsrate** einer zeitabhängigen Größe ist
  und können diese berechnen.
* Sie können den **Differenzenquotienten** einer Funktion berechnen.
* Sie können den Differenzenquotient als **Steigung der Sekante** geometrisch
  interpretieren.
* Sie wissen, was die **momentane Änderungsrate** einer zeitabhängigen Größe ist
  und können diese berechnen.
* Sie können den **Differentialquotienten** bzw. die **Ableitung** einer
  Funktion berechnen.
* Sie können den Differentialquotient/Ableitung als **Steigung der Tangente**
  geometrisch interpretieren.
```

## Die mittlere Änderungsrate oder der Differenzenquotient

2018 hat Italien ein neues System zur Geschwindigkeitsmessung in Betrieb
genommen (siehe
[https://www.verkehrsrundschau.de](https://www.verkehrsrundschau.de/nachrichten/transport-logistik/italien-neues-system-zur-geschwindigkeitsmessung-in-betrieb-2985039)).
Das System funktioniert nach dem Prinzip
[Abschnittskontrolle](https://de.wikipedia.org/wiki/Abschnittskontrolle), das
wie folgt funktioniert. Entlang der Strecke befinden sich mehrere
Kontrollpunkte. Wenn ein Auto den ersten Kontrollpunkt passiert, wird es
fotografiert und sein Kennzeichen ermittelt. Wird das Auto dann beim nächsten
Kontrollpunkt erneut per Kamera identifiziert, kann aus der Strecke zwischen den
Kontrollpunkten und der verstrichenen Zeit zwischen den beiden Aufnahmen die
Durchschnittsgeschwindigkeit berechnet werden. Ist die
Durchschnittsgeschwindigkeit höher als die erlaubte Geschwindigkeit, wird
automatisch ein Bußgeldverfahren eingeleitet.

Ein deutscher Tourist ist mit seinem Pkw auf der Autobahn unterwegs. Nachdem er
auf die Autobahn aufgefahren ist, protokolliert sein Fahrtenschreiber zweimal
pro Minute die zurückgelegte Strecke. Die Höchstgeschwindigkeit auf
italienischen Autobahnen ist 130 km/h. Wird er einen Bußgeldbescheid bekommen?

```{code-cell} ipython3
:tags: [remove-input]
import numpy as np
import plotly.express as px

s_km = np.array([1.1, 
    2.1, 3.1, 4.2, 5.2, 6.3, 
    7.3, 8.4, 9.4, 10.5, 11.5, 
    12.6, 13.6, 14.7, 15.7, 16.8, 
    17.8, 18.9, 20.0, 21.0, 22.1, 
    23.1, 24.2, 25.3, 26.4, 27.6, 
    28.7, 29.8, 30.9, 32.0, 33.2, 
    34.3, 35.4, 36.5, 37.7, 38.8, 
    39.9, 41.1, 42.2, 43.3, 44.4, 
    45.5, 46.6, 47.7, 48.8, 49.8, 
    50.8, 51.8, 52.8, 53.8, 54.8, 
    55.9, 57.0, 58.1, 59.2, 60.2, 
    61.3, 62.4, 63.5, 64.6, 65.6])
t = np.linspace(10, 40, len(s_km))
fig = px.scatter(x = t, y = s_km,
                 labels = {'x': 'Zeit [min]', 'y': 'Strecke seit Autobahnauffahrt [km]'},
                 title='Protokoll des Fahrtenschreibers')
fig.show()
```

```{admonition} Mini-Übung
:class: miniexercise
Wenn Sie mit dem Mauszeiger über die Punkte des Diagramms fahren, werden die
Zeit und die Strecke, die seit der Autobahnauffahrt zurückgelegt wurde,
eingeblendet.

1. Berechnen Sie die Durchschnittsgeschwindigkeit im Zeitraum [10 min, 40 min]. 
2. Berechnen Sie die Durchschnittsgeschwindigkeit im Zeitraum [15 min, 20 min]. 
3. Berechnen Sie die Durchschnittsgeschwindigkeit im Zeitraum [20 min, 30 min]. 
```

```{admonition} Lösung
:class: miniexercise, toggle
1. Die Strecke zum Zeitpunkt t<sub>1</sub> = 10 min ist s<sub>1</sub> = 1.1 km. Zum Zeitpunkt t<sub>2</sub> = 40 min wurden s<sub>2</sub> = 65.6 km zurückgelegt. Damit ist die Durchschnittsgeschwindigkeit im Zeitraum [10 min, 40 min]

$$\frac{65.6 \text{ km} - 1.1 \text{ km}}{40 \text{ min} - 10 \text{ min}} = 
\frac{64.5 \text{ km}}{30 \text{ min}} = \frac{64.5 \text{ km}}{0.5 \text{ h}} = 129.0 \text{ km/h}.$$

2. Die Strecke zum Zeitpunkt t<sub>1</sub> = 15 min ist s<sub>1</sub> = 11.5 km. Zum Zeitpunkt t<sub>2</sub> = 20 min wurden s<sub>2</sub> = 22.1 km zurückgelegt. Damit ist die Durchschnittsgeschwindigkeit im Zeitraum [15 min, 20 min]

$$\frac{22.1 \text{ km} - 11.5 \text{ km}}{20 \text{ min} - 15 \text{ min}} = 
\frac{10.6 \text{ km}}{5 \text{ min}} = \frac{10.6 \text{ km}}{1/12 \text{ h}} = 127.2 \text{ km/h}.$$

3. Die Strecke zum Zeitpunkt t<sub>1</sub> = 20 min ist s<sub>1</sub> = 22.1 km. Zum Zeitpunkt t<sub>2</sub> = 30 min wurden s<sub>2</sub> = 44.4 km zurückgelegt. Damit ist die Durchschnittsgeschwindigkeit im Zeitraum [20 min, 30 min]

$$\frac{44.4 \text{ km} - 22.1 \text{ km}}{30 \text{ min} - 20 \text{ min}} = 
\frac{22.3 \text{ km}}{10 \text{ min}} = \frac{22.3 \text{ km}}{1/6 \text{ h}} = 133.8 \text{ km/h}.$$

Je nachdem, wo das Auto die Kontrollpunkte passiert hat, droht ein Bußgeld.
```

Die obige Vorgehensweise zur Ermittlung der Durchschnittsgeschwindigkeit kann
auf andere zeitabhängige Größen verallgemeinert werden. Ist auf der x-Achse die
Zeit $t$ aufgetragen und auf der y-Achse die zeitabhängige Größe $f(t)$, so gibt
der Quotient

\begin{equation*}
\frac{f(t_2) - f(t_1)}{t_2 - t_1}
\end{equation*}

die sogenannte **mittlere Änderungsrate** der zeitabhängigen Größe $f(t)$ an.

```{admonition} Was ist ... die mittlere Änderungsrate?
:class: note
Die mittlere Änderungsrate einer zeitabhängigen Größe gibt an, wie sich die
zeitabhängige Größe durchschnittlich zwischen zwei Zeitpunkten verändert. 
Sie wird folgendermaßen berechnet:
\begin{equation*} 
\text{mittlere Änderungsrate} = \frac{f(t_2) - f(t_1)}{t_2 - t_1}.
\end{equation*}
Dabei stehen $t_1$ und $t_2$ für die beiden Zeitpunkte und $f(t_1)$ und $f(t_2)$
jeweils für den Wert der zeitabhängigen Größe zu diesen Zeitpunkten.
```

Allgemeiner betrachtet, kann jeder funktionale Zusammenhang, bei dem auf der
x-Achse die Ursache und auf der y-Achse die Wirkung dargestellt sind, auf diese
Weise analysiert werden. Die abhängige Größe (Wirkung) bezeichnen wir mit $f$,
die Ursache mit $x$. Betrachten wir zwei Messungen zur Ursache $x_1$ und zur
Ursache $x_2$, dann wird der Quotient

\begin{equation*}
\frac{f(x_2) - f(x_1)}{x_2 - x_1}
\end{equation*}

ganz allgemein **Differenzenquotient** genannt. Im Zähler steht eine Differenz,
im Nennen steht eine Differenz, der Term ist also ein Quotient von Differenzen
oder kurz ausgedrückt, ein Differenzenquotient. Er gibt an, wie sich
durchschnittlich die Wirkung verändert, wenn sich deren Ursache verändert.

```{admonition} Was ist ... der Differenzenquotient?
:class: note
Für eine reellwertige Funktion $f$, bei der das Intervall $[x_1, x_2]$ zur
Definitionsmenge gehört, bezeichnen wir den Term
\begin{equation*} 
\frac{f(x_2) - f(x_1)}{x_2 - x_1} 
\end{equation*}
als Differenzenquotient von $f$ im Intervall $[x_1, x_2]$.
```

## Der Differenzenquotient geometrisch interpretiert

Bisher haben wir zwei verschiedene Kontrollpunkte auf der Autobahn oder
allgemein zwei verschiedene Ursachen $x_1$ und $x_2$ betrachtet. Betrachten wir
die Punkte $(x_1, f(x_1))$ und $(x_2, f(x_2))$ rein geometrisch, also mit ihren
Koordinaten $(x_1,y_1)$ und $(x_2,y_2)$, so lautet der Differenzenquotient

\begin{equation*}
\frac{f(x_2) - f(x_1)}{x_2 - x_1} = \frac{y_2 - y_1}{x_2 - x_1} = \frac{\Delta y}{\Delta x}.
\end{equation*}

Verbinden wir die beiden Punkte $(x_1,y_1)$ und $(x_2,y_2)$ durch eine Gerade,
dann ist der Differenzenquotient die Steigung dieser Gerade. Diese spezielle
Gerade, die zwei Punkte eines Funktionsgraphens miteinander verbindet, wird
**Sekante** genannt. Der Differenzenquotient ist also die Steigung der Sekante.

```{dropdown} Video zu "Mittlere Änderungsrate" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/sXxK-JATrc0?si=bdcHhSJOUHSl3fNg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

> - [https://studyflix.de/mathematik/mittlere-aenderungsrate-4021](https://studyflix.de/mathematik/mittlere-aenderungsrate-4021)
> - [https://studyflix.de/mathematik/differenzenquotient-1881](https://studyflix.de/mathematik/differenzenquotient-1881)

## Die momentane Änderungsrate oder der Differentialquotient

Die mittlere Änderungsrate gibt uns eine durchschnittliche Veränderung innerhalb
eines Intervalls $[t_1, t_2]$. Aber was ist, wenn wir wissen möchten, wie sich
eine zeitabhängige Größe genau in einem bestimmten Zeitpunkt ändert? Hier kommt
die momentane Änderungsrate ins Spiel. Bei der Betrachtung der momentanen
Änderungsrate konzentrieren wir uns auf ein Zeitintervall, das so klein wird,
dass es fast einem einzelnen Punkt entspricht. In diesem Kontext nähert sich
$t_2$ kontinuierlich $t_1$ an, bis sie praktisch identisch sind. Mathematisch
ausgedrückt betrachten wir den Grenzwert $t_2 \to t_1$. Da die mittlere
Änderungsrate für das Intervall $[t_1, t_2]$ definiert ist, ändert sie sich mit
dem Intervall. Es entsteht eine Folge von mittleren Änderungsraten für immer
kleiner werdende Intervalle $[t_1, t_2]$. Wenn diese Folge von mittleren
Änderungsraten einen Grenzwert hat, nennen wir diesen Grenzwert **momentane
Änderungsrate**.

```{admonition} Was ist ... die momentane Änderungsrate?
:class: note
Die momentane Änderungsrate beschreibt die Änderung einer zeitabhängigen Größe für ein
unendlich kleines Intervall. Mathematisch ausgedrückt, ist sie der Grenzwert der
mittleren Änderungsrate:
\begin{equation*} 
\text{momentane Änderungsrate} = 
\lim_{t_2 \to t_1} \frac{f(t_2) - f(t_1)}{t_2 - t_1},
\end{equation*}
sofern der Grenzwert existiert.
```

Im Gegensatz zum Differenzenquotienten, der sich auf ein Zeitintervall $t_1,
t_2]$ bezieht, bezieht sich der Differentialquotient auf einen einzelnen
Zeitpunkt $t_1$.

Betrachten wir das obige Beispiel des deutschen Touristen auf der italienischen
Autobahn. Während die mittlere Änderungsrate uns die durchschnittliche
Geschwindigkeit über ein bestimmtes Zeitintervall gibt, würde die momentane
Änderungsrate uns die exakte Geschwindigkeit zu einem bestimmten Zeitpunkt, z.B.
genau 20 Minuten nach der Autobahnauffahrt, anzeigen.

Auch hier können wir den Begriff der momentanen Änderungsrate auf beliebige
funktionale Zusammenhänge verallgemeinern. Aus dem Differenzenquotienten wird so
der Differentialquotient.

```{admonition} Was ist ... der Differentialquotient?
:class: note
Wenn das Intervall des Differenzenquotienten unendlich klein wird und der
Grenzwert des Differenzenquotienten  
\begin{equation*} 
\lim_{x_2 \to x_1} \frac{f(x_2) - f(x_1)}{x_2 - x_1}
\end{equation*}
existiert, nennt man diesen Grenzwert Differentialquotient der Funktion $f$ an
der Stelle $x_1$.
```

## Geometrische Interpretation des Differentialquotienten

Während der Differenzenquotient die Steigung einer Sekante zwischen zwei Punkten
eines Funktionsgraphen beschreibt, gibt der Differentialquotient die Steigung
der Tangente an einem bestimmten Punkt des Graphen an. Die **Tangente** ist eine
Gerade, die den Graphen nur an diesem einen Punkt berührt.

Mathematisch ausgedrückt, wenn der Abstand $\Delta x$ zwischen zwei x-Werten $x$
und $x + \Delta x$ gegen Null geht, nähert sich die Sekante einer Tangente an.
Der Differentialquotient

\begin{equation*}
\lim_{\Delta x \to 0}\frac{f(x + \Delta x) - f(x)}{\Delta x}
\end{equation*}

gibt dann die Steigung dieser Tangente am Punkt $(x, f(x)$ an. Die Steigung der
Tangente der Funktion $f$ an der Stelle $x$ wird meist mit einem Strich
abgekürzt, also

\begin{equation*}
f'(x) = \lim_{\Delta x \to 0}\frac{f(x + \Delta x) - f(x)}{\Delta x}.
\end{equation*}

Man spricht das als "f Strich an der Stelle x ist ..." oder sagt "die Ableitung
der Funktion f an der Stelle x ist ...".

Geometrisch gesehen ist die Tangente die beste lineare Näherung der Funktion an
einem Punkt. Sie gibt uns eine Vorstellung davon, wie sich die Funktion in der
unmittelbaren Umgebung dieses Punktes verhält.

Um noch einmal auf das Beispiel zurückzukommen: Betrachten Sie die
Geschwindigkeit eines Autos auf der Autobahn. Während der Differenzenquotient
uns die durchschnittliche Geschwindigkeit zwischen zwei Zeitpunkten gibt, würde
der Differentialquotient uns die exakte Geschwindigkeit zu einem bestimmten
Zeitpunkt anzeigen.

```{dropdown} Video zu "Differentialquotient" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/_L6wmTzod_I?si=Fj3jbGIOcc3mC4wc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

```{dropdown} Video zu "Ableitung" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/FW7Vd1VI3uw?si=Ij7j2mb5CIKNYUEH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

> - [https://studyflix.de/mathematik/momentane-aenderungsrate-4034](https://studyflix.de/mathematik/momentane-aenderungsrate-4034)
> - [https://studyflix.de/mathematik/differentialquotient-1339](https://studyflix.de/mathematik/differentialquotient-1339)

## Zusammenfassung und Ausblick

In diesem Kapitel haben wir mit der Ableitung den zentralen Begriff der
Differentialrechnung kennengelernt. Es ist jedoch mühsam, die Ableitung bzw. den
Differentialquotienten als Grenzwert einer Folge von Differenzenquotienten zu
berechnen. Daher werden wir uns im nächsten Kapitel mit Rechenregeln für
Ableitungen beschäftigen, die die Grenzwertbildung vermeiden.