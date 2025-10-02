# 2.3 Potenzfunktionen und Polynome

## Lernziele

```{admonition} Lernziele Polynome
:class: goals
* Sie wissen, was eine **Potenzfunktion** ist ($f(x) = a \cdot x^n$) und kennen
  ihr Verhalten für verschiedene Exponenten.
* Sie kennen **lineare Funktionen** und können deren Graphen skizzieren. Sie
  wissen, was **Steigung** und **Achsenabschnitt** bedeuten.
* Sie kennen **quadratische Funktionen** und können deren Graphen skizzieren.
  Sie wissen, was der **Scheitelpunkt** ist.
* Sie wissen, dass ein **Polynom** eine Summe von Potenzfunktionen ist und
  kennen die Begriffe **Grad** und **Koeffizienten**.
```

## Potenzfunktionen

Unsere Kugelbahn aus dem letzten Kapitel hatte eine gerade, schräge Schiene. Die
Höhenfunktion war linear: $h(x) = -\frac{1}{4}x + 6$. Aber was wäre, wenn wir
eine gekrümmte Schiene verwenden? Oder eine Rampe, die immer steiler wird? Um
solche Bahnen mathematisch zu beschreiben, benötigen wir Potenzfunktionen.

Stellen wir uns verschiedene Kugelbahnen mit unterschiedlichen Schienen-Profilen
vor. Eine Möglichkeit wäre ein parabolisches Profil, bei dem die Höhe mit dem
Quadrat der Position zusammenhängt. Eine andere könnte einer Wurzelfunktion
folgen, bei der die Höhe langsamer abnimmt. All diese Schienen-Profile lassen
sich durch Potenzfunktionen beschreiben.

```{admonition} Was ist ... eine Potenzfunktion?
:class: note
Eine **Potenzfunktion** ist eine Funktion der Form

$$f(x) = a \cdot x^n,$$

wobei $a$ ein Koeffizient (meist $a \neq 0$) und $n$ der **Exponent** ist. Der
Exponent $n$ kann eine beliebige reelle Zahl sein.
```

Der Koeffizient $a$ bestimmt, wie steil oder flach die Funktion verläuft und ob
sie nach oben oder unten zeigt. Der Exponent $n$ bestimmt die grundlegende Form
der Funktion. Betrachten wir einige wichtige Fälle:

**Positive ganzzahlige Exponenten ($n = 1, 2, 3, \ldots$):**

* Für $n=1$ erhalten wir die einfachste Form: $f(x) = a \cdot x$. Dies ist eine
Gerade durch den Ursprung.
* Für $n=2$ bekommen wir eine Parabel: $f(x) = a \cdot x^2$. Je nachdem, ob $a$
positiv oder negativ ist, öffnet sich die Parabel nach oben oder unten.
* Für $n=3$ ergibt sich eine kubische Funktion: $f(x) = a \cdot x^3$. Diese hat
einen charakteristischen S-förmigen Verlauf und wechselt ihr Krümmungsverhalten.

**Negative Exponenten ($n = -1, -2, -3, \ldots$):**

Für negative Exponenten können wir die Potenzfunktion auch als Bruch schreiben:
  
  $$f(x) = a \cdot x^{-n} = \frac{a}{x^n}.$$

Diese Funktionen sind bei $x=0$ nicht definiert und nähern sich für $x \to 0$
dem Wert $\pm\infty$. Ein Beispiel ist die Hyperbel $f(x) = \frac{1}{x}$
(entspricht $n=-1$).

**Rationale Exponenten (Wurzelfunktionen):**

Ist der Exponent ein Bruch, beispielsweise $n = \frac{1}{2}$​, so erhalten wir
Wurzelfunktionen mit der Definitionsmenge $D = [0; \infty)$:

$$f(x) = x^{\frac{1}{2}} = \sqrt{x}.$$

Eine Kugelbahn mit einer Wurzelfunktion als Profil würde am Anfang steil
abfallen und dann immer flacher werden.

## Lineare Funktionen

Im letzten Kapitel haben wir bereits eine lineare Funktion kennengelernt: Die
Höhenfunktion unserer geraden Kugelbahn war $h(x) = -\frac{1}{4}x + 6$. Diese
Funktion enthält neben der Potenzfunktionen mit dem Exponenten $n=1$ noch einen
zusätzlichen konstanten Term.

Lineare Funktionen sind die einfachsten nichtkonstanten Funktionen und spielen
in der Mathematik und ihren Anwendungen eine zentrale Rolle. Ihr Graph ist immer
eine Gerade, was sie besonders übersichtlich und vorhersagbar macht.

```{admonition} Was ist ... eine lineare Funktion?
:class: note
Eine **lineare Funktion** ist eine Funktion der Form

$$f(x) = m \cdot x + b,$$

wobei $m$ die **Steigung** und $b$ der **Achsenabschnitt** (oder
y-Achsenabschnitt) ist. Beide Parameter $m$ und $b$ sind reelle Zahlen.
```

Die Steigung gibt an, wie stark die Gerade ansteigt oder abfällt. Bei unserer
Kugelbahn war $m = -\frac{1}{4}$​, die Schiene fiel also. Je größer der Betrag
von $m$ ist, desto steiler verläuft die Gerade:

* Ist $m > 0$, dann steigt die Gerade (monoton wachsende Funktion).
* Ist $m < 0$, dann fällt die Gerade (monoton fallende Funktion).
* Ist $m = 0$, dann ist die Funktion konstant (horizontale Gerade).

Die Steigung lässt sich geometrisch über das sogenannte Steigungsdreieck
bestimmen. Wenn wir von einem Punkt $(x_1, y_1)$ zu einem anderen Punkt $(x_2,
y_2)$ auf der Geraden gehen, dann gilt:

$$m = \frac{\Delta y}{\Delta x} = \frac{y_2 - y_1}{x_2 - x_1}​​.$$

Bei unserer Kugelbahn bedeutet eine Steigung von $m=-\frac{1}{4}$: Wenn die
Kugel 4 cm nach rechts rollt, sinkt sie um 1 cm.

Der Achsenabschnitt ist der y-Wert, bei dem die Gerade die y-Achse schneidet.
Setzen wir $x = 0$ in die Funktionsgleichung ein, erhalten wir:

$$f(0) = m \cdot 0 + b = b.$$

Bei unserer Kugelbahn war $b = 6$ cm. Das ist genau die Starthöhe am
Start-Stein, der sich bei $x = 0$ befindet.

```{dropdown} Video "Lineare Funktion" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/RDdLbEq-_v0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Lineare Funktion zeichnen" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/50E1gIunhzE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Quadratische Funktionen

Während die lineare Funktion eine gerade Schiene beschreibt, benötigen wir für
gekrümmte Kugelbahnen komplexere Funktionen. Die einfachste Möglichkeit, eine
Krümmung zu erzeugen, ist die quadratische Funktion. Ihr charakteristischer Term
ist $ax^2$, eine Potenzfunktion mit Exponent $n=2$.

Stellen wir uns eine Kugelbahn vor, die nicht einfach nur gerade abfällt,
sondern deren Gefälle sich kontinuierlich ändert. Eine solche Bahn könnte am
Anfang flach beginnen und dann immer steiler werden oder umgekehrt. Genau dieses
Verhalten lässt sich durch quadratische Funktionen beschreiben.

```{admonition} Was ist ... eine quadratische Funktion?
:class: note
Eine **quadratische Funktion** ist eine Funktion der Form

$$f(x) = ax^2 + bx + c,$$

wobei $a$, $b$ und $c$ reelle Zahlen sind und $a \neq 0$ gilt. Der Parameter $a$
heißt **Leitkoeffizient**.
```

Der Graph einer quadratischen Funktion ist eine **Parabel**. Die Form und Lage
der Parabel wird durch drei Parameter bestimmt:

* Der Leitkoeffizient $a$ bestimmt, ob die Parabel nach oben ($a > 0$) oder nach
  unten ($a < 0$) geöffnet ist. Je größer der Betrag von $a$, desto schmaler ist
  die Parabel.
* Die Parameter $b$ und $c$ bestimmen die Position der Parabel im
  Koordinatensystem.

Der wichtigste Punkt einer Parabel ist ihr **Scheitelpunkt**. Das ist der
tiefste Punkt bei nach oben geöffneten Parabeln oder der höchste Punkt bei nach
unten geöffneten Parabeln.

Bei einem parabolischen Kugelbahn-Profil wäre der Scheitelpunkt der tiefste
Punkt der Bahn. An diesem Punkt ist die Steigung der Bahn null; die Kugel rollt
für einen kurzen Moment weder bergauf noch bergab.

Es gibt zwei gängige Darstellungsformen für quadratische Funktionen, die jeweils
unterschiedliche Informationen liefern:

* Normalform: $f(x) = ax^2 + bx + c$
* Scheitelpunktform: $f(x) = a(x - x_S)^2 + y_S$

Die Normalform zeigt direkt den y-Achsenabschnitt $c$. Die Scheitelpunktform
zeigt direkt den Scheitelpunkt $S = (x_S, y_S)$. Die Koordinaten des
Scheitelpunkts lassen sich auch aus der Normalform berechnen:

$$x_S = -\frac{b}{2a} \quad \text{und} \quad y_S = f(x_S).$$

Eine wichtige Frage bei Kugelbahnen ist: Wo erreicht die Kugel die Tischebene?
Mathematisch entspricht das der Frage nach den **Nullstellen** der Funktion,
also den Stellen, an denen $f(x) = 0$ gilt.

Für quadratische Funktionen in der speziellen Form $f(x) = x^2 + px + q$ gibt es
die pq-Formel, die wir bereits aus Kapitel 1 kennen:

$$x_{1,2} = -\frac{p}{2} \pm \sqrt{\left(\frac{p}{2}\right)^2 - q}.$$

Ist die quadratische Funktion in der allgemeinen Form $f(x) = ax^2 + bx + c$
gegeben, können wir entweder zunächst durch $a$ teilen oder die abc-Formel (oder
Mitternachtsformel) verwenden:

$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}.$$

Der Ausdruck unter der Wurzel $D = b^2 - 4ac$ bzw. $D =
\left(\frac{p}{2}\right)^2 - q$ bei der pq-Formel heißt **Diskriminante** und
entscheidet über die Anzahl der Nullstellen:

* $D > 0$: zwei verschiedene Nullstellen (die Parabel schneidet die x-Achse zweimal)
* $D = 0$: eine Nullstelle (die Parabel berührt die x-Achse im Scheitelpunkt)
* $D < 0$: keine reellen Nullstellen (die Parabel schneidet die x-Achse nicht)

Um eine Parabel zu skizzieren, bestimmen wir:

1. die Öffnungsrichtung (Vorzeichen von $a$)
2. den Scheitelpunkt $S = (x_S, y_S)$
3. die Nullstellen (falls vorhanden)
4. optional: den y-Achsenabschnitt $f(0)=c$

Diese wenigen Punkte genügen meist, um die Parabel qualitativ korrekt zu
zeichnen.

Quadratische Funktionen sind bereits deutlich vielseitiger als lineare
Funktionen. Im nächsten Abschnitt werden wir sehen, wie wir durch Kombination
mehrerer Potenzfunktionen noch komplexere Kugelbahn-Profile beschreiben können.

```{dropdown} Video "Parabel aufstellen" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/QGwUeoV7NEg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "pq-Formel anwenden" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/IM1WtnTYJK4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Parabel zeichnen" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/RjhXB1aBDCM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Polynome

In den vorherigen Abschnitten haben wir lineare und quadratische Funktionen
kennengelernt. Beide haben eine gemeinsame Struktur: Sie bestehen aus Summen von
Potenzfunktionen und konstanten Termen. Diese Klasse von Funktionen hat einen
eigenen Namen: **Polynome**.

Stellen wir uns eine komplexe Kugelbahn vor, die verschiedene Abschnitte
kombiniert: erst eine flache Strecke, dann eine gekrümmte Passage, vielleicht
noch eine steilere Kurve. Solche komplizierten Höhenprofile lassen sich durch
Polynome beschreiben, indem wir mehrere Potenzfunktionen mit unterschiedlichen
Exponenten addieren.

```{admonition} Was ist ... ein Polynom?
:class: note
Ein **Polynom** ist eine Funktion der Form

$$p(x) = a_n x^n + a_{n-1} x^{n-1} + \ldots + a_2 x^2 + a_1 x + a_0,$$

wobei $a_0, a_1, \ldots, a_n$ reelle Zahlen sind, die **Koeffizienten** genannt
werden. Die höchste vorkommende Potenz $n$ (mit $a_n \neq 0$) heißt **Grad** des
Polynoms. Der Koeffizient $a_n$ beim höchsten Exponenten heißt
**Leitkoeffizient**.
```

Ein Polynom ist also nichts anderes als eine Summe von Potenzfunktionen $a_k
\cdot x^k$ mit verschiedenen Exponenten $k$, plus einem konstanten Term $a_0$​.

Beispiele:

* $f(x) = 5x + 3$ ist ein Polynom vom Grad 1 (lineare Funktion)
* $g(x) = 2x^2 - 3x + 1$ ist ein Polynom vom Grad 2 (quadratische Funktion)
* $h(x) = x^3 - 4x^2 + x - 7$ ist ein Polynom vom Grad 3 (kubisches Polynom)
* $k(x) = -0.5x^4 + 2x^3 - x + 5$ ist ein Polynom vom Grad 4

Die Koeffizienten $a_0, a_1, \ldots, a_n$ bestimmen die genaue Form der Kurve.
Besonders wichtig ist der Leitkoeffizient $a_n$: Er entscheidet, wie sich das
Polynom für sehr große oder sehr kleine x-Werte verhält:

* Ist $n$ gerade und $a_n > 0$: Der Graph geht für $x \to \pm\infty$ nach oben.
* Ist $n$ gerade und $a_n < 0$: Der Graph geht für $x \to \pm\infty$ nach unten.
* Ist $n$ ungerade und $a_n > 0$: Der Graph kommt von unten links und geht nach
  oben rechts.
* Ist $n$ ungerade und $a_n < 0$: Der Graph kommt von oben links und geht nach
  unten rechts.

Für unsere Kugelbahn bedeutet das: Je komplexer das Höhenprofil, desto höher der
Grad des benötigten Polynoms. Eine einfache gerade Schiene benötigt nur Grad 1,
eine parabolische Rampe Grad 2, und eine Kugelbahn mit mehreren Hügeln und
Tälern könnte ein Polynom höheren Grades erfordern.

Beispiel: Eine Kugelbahn mit dem Höhenprofil

$$h(x) = -0.001x^3 + 0.05x^2 - 0.5x + 6$$

ist ein Polynom vom Grad 3. Diese Funktion beschreibt eine Bahn, die zunächst
abfällt, dann vielleicht einen flachen Bereich durchläuft und schließlich wieder
steiler wird.

Polynome verallgemeinern die Funktionen, die wir bereits kennengelernt haben.
Potenzfunktionen sind Polynome mit nur einem Term. Lineare Funktionen sind
Polynome vom Grad 1. Quadratische Funktionen sind Polynome vom Grad 2.

```{dropdown} Video "Polynome" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/bUSOKjICFqQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

Aus Potenzfunktionen bauen wir Polynome zusammen. In den folgenden Kapiteln
werden wir weitere wichtige Funktionsklassen kennenlernen, die über Polynome
hinausgehen: Exponential-, Logarithmus- und trigonometrische Funktionen.
