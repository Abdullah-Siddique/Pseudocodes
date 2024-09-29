# DFS (Depth-First Search) is Easy to Learn

Many people fear DFS because they think it is a complicated algorithm. Let's see what it actually is, and you'll realize it's much simpler than it seems.

## Definition:

**Depth-First Search (DFS)** is an algorithm for traversing or searching tree or graph data structures. It starts at the root (or an arbitrary node) and explores as far as possible along each branch before backtracking.

## Pseudocode:

DFS(graph, start):
    create a stack
    push start onto the stack
    while stack is not empty:
        current = pop from the stack
        if current is not visited:
            mark current as visited
            for each neighbor of current:
                if neighbor is not visited:
                    push neighbor onto the stack


## Let's Feel It:

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

Now, look attentively and you'll see how DFS works!

---



# Depth-First Search (DFS) Explanation

---

## 1. Start at Node A:

Imagine you're at a maze's entrance, and **Node A** is your starting point. You want to explore as deeply as possible before considering other paths.

- **Traverse**: Begin by moving from **A**. Mark **A** as visited.
- **Backtrack**: You don’t need to backtrack yet since there are unexplored paths.

**Current Path**: `A`

---

## 2. Move to Neighbor B:

From **A**, you have two options: go to **B** or **C**. Following the DFS rule (deepest first), we’ll choose to traverse to **B**.

- **Traverse**: Move from **A** to **B** and mark **B** as visited. Think of it as venturing further down the maze.
- **Backtrack**: No need to backtrack yet because you’re still progressing.

**Current Path**: `A → B`

---

## 3. Move to Neighbor D:

You’re at **B** now. From here, you have only one unvisited neighbor: **D**. Keep going deeper into the maze.

- **Traverse**: Move from **B** to **D** and mark **D** as visited.
- **Backtrack**: **D** has no neighbors left to explore, so you’ve hit a dead end. Time to backtrack!

**Current Path**: `A → B → D`

---

## 4. Backtrack to B:

Since **D** has no neighbors left, you **backtrack** to **B**. Backtracking means you return to the last node that still has unexplored paths.

- You’re back at **B**, but there are no unexplored neighbors here either.
- **Backtrack again**: Go further back to **A**.

**Backtracked Path**: `A`

---

## 5. Move to Neighbor C:

You’ve now explored all possible paths from **B**, so now explore the unvisited neighbor from **A**, which is **C**.

- **Traverse**: Move from **A** to **C** and mark **C** as visited.

**Current Path**: `A → C`

---

## 6. Move to Neighbor E:

You’re at **C**. It has one unvisited neighbor, **E**. Time to go deeper into the maze.

- **Traverse**: Move from **C** to **E** and mark **E** as visited.
- **Backtrack**: **E** has no unvisited neighbors, so you’ve reached another dead end.

**Current Path**: `A → C → E`

---

## 7. Backtrack to C:

Since **E** is a dead end, you **backtrack** to **C**. There are no more unexplored paths at **C**.
- **Backtrack again**: Return to **A**.

---

## DFS Complete:

There are no more unvisited nodes connected to **A**, and you’ve traversed the entire tree using DFS.

---

### Order of Visits:
**A → B → D → C → E**

---

## Breaking Down the Keywords:

### 1. **Traverse**:
When you traverse, you move from one node to a neighbor, exploring deeper down a path.  
In DFS, you always traverse as far as possible, going from one node to the next until you reach a dead end.

### 2. **Backtracking**:
Backtracking happens when you hit a dead end, meaning the current node has no unvisited neighbors left.  
You go back to the previous node (where you came from) and check for other unvisited neighbors.

In our case, after visiting **D**, you backtracked to **B**, and then to **A**, because you had already explored everything from **B**.

---

