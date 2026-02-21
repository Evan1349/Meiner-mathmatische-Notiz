# Hauptkomponentenanalyse
--
![alt text](./Resources/image.png)
--
## 1. Defintion und Ziel
**Definition:** Die **Hauptkomponentenanalyse(PCA)** ist ein Verfahren der multivariaten Statistik, das zur *Dimensionsreduktion* verwendet wird.

**Hauptziel:** Um Informationen aus einem großen Datensatz zu vereinfachen, wobei sie die wichtigsten Merkmale enthalten blieben. Dadurch können die Daten das *Rauschen* reduzieren wird. 

## 2. Die Formel und Schritt-für-Schritt-Anleitung

### A. **Zentrierung der Daten** (Vorbereitung)
Zuerst werden die Daten Zentriert, um den *Mittelpunkt* der Datenwolke in den Ursprung zu verschieben.

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

### *Gegebene Daten (zentriert)*:
$D = \{(-1, -2), (-1, 0), (1, 0), (1, 2)\}$

### Schritt 1: Kovarianzmatrix berechnen

$$\Sigma = \begin{pmatrix} 4/3 & 4/3 \\ 4/3 & 8/3 \end{pmatrix}$$

### Schritt 2: Charakteristische Gleichung lösen

$$\det(\Sigma - \lambda I) = \lambda^2 - 4\lambda + \frac{16}{9} = 0$$

### Schritt 3: Ergebnisse für Eigenwerte

*nutzen*: $$\lambda = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

$$\lambda = 2 \pm \frac{2}{3}\sqrt{5}$$

### Schritt 4: Transformation

gesetzt 