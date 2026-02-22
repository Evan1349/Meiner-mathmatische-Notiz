# Hauptkomponentenanalyse
---
![Hauptkomponentenanalyse Visualisierung](../Resources/PCA.png)
---
## 1. Definition und Ziel
**Definition:** Die **Hauptkomponentenanalyse(PCA)** ist ein Verfahren der multivariaten Statistik, das zur *Dimensionsreduktion* verwendet wird.

**Hauptziel:** Um Informationen aus einem großen Datensatz zu vereinfachen, wobei sie die wichtigsten Merkmale enthalten blieben. Dadurch können die Daten das *Rauschen* reduzieren. 

## 2. Die Formel und Schritt-für-Schritt-Anleitung

### A. **Zentrierung der Daten** (Vorbereitung)
Zuerst werden die Daten zentriert, um den *Mittelpunkt* der Datenwolke in den Ursprung zu verschieben.

$$X_{\text{zentriert}} = X - \bar{x}$$

### B. **Kovarianzmatrix** (Statistik)
Danach berechnen wir die *Kovarianzmatrix*, um die Korrelationen zwischen den Variablen zu verstehen.

$$\Sigma = \frac{1}{n-1} X^T X$$

### C. **Charakteristische Gleichung** (Analyse)
Um *Eigenwerte* ($\lambda$) zu finden, berechnen wir det().

$$\det(\Sigma - \lambda I) = 0$$

### D. **Transformation**
Zuletzt *transformieren* wir die ursprüngliche Matrix in den neuen Merkmalsraum.

$$Y = X \cdot V$$

## 3. Beispiel
* **Gegeben sind vier Punkte: a(0, -1), b(0, 1), c(2, 1), d(2, 3)**

### Schritt A: Zentrierung der Daten
*Bestimmen $\bar{x}$*

$$\bar{x} = (1, 1)$$

*Daten (zentriert)*

$$D_{\text{martrix}} - \bar{x} = D_{\text{zentriert}}$$

$$D_{\text{zentriert}} = \begin{bmatrix} -1 & -2 \\-1 & 0 \\ 1 & 0 \\ 1 & 2 \end{bmatrix}$$

### Schritt B: Kovarianzmatrix berechnen

$$\Sigma = \begin{bmatrix} 4/3 & 4/3 \\ 4/3 & 8/3 \end{bmatrix}$$

### Schritt C: Charakteristische Gleichung lösen

$$\det(\Sigma - \lambda I) = \lambda^2 - 4\lambda + \frac{16}{9} = 0$$

**Ergebnisse für Eigenwerte**

*nutzen*: 
*$$\lambda = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$*


$$\lambda = 2 \pm \frac{2}{3}\sqrt{5}$$

### Schritt D: Transformation

**Setzen Sie $\lambda$ in $\det(X - \lambda I) = 0$ ein.**

---
*i. $$\Lambda = 2 + \frac{2}{3}\sqrt{5}$$*

$$\begin{bmatrix} 4/3-\Lambda & 4/3 \\ 4/3 & 8/3-\Lambda \end{bmatrix} \cdot \begin{bmatrix}V_1 \\ V_2\end{bmatrix} = 0$$

$$ 1+\sqrt{5}V_1 = 2V_2 $$

$$ V_{\text{matrix}}= \begin{bmatrix} 2 \\ 1+\sqrt{5} \end{bmatrix} $$

$$\|\mathbf{V}\| = \sqrt{10 + 2\sqrt{5}}$$

---

*ii. $$\Lambda = 2 - \frac{2}{3}\sqrt{5}$$*

$$\begin{bmatrix} 4/3-\Lambda & 4/3 \\ 4/3 & 8/3-\Lambda \end{bmatrix} \cdot \begin{bmatrix}V_1 \\ V_2\end{bmatrix} = 0$$

$$ 1-\sqrt{5}V_1 = 2V_2 $$

$$ V_{\text{matrix}}= \begin{bmatrix} 2 \\ 1-\sqrt{5} \end{bmatrix} $$

$$\|\mathbf{V}\| = \sqrt{10 - 2\sqrt{5}}$$

---

### Folgliches Ergebnis:

**Orientierung:**

*PC1 Orientierung* : $$\begin{bmatrix} 2 \\ 1+\sqrt{5} \end{bmatrix}$$

*PC2 Orientierung* : $$\begin{bmatrix} 2 \\ 1-\sqrt{5} \end{bmatrix}$$

**Varianzanteil:**

$\frac{\lambda_1}{\lambda_1 + \lambda_2} \times 100\%$

*PC1 Varianzanteil* : $\frac{3 + 2.236}{6} \approx \mathbf{87.27\%}$

*PC2 Varianzanteil* : $\frac{3 - 2.236}{6} \approx \mathbf{12.73\%}$

---