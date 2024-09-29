# BFS (Breadth-First Search)

BFS refers to **Breadth-First Search**, and we can define it as an algorithm for traversing or searching tree or graph data structures. It starts at a specified node and explores all its neighbors at the present depth level before moving on to nodes at the next depth level.

## Pseudocode:

```text
BFS(graph, start):
    create a queue
    enqueue start
    mark start as visited
    while queue is not empty:
        current = dequeue from the queue
        for each neighbor of current:
            if neighbor is not visited:
                mark neighbor as visited
                enqueue neighbor

Visualization:

```
    A
   / \
  B   C
 /     \
D       E

```

### Nodes:
- A, B, C, D, E

### Edges:
- A to B
- A to C
- B to D
- C to E

## Let's Feel It:

# Breadth-First Search (BFS) Explanation

---

## 1. Start at Node A:

Imagine you're at a park entrance, and **Node A** is where you begin your exploration. In BFS, you want to explore all neighboring areas at the same level before moving deeper.

- **Explore**: Start by visiting **A**. Mark **A** as visited.
- **Level Up**: Before moving deeper, check all immediate neighbors.

**Current Path**: `A`

---

## 2. Move to Neighbors B and C:

From **A**, you have two neighbors: **B** and **C**. According to the BFS rule (visit all neighbors at the current level), you’ll visit both.

- **Explore**: Move to **B** and mark it as visited.
- Then, visit **C** and mark it as visited too.

**Current Path**: `A → B, C`

---

## 3. Move to Neighbor D:

Next, you check for unvisited neighbors of **B**. You find **D**.

- **Explore**: Move from **B** to **D** and mark it as visited.

**Current Path**: `A → B → D`

---

## 4. Move to Neighbor E:

Now, check the unvisited neighbors of **C**. You find **E**.

- **Explore**: Move from **C** to **E** and mark it as visited.

**Current Path**: `A → B → C → E`

---

## 5. Complete BFS:

At this point, you've visited all the nodes connected to **A**. Nodes **D** and **E** have no unvisited neighbors, so you're done.

---

### Order of Visits:
**A → B → C → D → E**

---

## Breaking Down the Keywords:

### 1. **Explore**:
When you explore, you visit a node and check all its neighbors before moving deeper.  
In BFS, you explore all neighbors of a node before going to the next level.

### 2. **Level Up**:
Leveling up means moving to the next depth level after you’ve visited all neighbors at the current level.  
You move to the next set of nodes only after fully exploring the current nodes.

---

