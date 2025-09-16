# 2.2 Eigenschaften von Funktionen

Nachdem wir im vorherigen Kapitel die Grundlagen von Funktionen anhand einer
einfachen geraden Kugelbahn kennengelernt haben, erweitern wir nun das
Kugelbahn-System. Wir bauen verschiedene Bahnformen und entdecken dabei wichtige
Eigenschaften von Funktionen, die uns helfen, das Verhalten mathematischer
Zusammenhänge zu verstehen und zu klassifizieren.

## Lernziele

```{admonition} Lernziele Eigenschaften von Funktionen
:class: goals
Sie kennen die wichtigsten Eigenschaften von mathematischen Funktionen wie
beispielsweise
- **Monotonie**,
- **Symmetrie**,
- **Periodizität** und
- **Beschränktheit**.
```

## Monotonie - Steigt oder fällt die Bahn?

Betrachten wir zunächst unsere ursprüngliche gerade Kugelbahn genauer. Die Kugel
rollt von links nach rechts und ihre Höhe wird dabei kontinuierlich niedriger.
Diese Eigenschaft nennen wir **Monotonie**.

```{raw} html
<div class="kugelbahn-wrapper">
<iframe src="../chap02/marble_track_simple.html"
width="100%" height="500"
frameborder="0"scrolling="no"
title="Interaktive Kugelbahn">
</iframe>
</div>
```

Je größer der Abstand zum Start ist, desto niedriger ist die Höhe der Kugel und
das gilt sogar streng. Wir formulieren diese Beobachtung mathematisch: Wenn
$x_1$ kleiner als $x_2$ ist, dann ist die Höhe $h(x_1)$ echt größer als die Höhe
$h(x_2)$. Verallgemeinert auf alle Funktionen gilt:

Eine Funktion $f$ heißt **streng monoton fallend**, wenn ihre Funktionswerte mit
wachsenden x-Werten streng abnehmen:

$$x_1 < x_2 \quad \Rightarrow \quad f(x_1) \textcolor{red}{>} f(x_2).$$

Wir können uns aber auch vorstellen, ein Plateau einzubauen, wie in der
folgenden Kugelbahn. Damit leichter erkennbar ist, wo das Plateau beginnt, wird
die Kugel bei einem Plateau weiß gefärbt. Je steiler die Kugelbahn ist, desto
dunkler wird die Kugel eingefärbt. Das hat nichts mit der physikalischen
Geschwindigkeit der Kugel zu tun, sondern zeigt die Eigenschaften der Schienen.

```{raw} html
<div class="kugelbahn-wrapper">
<iframe src="../chap02/marble_track_simple_with_plateau.html"
width="100%" height="500"
frameborder="0"scrolling="no"
title="Interaktive Kugelbahn">
</iframe>
</div>
```

Wenn wir die obige Kugelbahn als mathematische Funktion darstellen möchten,
müssen wir drei Abschnitte unterscheiden:

- Abschnitt 1: von 0 cm bis 8 cm gilt $\;h_1(x)=-0.25x+6$,
- Abschnitt 2: von 8 cm bis 12 cm gilt $\;h_2(x)=4$,
- Abschnitt 3: von 12 cm bis 24 cm gilt $\;h_3(x)=-\frac{1}{3}x+8$.

Die Definitionsmenge $D=[0;24]$ wird in drei Teilintervalle

$$I_1 = [0;8], \quad I_2 = (8; 12], \quad I_3 = (12; 24]$$

unterteilt und für jeden Abschnitt gilt eine andere Funktionsgleichung. Die
Intervalle sind dabei so gewählt, dass sie nicht überlappen. Die Position $x=8$
beispielsweise gehört eindeutig zum ersten Intervall und nicht zum zweiten. Eine
solche Funktion nennen wir **abschnittsweise definierte Funktion**. Insgesamt
schreiben wir die Höhenfunktion $h$ folgendermaßen:

$$h(x) = \begin{cases}
-0.25x+6, \quad & x\in[0;8],\\
4, \quad & x\in(8; 12],\\
-\frac{1}{3}x+8, \quad & x\in(12; 24].
\end{cases}$$

Mehr zu abschnittsweise definierten Funktionen finden Sie im folgenden Video:

```{dropdown} Video "abschnittsweise definierte Funktionen" von Mathematische Methoden
<iframe width="560" height="315"
src="https://www.youtube.com/embed/XGpoI5X5z5s?si=Afjv_VDPQwLUI_ln"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

Die Höhenfunktion zeigt folgendes Monotonieverhalten:

- Abschnitt 1 (für das Intervall $I_1=[0; 8]$): streng monoton fallend, d.h.
  $h(x_1)>h(x_2)$,
- Abschnitt 2 (für das Intervall $I_2=(8; 12]$): konstant, d.h. $h(x_1)=h(x_2)$,
- Abschnitt 3 (für das Intervall $I_3=(12; 24]$): streng monoton fallend, d.h.
  $h(x_1)>h(x_2)$.

Wenn wir den Begriff »streng« lockern, dann gilt für die gesamte Funktion $h$
auf der kompletten Definitionsmenge $D=[0; 24]$ entweder $h(x_1) > h(x_2)$ oder
$h(x_1)=h(x_2)$, wobei $x_1<x_2$ vorausgesetzt wird. Die Funktion ist
abschnittsweise streng monoton fallend und insgesamt (auf $[0,24]$) **monoton
fallend**.

Für die Kugelbahn könnte es ein Förderband geben, das die Kugel zum Start-Block
transportiert. Das wäre eine wachsende Funktion, da die Funktionswerte größer
werden, je weiter wir uns nach rechts auf der $x$-Achse bewegen. Wir fassen
zusammen:

```{admonition} Was ist ... Monotonie?
:class: note
Sei $D\subset\mathbb{R}$ und $f$ eine reellwertige Funktion
$f:D\rightarrow\mathbb{R}$. Die Funktion $f$ heißt auf einem Intervall $I\subset
D$
- **monoton wachsend**, falls für alle $x_1, x_2 \in I$ gilt:<br>
Wenn $x_1 < x_2$, dann $f(x_1) \leq f(x_2)$.
- **streng monoton wachsend**, falls für alle $x_1, x_2 \in I$ gilt:<br>
Wenn $x_1 < x_2$, dann $f(x_1) < f(x_2)$.
- **monoton fallend**, falls für alle $x_1, x_2 \in I$ gilt:<br>
Wenn $x_1 < x_2$, dann $f(x_1) \geq f(x_2)$.
- **streng monoton fallend**, falls für alle $x_1, x_2 \in I$ gilt:<br>
Wenn $x_1 < x_2$, dann $f(x_1) > f(x_2)$.
```

Hinweis: In diesem Vorlesungsskript verwenden wir konsequent die Bezeichnungen
wachsend/fallend. In anderen Quellen wird oft auch steigend/abnehmend gesagt.

Mehr Details zur Monotonie finden Sie in den folgenden Videos.

```{dropdown} Video "Was ist Monotonie?" von studiVEMINT
<iframe width="560" height="315"
src="https://www.youtube.com/embed/QfDPvxHAz3k?si=krDjMMRx1o328vNU"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Monotonie" von HM Kompakt
<iframe width="560" height="315"
src="https://www.youtube.com/embed/FFfcZK_nCws?si=VPXEZSaDTb7Wdb3x"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{admonition} Weiteres Lernmaterial
:class: seealso
- [Monoton steigend und fallend von
  Studyflix](https://studyflix.de/mathematik/was-ist-monotonie-7417)
- [Monotonie von Serlo](https://de.serlo.org/mathe/1911/monotonie)
```

## Beschränktheit - Wie hoch und wie tief geht es?

Jede reale Kugelbahn hat physikalische Grenzen. Diese führen uns zum Konzept der
**Beschränktheit**.

```{admonition} Was ist ... Beschränktheit?
:class: note
Eine Funktion $f$ heißt **nach oben beschränkt**, wenn es eine Zahl $S$ gibt,
sodass $f(x) \leq S$ für alle $x$ aus der Definitionsmenge.

Eine Funktion $f$ heißt **nach unten beschränkt**, wenn es eine Zahl $s$ gibt,
sodass $f(x) \geq s$ für alle $x$ aus der Definitionsmenge.

Eine **beschränkte** Funktion ist sowohl nach oben als auch nach unten
beschränkt.
```

Die Kugelbahn ist nach unten beschränkt durch die Tischplatte, es ist also $s =
0~\text{cm}$. Die größte Höhe finden wir am Start-Block, also ist $S =
6~\text{cm}$. Da die Höhenfunktion sowohl nach unten als auch nach oben
beschränkt ist, ist sie beschränkt.

## Symmetrie - Spiegelbahnen

Die Kugelbahn hat uns geholfen, das Konzept der Monotonie zu verstehen. Nun
wollen wir ein neues Unterscheidungsmerkmal kennenlernen: die Symmetrie.
Symmetrie begegnet uns ständig in der Technik. Bauteile sind oft
spiegelsymmetrisch konstruiert, während andere Strukturen punktsymmetrisch sind.
In der Mathematik drücken wir diese Symmetrien durch gerade und ungerade
Funktionen aus.

In diesem Beispiel ist die Kugelbahn symmetrisch nach links weitergebaut worden.
Die Kugel kann vom Start-Block entweder nach links oder rechts rollen. Versehen
wir die Kugelbahn erneut mit einem Koordinatensystem und befindet sich die
y-Achse im Turm des Start-Blocks, so sind die Schienen spiegelbildlich zur
y-Achse. Wir beschreiben diese Kugelbahn durch die Funktionsgleichung

$$h(x)=\begin{cases}
0.25x + 6, \quad & -24 \leq x < 0,\\
-0.25x + 6, \quad & 0 \leq x \leq 24.\\
\end{cases}$$

Außerdem stellen wir fest, dass $h(-x) = h(x)$ gilt.

```{figure} pics/function_marble_track_symmetric.svg
---
width: 75%
name: function_marble_track_symmetric
---
Graph bzw. Plot der Höhenfunktion der Kugel einer y-achsensymmetrischen Kugelbahn
(Quelle: eigene Darstellung; Lizenz: [CC BY-SA
4.0](https://creativecommons.org/licenses/by-sa/4.0))
```

Eine realistische Kugelbahn, die punktsymmetrisch zum Ursprung ist, können wir
in diesem Beispiel nicht konstruieren, da die Tischplatte die Kugelbahn nach
unten beschränkt und negative Höhen nicht zugelassen sind. Aber es gibt viele
technische Systeme, für diese Einschränkung nicht gilt. Anstatt einer Kugelbahn
betrachten wir nun eine Achterbahn, die in hügeliges Gelände gebaut wurde.
Stellen Sie sich vor, die Schienen führen auf der rechten Seite über einen Hügel
und auf der linken Seite durch ein entsprechend tiefes Tal.

```{figure} pics/function_marble_track_odd.svg
---
width: 75%
name: function_marble_track_odd
---
Graph einer zum Ursprung punktsymmetrischen Achterbahn
(Quelle: eigene Darstellung; Lizenz: [CC BY-SA
4.0](https://creativecommons.org/licenses/by-sa/4.0))
```

Diese Achterbahn können wir mathematisch durch die Funktion

$$h(x) = 0.1 x^3$$

beschreiben, wobei das Koordinatensystem so gewählt ist, dass der Nullpunkt in
der Mitte liegt. Die Besonderheit dieser Funktion zeigt sich, wenn wir die
Symmetrie untersuchen:

- Bei $x = 2$ ist die Höhe $h(2) = 0.1 \cdot 2^3 = 0.8~\text{cm}$ (Hügel)
- Bei $x = -2$ ist die Höhe $h(-2) = 0.1 \cdot (-2)^3 = -0.8~\text{cm}$ (Tal)

Allgemein gilt: $h(-x) = 0{,}1 \cdot (-x)^3 = -0{,}1x^3 = -h(x)$.

Die Achterbahn-Kugelbahn veranschaulicht eine fundamentale Eigenschaft vieler
technischer Systeme: Aktion und Reaktion sind betragsmäßig gleich, aber
entgegengesetzt gerichtet.

```{admonition} Was ist ... Symmetrie?
:class: note
**Achsensymmetrie (gerade Funktion)**: Eine Funktion ist achsensymmetrisch zur
y-Achse, wenn $f(-x) = f(x)$ gilt. Der Graph ist spiegelbar an der y-Achse.

**Punktsymmetrie (ungerade Funktion):** Eine Funktion ist punktsymmetrisch zum
Ursprung, wenn $f(-x) = -f(x)$ gilt. Der Graph ist spiegelbar am Ursprung.
```

```{dropdown} Video "Symmetrie - Gerade und ungerade Funktionen" von HM Kompakt
<iframe width="560" height="315"
src="https://www.youtube.com/embed/6zycknHh1-M?si=_tuwbMJSLhUjPLcG"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Beispiele gerade und ungerade Funktionen" von HM Kompakt
<iframe width="560" height="315"
src="https://www.youtube.com/embed/C0kEBDmNrYU?si=See83DQYwZ52pr2J"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Was ist die Achsensymmetrie?" von studiVEMINT
<iframe width="560" height="315"
src="https://www.youtube.com/embed/ertsVp3ANsE?si=OkXFyBbEMuvHv9Il"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Was ist die Punktsymmetrie?" von studiVEMINT
<iframe width="560" height="315"
src="https://www.youtube.com/embed/A3vSYkVmpi0?si=XBxnbtfdvrC1amgz"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Periodizität - Wiederholende Muster

Stellen Sie sich eine Kugelbahn vor, die über eine Reihe identischer Hügel
führt. Diese wiederholende Struktur führt uns zur **Periodizität**.

```{figure} pics/function_marble_track_periodic.svg
---
width: 75%
name: function_marble_track_periodic
---
Graph einer periodischen Kugelbahn mit Periode $\pi$
(Quelle: eigene Darstellung; Lizenz: [CC BY-SA
4.0](https://creativecommons.org/licenses/by-sa/4.0))
```

```{admonition} Was ist ... Periodizität?
:class: note
Eine Funktion $f$ heißt **periodisch** mit der Periode $T > 0$, wenn $f(x + T) =
f(x)$ für alle $x$ aus der Definitionsmenge gilt.

Die kleinste positive Zahl $T$ mit dieser Eigenschaft heißt **Grundperiode**.
```

## Zusammenfassung und Ausblick

Die Eigenschaften von Funktionen - Monotonie, Beschränktheit, Symmetrie und
Periodizität - helfen uns, das Verhalten mathematischer Zusammenhänge zu
verstehen und zu klassifizieren. Anhand unserer Kugelbahn-Beispiele wird
deutlich, wie diese abstrakten Konzepte ganz konkrete praktische Bedeutung
haben. In den nächsten Kapiteln werden wir verschiedene Klassen von Funktionen
kennenlernen und dabei diese Eigenschaften immer wieder aufgreifen.
