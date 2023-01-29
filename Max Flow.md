# Max Flow

## Flow and Max flow

There's a flow network G = (V, E), which is a directed graph, each edge has a capacity. Imagine each edge is a water pipe, and there is a source vertex s and a destination t. We need to input some water into s, go through the pipes, and reach the destination. All the water in the pipes can be regarded as a flow. Each pipe can contain a different amount of water, so we are looking for a way to transfer as much water as possible through the graph, and that is a max flow.

### definitions

Capacity constraint: For all $u, v \in V$, we require $0 \leq f(u, v) \leq c(u, v)$

Flow conservation: For all $u \in V-\{s, t\}$, we require $\sum_{v \in V} f(v, u)=\sum_{v \in V} f(u, v)$.

Flow value: $|f|=\sum_{v \in V} f(s, v)-\sum_{v \in V} f(v, s)$

## Ford-Fulkerson

### Predefine concepts

Residual network: $G_f$ is a flow network with a capacity of $c_f$ 

$c_f(u, v)= \begin{cases}c(u, v)-f(u, v) & \text { if }(u, v) \in E \\ f(v, u) & \text { if }(v, u) \in E \\ 0 & \text { otherwise }\end{cases}$

For each edge in G, calculate its two-way residual edge, and use it to form the new residual network.

Augmenting path: a path from s to t

Augmentation of flow: $f \uparrow f^{\prime}$

$\left(f \uparrow f^{\prime}\right)(u, v)= \begin{cases}f(u, v)+f^{\prime}(u, v)-f^{\prime}(v, u) & \text { if }(u, v) \in E \\ 0 & \text { otherwise }\end{cases}$

### F.F. algorithm

do

find an augmentation path in $G_f$

Change the flow in G.

repeat

### Running time of F.F

if all capacities of G are int, then F.F consume $O(E*|f^*|)$ time.E is the number of edges, |f*| is the number of iteration.In the worst case, it's maxflow value.

### Cut

Cut(S, T) separate vertexes into S(includes s) and T(has t).

Cut capacity is the sum of edges from S to T's capacity. 

### Max flow Min cut theorem

if f is a max flow in G, then the residual network $G_f$ doesn't have an augmenting path, and the capacity of any cut of G is minimal and equal to $|f|$

## EK algorithm

The only difference is it selects the shortest aug path each time.

It runs in $O(VE^2)$ time