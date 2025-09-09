# 7.5 Eigenwerte und Eigenvektoren (2x2-Matrix)

Eigenwerte und Eigenvektoren bieten eine Möglichkeit, schwingende Systeme zu
analysieren. In diesem Kapitel werden die Grundlagen von Eigenwerten und
Eigenvektoren für $2\times 2$-Matrizen erklärt.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie kennen die Definition des Fachbegriffes **Eigenwert** und wissen, was ein
  **Eigenvektor** ist.
* Sie können die Eigenwerte und Eigenvektoren einer $2\times 2$-Matrix
  berechnen.
```

## Was sind Eigenwerte und Eigenvektoren?

Gegeben sei eine quadratische Matrix $\mathbf{A} \in \mathbb{R}^{2 \times 2}$.
Ein Vektor $\vec{v} \neq \vec{0} $ heißt **Eigenvektor** von $\mathbf{A}$, wenn
für einen Skalar $\lambda \in \mathbb{R}$ die folgende Gleichung gilt:

$$\mathbf{A} \vec{v} = \lambda \vec{v}.$$

Der Skalar $\lambda$ wird dabei als **Eigenwert** von $\mathbf{A}$ bezeichnet.
Dies bedeutet, dass die Wirkung der Matrix $\mathbf{A}$ auf den Vektor $\vec{v}$
lediglich eine Streckung oder Stauchung des Vektors um den Faktor $\lambda$
darstellt, ohne dessen Richtung zu verändern.

## Wie werden Eigenwerte berechnet?

Um die Eigenwerte $\lambda$ einer $2 \times 2$-Matrix $\mathbf{A}$ zu berechnen,
muss die **charakteristische Gleichung** gelöst werden. Diese ergibt sich aus
der Determinante der Matrix $\mathbf{A} - \lambda \mathbf{E} $, wobei
$\mathbf{E}$ die Einheitsmatrix ist. Die charakteristische Gleichung lautet:

$$
\det(\mathbf{A} - \lambda \mathbf{E}) = 0.
$$

Für eine Matrix $\mathbf{A} = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$
ergibt sich die charakteristische Gleichung zu:

$$ \det\begin{pmatrix} a - \lambda & b \\ c & d - \lambda \end{pmatrix} = (a -
\lambda)(d - \lambda) - bc = 0. $$

Dies ist eine quadratische Gleichung für $\lambda$, deren Lösungen die
Eigenwerte der Matrix $\mathbf{A}$ sind.

Wir betrachten als Beispiel die $2\times 2$-Matrix

$$
\mathbf{A} = \begin{pmatrix} 6 & 2 \\ 2 & 3 \end{pmatrix}.
$$

Zunächst berechnen wir die Eigenwerte $\lambda$ der Matrix $\mathbf{A}$. Dazu
lösen wir die charakteristische Gleichung:

$$
\det(\mathbf{A} - \lambda \mathbf{E}) = 0.
$$

Die Matrix $\mathbf{A} - \lambda \mathbf{E}$ ergibt sich zu

$$
\mathbf{A} - \lambda \mathbf{E} =
\begin{pmatrix} 6 - \lambda & 2 \\ 2 & 3 - \lambda \end{pmatrix}.
$$

Nun berechnen wir die Determinante dieser Matrix:

$$
\det\begin{pmatrix} 6 - \lambda & 2 \\ 2 & 3 - \lambda \end{pmatrix}
= (6 - \lambda)(3 - \lambda) - 2 \cdot 2.
$$

Damit ergibt die charakteristische Gleichung

$$
(6 - \lambda)(3 - \lambda) - 4 =
18 - 9\lambda + \lambda^2 - 4 = \lambda^2 - 9\lambda + 14 = 0.
$$

Diese quadratische Gleichung lösen wir mit der pq-Formel:

\begin{align*}
\lambda_{1/2}
&= \frac{-(-9)}{2} \pm \sqrt{\frac{81}{4} - 14} \\
&= \frac{9}{2} \pm \sqrt{\frac{81-56}{4}} \\
&= \frac{9}{2} \pm \frac{5}{2}.
\end{align*}

Damit erhalten wir die beiden Eigenwerte

$$
\lambda_{1} = \frac{9}{2} + \frac{5}{2} = 7 \; \text{ und } \;
\lambda_{2} = \frac{9}{2} - \frac{5}{2} = 2.
$$

## Wie werden die Eigenvektoren berechnet?

Ist ein Eigenwert $\lambda$ gefunden, so lassen sich die zugehörigen
Eigenvektoren $\vec{v}$ berechnen, indem das Gleichungssystem

$$
(\mathbf{A} - \lambda \mathbf{E}) \vec{v} = \vec{0}
$$

gelöst wird. Dies führt auf ein lineares Gleichungssystem, dessen Lösungen die
Eigenvektoren der Matrix $\mathbf{A}$ sind.

Wir demonstrieren die Vorgehensweise an dem obige Beispiel. Mit Hilfe der
charakteristischen Gleichung haben wir bereits zu der Matrix

$$\mathbf{A} = \begin{pmatrix} 6 & 2 \\ 2 & 3 \end{pmatrix}.$$

die beiden Eigenwerte $\lambda_1 = 7$ und $\lambda_2 = 2$ gefunden. Zu jedem
dieser beiden Eigenwerte wird nun der dazugehörige Eigenvektor berechnet.

### Eigenvektor zu $\lambda_1 = 7$:

Das Gleichungssystem lautet:

$$
(\mathbf{A} - 7 \mathbf{E}) \vec{v}_{1} = \vec{0}.
$$

Die Matrix $\mathbf{A} - 7 \mathbf{E}$ ist:

$$
\mathbf{A} - 7 \mathbf{E} =
\begin{pmatrix} 6 - 7 & 2 \\ 2 & 3 - 7 \end{pmatrix} =
\begin{pmatrix} -1 & 2 \\ 2 & -4 \end{pmatrix}.
$$

Somit müssen wir das lineare Gleichungssystem

$$
\begin{pmatrix} -1 & 2 \\ 2 & -4 \end{pmatrix} \cdot
\begin{pmatrix} x \\ y \end{pmatrix} =
\begin{pmatrix} 0 \\ 0 \end{pmatrix}
$$

lösen. Dies ergibt zwei Gleichungen:

\begin{align*}
-1 x + 2 y &= 0 \quad \text{(I)}\\
2 x - 4 y &= 0 \quad \text{(II)}
\end{align*}

Gleichung (I) lösen wir nach $x$ auf:

$$x = 2 y.$$

Setzen wir dies in Gleichung (II) ein:

$$
2 (2 y) - 4 y = 0 \quad \Rightarrow \quad 4 y - 4 y = 0.
$$

Dies ist immer erfüllt, wir haben unendlich viele Lösungen. Daher wählen wir
einen Parameter $s$ für $y$, also

$$y = s,$$

was $x = 2s$ ergibt. Die Menge aller Eigenvektoren zu $\lambda_1 = 7$ ist also

$$
\vec{v}_1 = s\cdot\begin{pmatrix} 2 \\ 1 \end{pmatrix}.
$$

### Eigenvektor zu $\lambda_2 = 2$:

Das Gleichungssystem lautet:

$$(\mathbf{A} - 2 \mathbf{E}) \vec{v}_{2} = \vec{0}.$$

Die Matrix $\mathbf{A} - 2 \mathbf{E}$ ist:

$$
\mathbf{A} - 2 \mathbf{E} =
\begin{pmatrix} 6 - 2 & 2 \\ 2 & 3 - 2 \end{pmatrix} =
\begin{pmatrix} 4 & 2 \\ 2 & 1 \end{pmatrix}.
$$

Das lineare Gleichungssystem lautet

$$
\begin{pmatrix} 4 & 2 \\ 2 & 1 \end{pmatrix} \cdot
\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}.
$$

Dies ergibt zwei Gleichungen:

\begin{align*}
4 x + 2 y &= 0 \quad \text{(I)}\\
2 x + 1 y &= 0 \quad \text{(II)}
\end{align*}

Gleichung (II) lösen wir nach $y$ auf:

$$y = -2 x.$$

Setzen wir dies in Gleichung (I) ein:

$$
4 x + 2 (-2 x) = 0 \quad \Rightarrow \quad 4 x - 4 x = 0.
$$

Dies ist immer erfüllt, daher wählen wir $x = t$, was $y = -2 t$ ergibt.

Der Eigenvektor zu $\lambda_2 = 2$ ist also

$$
\vec{v}_2 = t\cdot\begin{pmatrix} 1 \\ -2 \end{pmatrix}.
$$

In dem folgenden Video wird ein weiteres Beispiel gerechnet.

```{dropdown} Video "Eigenwerte, Eigenvektoren 2x2" von Daniel Jung
<iframe width="560" height="315" src="https://www.youtube.com/embed/Rr0aa7oo5u8"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

In diesem Kapitel haben wir gelernt, was Eigenwerte und Eigenvektoren sind.
Diese Definition ist auch für größere quadratische Matrizen gültig, nur die
Berechnung wird etwas länglicher. Das sehen wir uns im nächsten Kapitel an.
