# 1.1 Zahlen

Mit zunehmender Komplexität unseres Alltags wächst auch die Komplexität der
Zahlen, die wir benötigen, um ihn zu beschreiben. Bereits im Kindergarten lernen
wir, mit Zahlen bis zehn umzugehen, um beispielsweise unser Alter oder die
Anzahl der Gäste bei einem Geburtstag zu bestimmen. Hierbei handelt es sich um
*natürliche Zahlen*, die grundlegend für das Zählen sind.

Wenn wir jedoch in den Bereich der Finanzen eintauchen, erweitert sich unser
Zahlenverständnis. Wenn wir beispielsweise mehr Geld ausgeben, als wir zur
Verfügung haben, benötigen wir *ganze Zahlen*, um einen negativen Kontostand
darzustellen. Beim Kauf eines Handys für 500 EUR, das wir in 24 Monatsraten
abzahlen, nutzen wir *rationale Zahlen*. Die Monatsrate berechnet als 500/24 EUR
illustriert dies anschaulich.

Technische und naturwissenschaftliche Beschreibungen erfordern oft den Gebrauch
von *reellen Zahlen*. Ein klassisches Beispiel ist die Länge der Diagonale eines
DIN A4-Blattes, die mit $\sqrt{297^2 + 210^2}$ mm berechnet wird und somit eine
reelle Zahl ist.

## Lernziele

```{admonition} Lernziele
:class: attention
* Sie kennen die
  * **natürlichen Zahlen** $\mathbb{N}$,
  * **ganzen Zahlen** $\mathbb{Z}$,
  * **rationalen Zahlen** $\mathbb{Q}$,
  * **reellen Zahlen** $\mathbb{R}$.
* Sie kennen die Einbettung der Zahlen
  $\mathbb{N}\subset\mathbb{Z}\subset\mathbb{Q}\subset\mathbb{R}$.
```

## Natürliche Zahlen

Die **natürlichen Zahlen** sind die Zahlen, mit denen wir als Kinder das Zählen
lernen. Wir haben einen Bruder, sind zwei Jahre alt und mit den Eltern besteht
die Familie aus drei Personen. Die Zahlen haben ihre eigenen Zeichen und werden
geschrieben als

\begin{equation*}
1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, \dots
\end{equation*}

Manchmal wird auch die Zahl $0$ (Null) zu den natürlichen Zahlen gezählt. Die
Menge der natürlichen Zahlen bezeichnen wir mit dem Symbol $\mathbb{N}$. In dieser Vorlesung nutezn wir die Konvention

\begin{equation*}
\mathbb{N} = \{0, 1, 2, 3, 4, 5, \dots\}.
\end{equation*}

In der Schule werden die natürlichen Zahlen oft als **Zahlenstrahl**
dargestellt. Das soll den Schülerinnen und Schülern helfen zu verstehen, dass
die natürlichen Zahlen eine **Ordnung** haben, also beispielsweise die Aussage
"3 ist kleiner als 7" gilt (in mathematischer Notation: $3 < 7$). Auch die
Addition und die Multiplikation können so intuitiv erklärt werden.

```{figure} pics/fig01_line_number_N.svg
---
width: 100%
name: fig01_line_number_N
---
Zahlenstrahl der natürlichen Zahlen (Quelle: eigene Darstellung; Lizenz [CC 
BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/))
```

## Ganze Zahlen

Für die Gleichung $x + 3 = 2$ finden wir innerhalb der natürlichen Zahlen keine
Lösung. Wir müssen die natürlichen Zahlen erweitern, um diese Gleichung lösen zu
können. Wir bezeichnen die Menge der Zahlen

\begin{equation*} \mathbb{Z} = \{\ldots, -3, -2, -1, 0, 1, 2, 3, 4, \ldots\}
\end{equation*}

als **ganze Zahlen**.

Die ganzen Zahlen werden auch häufig als **Zahlengerade** visualisiert.

```{figure} pics/fig01_line_number_Z.svg
---
width: 100%
name: fig01_line_number_Z
---
Zahlengerade der ganzen Zahlen (Quelle: eigene Darstellung; Lizenz [CC 
BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/))
```

## Rationale Zahlen

Auch bei den ganzen Zahlen lassen sich nicht alle Gleichungen lösen, so dass das
Ergebnis wieder eine ganze Zahl ist. Beispielsweise finden wir keine ganze Zahl,
so dass $2\cdot x = 7$ gilt. Daher führen wir als Erweiterung der ganzen Zahlen
die **rationalen Zahlen** ein. Diese Zahlen können wir nicht so übersichtlich
als Menge schreiben wie die natürlichen und ganzen Zahlen. Stattdessen legen wir
fest:

Eine rationale Zahl ist eine Zahl, die als Bruch bzw. Quotient zweier ganzer
Zahlen dargestellt werden kann, wobei nicht durch Null geteilt werden darf. Wir
bezeichnen die Menge der rationalen Zahlen mit dem Symbol $\mathbb{Q}$.

Es gibt zwei Schreibweisen von rationalen Zahlen:

1. als Bruch (Beispiele $\frac{3}{8}$ oder $\frac{2}{3}$) oder
2. als Fließkommazahl (Beispiele $0.375$ oder $0.\bar{6}$).

```{figure} pics/fig01_line_number_Q.svg
---
width: 100%
name: fig01_line_number_Q
---
Zahlengerade mit rationalen Zahlen; zwischen zwei rationalen Zahlen liegen
unendlich viele weitere rationale Zahlen, drei rationale Zahlen sind hier
exemplarisch in blau eingezeichnet (Quelle: eigene Darstellung; Lizenz [CC 
BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/))
```

## Reelle Zahlen

Welche Gleichung lässt sich nicht mit den rationalen Zahlen lösen? Für die
Gleichung $x^2 = 2$ finden wir keine rationale Zahl als Lösung. Die Zahl
$1.41421$ kommt dem Ergebnis schon recht nahe, dann $1.41421^2 = 1.99998992$,
aber sie ist keine exakte Lösung, sondern nur eine Näherung an die exakte
Lösung. Wir könnten immer mehr Nachkommastellen dazu nehmen

\begin{equation*} 1.414213562 \ldots, \end{equation*}

würden aber beim Quadrieren nie $2$ erhalten. Die exakte Lösung der quadratischen
Gleichung $x^2 =2$ bezeichnen wir mit dem Symbol $\sqrt{2}$ (und tatsächlich ist
auch $-\sqrt{2}$ eine weitere Lösung dieser Gleichung). Zahlen, die nicht
rational sind, werden **irrational** genannt. Weitere Beispiele für irrationale Zahlen sind die Kreiszahl

\begin{equation*}
\pi =3.14159\,26535\,89793\,23846\,26433\,83279\,50288\,41971\,69399\,37510\,\dots
\end{equation*}

oder die Eulersche Zahl

\begin{equation*}
e = 2.71828 \, 18284 \, 59045 \, 23536 \, 02874 \, 71352 \, 66249 \, 77572 \, 47093 \, 69995 \, \dots .
\end{equation*}

Irrationale Zahlen werden selten alleine betrachtet, weshalb es auch kein
mathematisches Symbol für sie gibt. Viel gebräuchlicher ist es, die rationalen
und irrationalen Zahlen zusammen zu betrachten. Beide Zahlenarten zusammen
werden als **reelle Zahlen** bezeichnet und mit dem mathematischen Symbol
$\mathbb{R}$ abgekürzt.

```{figure} pics/fig01_line_number_R.svg
---
width: 100%
name: fig01_line_number_R
---
Zahlengerade mit reellen Zahlen (Quelle: eigene Darstellung; Lizenz [CC 
BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/))
```

## Einbettung der Zahlen

Die folgende Grafik veranschaulicht, wie die Zahlen immer weiter von den
natürlichen Zahlen zu den ganzen Zahlen, den rationalen Zahlen und letztendlich
den reellen Zahlen erweitert werden. Die Erweiterungen werden immer dann
notwendig, wenn eine Gleichung nicht mit dieser Art von Zahlen gelöst werden
kann. Und wir werden in einem späteren Kapitel sehen, dass bei den reellen
Zahlen noch nicht Schluss ist, denn wir möchten auch eine Gleichung wie
beispielsweise $x^2 = -1$ lösen können. Das wird uns zu den **komplexen Zahlen**
führen.

```{figure} pics/fig01_number_embedding_DE.svg
---
width: 100%
name: fig01_number_embedding_DE
---
Einbettung der Zahlen
$\mathbb{N}\subset\mathbb{Z}\subset\mathbb{Q}\subset\mathbb{R}$ (Quelle: eigene
Darstellung; Lizenz [CC BY-NC-SA
4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/))
```

```{dropdown} Video "Wichtige Mengen (Teil 1)" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/GBdeyJy7iKA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Wichtige Mengen (Teil 2)" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/aCbxnjveEwA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Zahlenmengen" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/c3Tvoew31aU?si=tXE16_39GxzPzlZ8"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media;
gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen>
</iframe>
```

## Zusammenfassung und Ausblick

In diesem Kapitel haben wir uns mit den verschiedenen Zahlenarten beschäftigt.
Im Maschinenbau betrachten wir meistens reelle Zahlen, um technische Anwendungen
zu beschreiben. In der Programmierung werden hauptsächlich ganze Zahlen und
rationale Zahlen in Form von Fließkommazahlen benutzt. Die sogenannten komplexen
Zahlen werden wir später behandeln.
