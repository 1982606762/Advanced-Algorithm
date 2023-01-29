# Randomized Algorithm xuanlang zhao kxs806

## Quicksort

While doing classic QS, randomly choosing a number as a pivot to split the number into L and R lists, this algorithm costs O(N log N) time on average.

Let X be the number of the comparison, $X_{i j}$to be the number of comparisons between $S_i$ and $S_j$ ,$X_{i j} = \{0,1\}$

Then we can get $E[X]=E\left[\sum_{i=1}^n \sum_{j>i} X_{i j}\right]=\sum_{i=1}^n \sum_{j>i} E\left[X_{i j}\right]=2 n H(n)=O(n \log n)$

## MinCut

Pick a random edge, contract it, and remove self-loops; repeat this step then we can get the min-cut of the graph. This algorithm always returns a cut.

$\operatorname{Pr}[C$ returned $]$

$=\prod_{i=1}^{n-2} p_i \quad$ where $p_i=\operatorname{Pr}\left[\mathcal{E}_i \mid \mathcal{E}_1 \cap \cdots \cap \mathcal{E}_{i-1}\right]$

$\geq \prod_{i=1}^{n-2} \frac{n-1-i}{n+1-i}$

$=\frac{n-2}{n} \cdot \frac{n-3}{n-1} \cdot \frac{n-4}{n-2} \cdots \frac{3}{5} \cdot \frac{2}{4} \cdot \frac{1}{3}$

$=\frac{2}{n(n-1)}$



