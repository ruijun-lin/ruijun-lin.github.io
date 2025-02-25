# Connections between topological and categorical limits


The definitions of a filter and its related concepts are from Tai-Danae Bradley, Tyler Bryson, and John Terilla, *Topology: A Categorical Approach*.

> **Definition.** (filter) A **filter** on a set $X$ is a collection $\mathcal{F}$ that is
> (i) downward directed: $A,B\in \mathcal{F}$ implies there exists $C\in \mathcal{F}$ such that $C\subseteq A\cap B$,
> (ii) nonempty: $\mathcal{F} \neq \varnothing$,
> (iii) upward closed: $A\in \mathcal{F}$ and $A\subseteq B$ implies $B\in \mathcal{F}$.
> An additional property is often useful:
> (iv) proper: there exists $A\subseteq X$ such that $A\notin \mathcal{F}$.

*Remarks:*

- Being downward directed and upward closed implies that filters are closed under finite intersections, and being proper is equivalent to the requirement that  $\varnothing \notin \mathcal{F}$.
- $2^{X}$ is itself a filter but not proper.
- A set that is only downward directed and nonempty is called a **filterbase**. Any filterbase generates a filter simply by taking the upward closure of the base.

**Examples.**

- (trivial filter) For any set $X$ there is the smallest filter $\{X\}$ called the trivial filter.
- (eventuality filter) Given a sequence $\{x_{n}\}$ in a space $X$, the set

$\mathcal{E}_ {x_n} = \lbrace A \subseteq X \mid \text{ there exists an } N \text{ so that } x_n \in A \text{ for all } n \geq N \rbrace$

is a proper filter.

- (non-example, open neighborhoods of a point $x$) Given a topological space $X$ and a point $x\in X$ , the collection of open neighborhoods of $x$ denoted by $\mathcal{T}_{x}$, is generally not a filter, but a filterbase.

> **Definition.** (convergence) A filter $\mathcal{F}$ on a topological space $(X,\mathcal{T})$ converges to $x$ if and only if $\mathcal{F}$ refines $\mathcal{T}_x$, that is, if $\mathcal{T}_x \subseteq \mathcal{F}$. When $\mathcal{F}$ converges to $x$ we will write $\mathcal{F} \rightarrow x$.

As an easy observation, a sequence $\{x_{n}\}$ converges to a point $x$ if and only if $\mathcal{E}_{x_n}$.

With the concept of filters, we now give an equivalence statement between the **categorical limit** and the **topological limit.**

Let $X$ be a topological space and $\mathcal{F}_X$ be the collenction of all filters on $X$.

Given $x \in X$ and $F \in \mathcal{F}_{X}$, let $\mathcal{U}_X(x)$ be the neighborhood filter of $x$, which is the filter generated by $\mathcal{T}_x$ and let

$$
\mathcal{F}_{x,F} = \lbrace G \in \mathcal{F}_X \mid \mathcal{F} \cup \mathcal{U}_X(x) \subseteq G \rbrace
$$

be the collection of all the filters containing both $F$ and the neighborhood filter of $x$.

We observed that
$F \subseteq F \cup \mathcal{U}_ X(x) \subseteq \bigcap_{G\in \mathcal{F}_ {x,F}}G,$ and the latter two sets are filters.

Also since $\bigcap_ {G\in \mathcal{F}_ {x,F}}G$ is the smallest filter containing $F \cup \mathcal{U}_ X(x)$ and $F \cup \mathcal{U}_ X(x)$ is itself a filter, we have that $\bigcap_{G\in \mathcal{F}_ {x,F}}G \subseteq F \cup \mathcal{U}_ X(x)$ so that $\bigcap_ {G\in \mathcal{F}_ {x,F}}G = F \cup \mathcal{U}_ X(x)$.

View the inclusion of sets "$\subseteq$" as a partial order on $\mathcal{F}_ X$ and $\mathcal{F}_ {X,F}$. Then $\mathcal{F}_ X$ becomes a small category and $\mathcal{F}_ {X,F}$ is its subcategory. Let $E : \mathcal{F}_ {X,F} \to \mathcal{F}_X$ be the embedding functor. Now we have a theorem indicating the connection between the categorical limit and the topological limit.

> **Theorem.** $x$ is a topological limit of the filter $F$ if and only if $F$ is a categorical limit of the functor $E$.

*Proof.* $x$ is a topological limit of the filter $F$, i.e., $F \to x$

$\Leftrightarrow (\mathcal{T}_x \subseteq \mathcal{U}(x)) \subseteq F \ \text{and} \ F \cup \mathcal{U}(x) \subseteq F$

$F = \bigcap_{G \in \mathcal{F}_{X,F}} g$ (the universal object)

$\Leftrightarrow (F \xrightarrow{p_{G}}E(G))_ {G \in \mathcal{F}_ {x,F}}$ is a limit cone of $E$

(i.e., $F$ is a categorical limit of $E$)

**References**

- Bradley, T.-D., Terilla, J. and Bryson, T. (2020) *Topology: A categorical approach*. Cambridge, MA: The MIT Press.
- Rafael MrdenRafael Mrden 2, bonnbakibonnbaki 98899 silver badges1010 bronze badges and Damien LDamien L 6 (1956) Category-theoretic limit related to topological limit?, Mathematics Stack Exchange. Available at: https://math.stackexchange.com/questions/60590/category-theoretic-limit-related-to-topological-limit (Accessed: 08 February 2025). 
 

