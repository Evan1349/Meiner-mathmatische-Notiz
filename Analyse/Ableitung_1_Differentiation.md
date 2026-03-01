# Ableitung Und Differentiation
---
![Ableitung Visualisierung](../Resources/Ableitung_Differentiation.png)
> Wie weiß man, wie sich eine Funktion an einem Punkt verändert?
> - Die Lösung ist die Steigung der Tangente.

> Aber wie berechnet man die Steigung an einem einzigen Punkt?
> - Wir nehmen zwei Punkte und berechnen die Steigung der Sekante.
> - Dann lassen wir h → 0 (Limit), sodass die Sekante zur Tangente wird.
> - Das Ergebnis ist die Ableitung f′(x).
> - Die Ableitung ist der Übergang von der diskreten zur infinitesimalen Betrachtung.

---
## 1. Definition
**Definition:** 
Die Ableitung $f'(x)$ gibt die *momentane Änderungsrate* (Steigung) einer Funktion an einer Stelle $x$ an.

>Die momentane Änderungsrate entspricht der Momentangeschwindigkeit eines Objekts zu einem ganz bestimmten Zeitpunkt.

**Differenzierbarkeit:**
Eine Funktion ist an einer Stelle $x_0$ differenzierbar, wenn der Differenzenquotient einen endlichen Grenzwert besitzt. Die Differenzierbarkeit impliziert zudem, dass der Funktionsgraph keine Unterbrechungen hat, was als **Stetigkeit** bezeichnet wird.

*z.B :*
$f(x) = |x|$
> Die Betragsfunktion ist an der Stelle x=0 zwar stetig, aber nicht differenzierbar, da der Graph dort einen Knick aufweist.


>strukturelle Zusammenfassung

## 2. Satz 

*1. Differentialquotient*

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

*2. Potenzfunktion*

- $f(x) = ax^n + b \implies f'(x) = a \cdot n \cdot x^{n-1}$

*3. Trigonometrische Funktionen*

- $(\sin x)' = \cos x$
- $(\cos x)' = -\sin x$

*4. Exponentialfunktion*

- $(e^x)' = e^x$

*5. Die Konstanten*

- $f(c) = c \implies f'(x) = 0$


>strukturelle Zusammenfassung
---

## 3. Beispiel

**(1) Differentialquotient**

Gegeben sei $f(x) = 5x^3+2x^2+1$. Berechnen Sie die Ableitung der Funktion $f(x)$ mithilfe der Definition: $$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

a. $$f(x+h) = 5(x+h)^3+2(x+h)^2+1$$ 

$$=5x^3+2x^2+15x^2h+4xh+15xh^2+5h^3+2h^2+1$$

$$=(5x^3+2x^2+1)+h(15x^2+4x+5h^2+15xh+2h)$$

b. 

$$ f(x+h)- f(x) = h(15x^2+4x+5h^2+15xh+2h)$$

c. 

$$\frac{f(x+h) - f(x)}{h} = (15x^2+4x+5h^2+15xh+2h)$$

d. Wenn $ h \to 0$, dass $h=0$ die Funktion gesetzen $\to$ Setzt man $h=0$ in den Ausdruck ein, erhält man: $15x^2+4x$.

e. Ergebnis: 

$$f'(x) = 15x^2 + 4x \quad \text{(Anwendung der Regel: } f(x) = ax^n \implies f'(x) = a \cdot n \cdot x^{n-1} \text{)}$$

---

**(2) Potenzfunktion**

Gegeben sei $f(x) = 7x^5+x^4+10x^3+2x^2+9x+10$. Berechnen Sie die Ableitung.

$$f'(x) = 35x^4+4x^3+30x^2+4x+9$$

---

**(3) Trigonometrische Funktionen (Ableitung der Cosinusfunktion)**

Gegeben sei $f(x) = \cos(x)$. Berechnen Sie die Ableitung der Funktion $f(x)$ mithilfe der Definition:$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

a. Einsetzen der Funktion:

$$f'(x) = \lim_{h \to 0} \frac{\cos(x+h) - \cos(x)}{h}$$

>Additionstheorem:

$$\cos(x + h) = \cos(x)\cos(h) - \sin(x)\sin(h)$$

b. Anwendung des Additionstheorems:

$$f'(x) = \lim_{h \to 0} \frac{[\cos(x)\cos(h) - \sin(x)\sin(h)] - \cos(x)}{h}$$

c. Umstellen und Ausklammern von $\cos(x)$:

$$f'(x) = \lim_{h \to 0} \frac{\cos(x)(\cos(h) - 1) - \sin(x)\sin(h)}{h}$$

d. Aufteilen in zwei Grenzwerte:

$$f'(x) = \cos(x) \cdot \lim_{h \to 0} \frac{\cos(h) - 1}{h} - \sin(x) \cdot \lim_{h \to 0} \frac{\sin(h)}{h}$$

Wichtige Grenzwerte für Winkelfunktionen:

$\lim_{h \to 0} \frac{\sin(h)}{h} = 1$,
$\lim_{h \to 0} \frac{\cos(h) - 1}{h} = 0$

>Bogenmaß vorausgesetzt

e. Einsetzen der Grenzwerte:

$$f'(x) = \cos(x) \cdot (0) - \sin(x) \cdot (1)$$

f. Ergebnis:

$$f'(x) = - \sin(x)$$


**4. Die natürliche Exponentialfunktion (Ableitung von $e^x$)**

Gegeben sei die Funktion $f(x) = e^x$. Wir berechnen die Ableitung mithilfe des Differentialquotienten:$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

a. Einsetzen der Funktion:

$$f'(x) = \lim_{h \to 0} \frac{e^{x+h} - e^x}{h}$$

b. Anwendung der Potenzgesetze ($e^{x+h} = e^x \cdot e^h$):

$$f'(x) = \lim_{h \to 0} \frac{e^x \cdot e^h - e^x}{h}$$

c. Ausklammern von $e^x$:

$$f'(x) = \lim_{h \to 0} \frac{e^x (e^h - 1)}{h}$$

d. Da $e^x$ nicht von $h$ abhängt, ziehen wir es vor den Grenzwert:

$$f'(x) = e^x \cdot \lim_{h \to 0} \frac{e^h - 1}{h}$$

Definition der Eulerschen Zahl ($e$):Die Zahl $e$ ist genau so definiert, dass dieser spezifische Grenzwert $1$ ergibt:

$$\lim_{h \to 0} \frac{e^h - 1}{h} = 1$$

e. Einsetzen des Grenzwerts:

$$f'(x) = e^x \cdot 1$$

f. Ergebnis:

$$f'(x) = e^x$$

*Zusammenfassung:*
Die Funktion $f(x) = e^x$ ist ihre eigene Ableitung. Das bedeutet, dass zu jedem Zeitpunkt die Steigung der Kurve exakt ihrem aktuellen Wert entspricht.

>strukturelle Zusammenfassung