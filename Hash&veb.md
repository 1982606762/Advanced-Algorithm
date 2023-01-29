### Xuanlang Zhao (kxd806)

#### Hashing

1. Hash function

A truly random hash function $h: U \longrightarrow[m]$ is a random variable in the class of all functions $U \longrightarrow[m]$, that is, it consists of a random variable $h(x)$ for each $x \in U$.

There are three things that need to pay attention to.

strongly universal

c-approximately universal

2. Application

* Unordered sets use a balanced tree to store

* Hashing with chaining

Each operation takes O( | L[h(x)] | + 1) time.

For $x \notin S, \mathbb{E}[|L[h(x)]|] \leq 1$

* Signatures

Assign a unique "signature" to each $x \in S \subseteq U$, $|S|=n$

$\begin{aligned} \operatorname{Pr}[\exists\{x, y\} \subseteq S \mid s(x)=s(y)] &<\frac{1}{2 n}\end{aligned}$

3. Practical hash functions

* Multiply-mod-prime
* Multiply-shift

#### van Emde Boas Tree

1. Naive solution

predecessor,successor and delete cost O(|U|), others cost O(1)

2. Two level

Predecessor, Successor, and delete cost $\Theta(\sqrt{|U|})$

Others cost O(1)

3. Recursive

Member,predecessor,successor cost O(loglog|U|)

insert and delete cost O(log|U|)

Empty,min,max cost O(1)

4. veb tree

Exclude min ( S ) and / or max ( S ) from the set of ke y s stored in summar y and clusters.

Define summary and clusters[h] array

predecessor, insert cost worst case O(loglog|U|) time

5. RS-veb

Use a hash table instead of an arra y to store clusters [ · ] , and don’t store em p t y substructures.

Cost O(nloglog|U|) space





