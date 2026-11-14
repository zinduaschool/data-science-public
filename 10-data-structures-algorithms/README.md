# Bonus: Data Structures & Algorithms


- **Course Description:** A 10-week bonus course that turns capable coders into problem solvers. Learners build progressively — complexity analysis and search, then sorting and recursion, then linear data structures, then greedy and dynamic programming, then trees, heaps and graphs — before closing with backtracking, intractability and approximation.

- **Course Objective:** Equip learners to analyse an unfamiliar problem, identify its brute-force cost and the paradigm that fits, and implement an efficient solution while reasoning explicitly about time and space trade-offs.

- **Skills to be learned:** Big-O analysis, searching & sorting algorithms, recursion, arrays, hashmaps, linked lists, stacks, queues & deques, greedy algorithms, dynamic programming, trees & heaps, graphs & traversal, pathfinding, backtracking, approximation algorithms

**Audience:** Graduates of the Software Engineering and Data Science bootcamps. Capable coders, *not* CS majors — they need intuition for speed and memory, not formalism for its own sake.

**Goal:** Build problem solvers. By the end, a student should look at an unfamiliar problem and ask the right questions: *What's the brute-force cost? Which paradigm fits? What's the space-time trade?*

**Format:** 10 weeks · 2 live sessions/week (20 live sessions) · **Bonus** items are self-read, not lectured. Every live session ships with a problem set — watching does not build skill, reps do.

---

## Two threads that run through every session

1. **The Big-O reflex.** From Week 1 onward, *every* algorithm gets the same two questions before we move on: what's its time complexity, what's its space complexity. By Week 4 the students should be answering before you ask.
2. **"Which pattern is this?"** Starting at the paradigms block, open or close each session by classifying a problem: brute force, divide & conquer, greedy, or DP? Pattern *recognition* is the actual transferable skill — the specific algorithms are just evidence.

---

## Sections

- **A — Algorithm Foundations**
- **B — Linear Data Structures**
- **C — Optimization Algorithms** *(greedy + DP; D&C is named explicitly where it really lives, in sorting and search)*
- **D — Dynamic Data Structures**
- **E — Hard Problems & Advanced Techniques**

---

## Week 1 — Foundations: cost as a first-class concern
> **Objective:** Treat cost as a first-class concern: learners will be able to state the time and space complexity of an algorithm in Big-O notation, and compare linear, binary and interpolation search on the data they suit.

**Section A**

### Session 1.1 — Big-O Notation
- Why we measure growth, not stopwatch time. Best/average/worst case.
- The ladder: O(1) → O(log n) → O(n) → O(n log n) → O(n²) → O(2ⁿ) → O(n!), with a concrete real-world instance of each.
- Space complexity given equal billing — these are DS grads; memory is not an afterthought.
- *Practice:* annotate a dozen given code snippets with their complexity.

### Session 1.2 — Array Search: Linear vs Binary vs Interpolation
- First real trade-off: binary's O(log n) buys speed but costs a sorted precondition.
- Interpolation as "binary search that guesses where to look" — and where it degrades.
- **First D&C sighting** — name it: binary search halves the problem each step. Plant the flag here.
- *Practice:* implement all three; empirically time them on growing inputs and plot it.

---

## Week 2 — Sorting & first contact with recursion
> **Objective:** Sort data and reason about the cost: learners will be able to implement and compare selection, bubble and insertion sort, and use recursion and divide-and-conquer to implement merge sort and quick sort.

**Section A**

### Session 2.1 — Basic Sorting: Selection, Bubble, Insertion
- Three O(n²) sorts — taught so students *feel* why O(n²) hurts before we rescue them.
- Stability, in-place, and best-case behavior (insertion sort on nearly-sorted data).
- *Practice:* implement all three; instrument comparisons and swaps.

### Session 2.2 — Recursive Sorting: Merge Sort & Quick Sort
- **Recursion's first appearance** — introduced here lightly out of necessity: call stack, base case, recursive case. Just enough to understand the sorts; the rigorous treatment comes in Week 5.
- Merge sort (D&C, stable, O(n log n), O(n) space) vs quicksort (in-place, fast average, O(n²) worst, pivot sensitivity).
- **Second D&C sighting** — explicitly tie back to binary search: same "split, solve, combine" shape.
- *Practice:* implement both; break quicksort with an adversarial input, then fix it with a better pivot.

> **Bonus 2.3 (self-read):** Heap sort, radix sort, bogo sort. Heap sort is best read *after* Week 7 once heaps are taught — flag this forward reference. Radix as the "sorting without comparisons" curiosity; bogo as the joke that teaches why we measure complexity.

---

## Week 3 — Linear structures: the everyday workhorses
> **Objective:** Choose the right everyday structure: learners will be able to use arrays and hashmaps for fast access and lookup, and implement linked lists while explaining their trade-offs against arrays.

**Section B**

### Session 3.1 — Arrays & Hashmaps
- Arrays: contiguous memory, O(1) index, costly insert/delete.
- Hashmaps as the most important practical structure they'll use: O(1) average lookup, hashing, collisions, the load-factor trade. For DS grads, this is the bread-and-butter.
- *Practice:* the classic hashmap reps — two-sum, frequency counts, dedup, group-by.

### Session 3.2 — Linked Lists
- Singly/doubly; pointer mechanics; O(1) insert/delete vs O(n) access — the exact inverse of arrays.
- Two-pointer technique (fast/slow), cycle detection.
- *Practice:* reverse a list, detect a cycle, merge two sorted lists.

---

## Week 4 — Abstract types, then the first paradigm
> **Objective:** Model behaviour with abstract types and a first paradigm: learners will be able to implement stacks, queues and deques, and recognise and solve problems where a greedy choice is provably correct.

**Section B → C**

### Session 4.1 — Stacks, Queues & Deques
- LIFO/FIFO as *abstract* types over arrays or lists. Where each shows up: call stacks, BFS queues, undo, sliding windows.
- *Practice:* balanced-parentheses, min-stack, queue-from-two-stacks.

### Session 4.2 — Greedy Algorithms
- **First paradigm taught in the abstract.** Make a locally optimal choice; when does it yield the global optimum?
- Worked: coin change (where greedy works and where it lies), interval scheduling, Huffman intuition.
- The honest framing: greedy is the simple thing you try first — and DP is what you reach for *when greedy fails*. This sets up Week 5.
- *Practice:* a greedy problem that works and a near-identical one that doesn't — make them find the seam.

---

## Week 5 — Recursion → Memoization → Dynamic Programming
> **Objective:** Turn exponential recursion into efficient solutions: learners will be able to add memoization to recursive solutions, build bottom-up dynamic programming tables, and apply the longest-common-subsequence pattern.

**Section C**

### Session 5.1 — Intro to Dynamic Programming
- **The rigorous recursion session.** Recursion was introduced lightly in Week 2; here it gets the full treatment: stack frames, base cases, reading a recursion tree to *see* the repeated subproblems.
- The pipeline that makes DP click: brute-force recursion → spot overlapping subproblems → memoize (top-down) → tabulate (bottom-up).
- Optimal substructure + overlapping subproblems as the two conditions to look for.
- *Practice:* take recursive Fibonacci from O(2ⁿ) to O(n) live; then climbing-stairs / coin-change-count.

### Session 5.2 — The LCS DP Pattern
- Longest Common Subsequence as the canonical 2-D table. Highly relevant to DS grads: diffing, fuzzy matching, edit distance's cousin.
- Filling the grid, reading the answer, reconstructing the path.
- *Practice:* LCS, then edit distance as a variation on the same scaffold.

> **Bonus 5.3 (self-read):** Fibonacci DP — extra solved 1-D examples for students who want more reps before the 2-D knapsack jump.

---

## Week 6 — The Knapsack family
> **Objective:** Optimise under constraints: learners will be able to recognise knapsack-style problems and solve 0/1 and unbounded knapsack variants with dynamic programming.

**Section C**

### Session 6.1 — 0/1 Knapsack
- The archetypal capacity-vs-value DP. Each item taken once.
- The 2-D table, then the 1-D space optimization — a clean lesson in *trading a dimension away*.
- *Practice:* subset-sum and partition-equal-subset as knapsack in disguise (pattern recognition payoff).

### Session 6.2 — Unbounded Knapsack
- Same frame, items reusable — and how that single change rewrites the recurrence.
- Coin-change (min coins) revisited as unbounded knapsack — closing the loop with the Week 4 greedy version so they see why DP was needed.
- *Practice:* rod-cutting, coin-change-min.

> **Bonus 6.3 (self-read):** Egg-dropping (a min-max DP) **and** matrix-chain multiplication (an interval DP). *These are two distinct patterns* — keep them clearly separated, not conflated. Strong material for the keen, genuinely harder than the core.

---

## Week 7 — Trees & heaps
> **Objective:** Work with hierarchical data: learners will be able to implement and traverse trees and binary search trees, and use heaps for priority-based problems.

**Section D**

### Session 7.1 — Trees
- Terminology (root, height, depth, leaf), binary trees, and the BST property.
- BST insert / search / delete, and the **balancing intuition**: why a degenerate BST decays from O(log n) to O(n). Self-balancing trees (AVL, Red-Black) named *by purpose* — mechanics deferred to bonus.
- One-line live mention of B-trees: this is the shape inside every database index your DS grads will touch.
- *Practice:* validate a BST, find kth-smallest, compute height.

### Session 7.2 — Tree-based Algorithms (incl. Heaps)
- The traversals as core machinery: pre/in/post-order (DFS family) + level-order (BFS) — these recur everywhere downstream.
- **Heaps & priority queues** taught here (a heap *is* a tree): heapify, push/pop, why it's the right tool for "always give me the current best." Directly arms Dijkstra in Week 9.
- *Practice:* top-k elements, merge-k-sorted-lists, level-order traversal.

> **Recommended reading (elevated from bonus):** **Tries** — prefix search and autocomplete are everyday DS/SWE work; worth more than a footnote.
> **Bonus (self-read):** AVL/Red-Black rotation mechanics, segment/Fenwick trees.

---

## Week 8 — Graphs & traversal
> **Objective:** Model connected data: learners will be able to represent graphs as adjacency lists and matrices, and explore them with breadth-first and depth-first traversal.

**Section D**

### Session 8.1 — Graphs
- Modeling the world as nodes + edges. Directed/undirected, weighted/unweighted, cyclic/acyclic.
- Representations and their trade: adjacency list vs matrix (space vs lookup) — a Big-O decision in its own right.
- *Practice:* build both representations; convert between them.

### Session 8.2 — Traversal Algorithms
- BFS and DFS as the two lenses — and the payoff that they're the *same* structures from Week 4 (queue → BFS, stack/recursion → DFS).
- Connected components, cycle detection, topological sort.
- *Practice:* number-of-islands (grid-as-graph), course-schedule (topo sort).

---

## Week 9 — Putting paradigms on graphs
> **Objective:** Apply paradigms to graphs: learners will be able to find shortest paths with greedy and dynamic-programming algorithms such as Dijkstra and Floyd-Warshall, and solve dynamic programming problems on grids.

**Section D** — *this is where the abstract paradigms from Weeks 4-6 get re-applied concretely. That re-application is the whole reason optimization came first.*

### Session 9.1 — Pathfinding Algorithms
- Dijkstra as **greedy on a graph** — and it runs on the priority queue from Week 7. Name the callback explicitly.
- A* as Dijkstra plus a heuristic; brief note on why negative edges break greedy (motivates the next session).
- *Practice:* shortest path on a weighted graph; trace the frontier by hand once before coding.

### Session 9.2 — DP on Graphs & Grids
- Grid DP (unique-paths, min-path-sum) as DP on a 2-D lattice — a clean bridge from the knapsack tables.
- **Floyd-Warshall as all-pairs shortest path** — this is **DP on a graph, not grid DP**; label it correctly. The triple loop *is* a DP recurrence over "shortest path using only the first k nodes."
- *Practice:* min-path-sum grid; then Floyd-Warshall on a small weighted graph.

---

## Week 10 — Hard problems & advanced techniques (capstone)
> **Objective:** Recognise the limits of efficient computation: learners will be able to solve constraint problems with backtracking, explain intractability and NP-hardness, and apply approximation strategies to problems such as the travelling salesman problem.

**Section E** — *promoted from bonus to live. This is where "build problem solvers" is cashed out.*

### Session 10.1 — Backtracking
- The systematic brute force: choose → explore → un-choose. DFS over a decision space with pruning.
- Worked: permutations, subsets, N-Queens, Sudoku — and **brute-force TSP**, deliberately, so they watch the factorial blow-up happen.
- *Practice:* generate-permutations, combination-sum, N-Queens.

### Session 10.2 — Intractability & Approximation (NP + TSP, the closing arc)
- Name what backtracking-TSP just showed them: a class of problems with no known efficient solution — **NP-hardness**, taught *concept-only* and *situated in TSP*, not as an abstract lecture. Intuition for P vs NP; why *checking* a solution can be easy while *finding* one is not.
- **Approximation** as the practical response: nearest-neighbor and greedy heuristics for TSP that get close, fast. The honest engineering lesson — when optimal is off the table, get provably-good-enough.
- Capstone framing of the whole course: **brute force → recognize intractability → reach for the right paradigm or a good-enough heuristic.**
- *Practice:* implement a TSP approximation; compare its tour to brute-force optimal on small inputs.

> **Bonus (self-read):** Bit manipulation — genuinely niche for this cohort; useful tricks (masks, XOR swaps, subset enumeration) but not load-bearing for the course's goals.

---

## Self-read / bonus track (consolidated)

| Item | Where it attaches | Why it's bonus |
|---|---|---|
| Heap, radix, bogo sort | After Week 7 (needs heaps) | Heap sort reinforces heaps; radix/bogo are curiosities |
| Fibonacci DP extras | Week 5 | More 1-D reps before 2-D DP |
| Egg-drop + matrix-chain DP | Week 6 | Distinct, harder patterns for the keen |
| Tries *(recommended, not optional)* | Week 7 | Everyday DS/SWE; elevate if time allows |
| AVL / Red-Black rotations | Week 7 | Mechanics; the *purpose* is already core |
| Segment / Fenwick trees | Week 7 | Competitive-programming flavor |
| Bit manipulation | Week 10 | Niche for this cohort |

---

## A note on sequencing

Paradigms (greedy, DP) are taught **in the abstract on arrays first (Weeks 4-6)**, *then* the dynamic structures (Weeks 7-9) re-apply them: Dijkstra *is* greedy, Floyd-Warshall *is* DP. Students meet each idea twice — once pure, once embodied — which is what makes the graph algorithms land instead of feeling like magic. This is why optimization precedes trees and graphs, and it's a deliberate design choice, not an accident of ordering.

---

## Course Contributors
This course has been built by:
- Cyril Michino: Co-founder at Zindua School
- Kipkirui Keter: Tech Ops at Zindua School

Other previous contributors are: Bonaventure Ogeto, Walobwa Dan, and Kwanusu Joseph
