# Day 97: Minimum Operations to Change Tree Coloring

## 📝 Problem Description

Arun has a **rooted tree** of `N` vertices rooted at vertex 1. Each vertex is either **black (1)** or **white (0)**. 

The tree starts with a coloring described by `A` (initial colors) and needs to be transformed into a new coloring described by `B` (desired colors). 

### Allowed Operation
Arun can perform the following operation any number of times:
- Choose any **subtree** and paint all its vertices **white** or **black**.

### Goal
Find the **minimum number of operations** required to transform the coloring of the vertices from `A` to `B`.

---

## 🚀 Approach

### Key Observations
1. A **subtree flip** changes all vertices of the subtree to either **black** or **white**.
2. Use **DFS traversal** to:
   - Compare the current color of a node with its desired color.
   - Determine whether a flip is required for the current subtree.

3. Use parent and grandparent "flip states" to track cumulative flips during the traversal.

### Steps:
1. **Input Parsing**:
   - Read the number of test cases.
   - For each test case, read the tree structure, initial colors (`A`), and desired colors (`B`).

2. **Tree Representation**:
   - Use an adjacency list to represent the tree structure.

3. **DFS Traversal**:
   - Traverse the tree starting from the root (vertex 1).
   - For each node, calculate the **current flip state**:
     - `(A[node] + parentFlip + grandParentFlip) % 2`
   - If the current state does not match the desired state (`B[node]`):
     - Perform a subtree flip.
     - Update the parent's flip state.

4. **Count Operations**:
   - Maintain a counter to track the number of flips performed.

5. **Output the Result**:
   - For each test case, output the minimum number of flips.

---

## 💻 Code

```java
package coading_Challange;

import java.util.*;

public class Day_97 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int T = input.nextInt(); // Number of test cases

        while (T-- > 0) {
            int N = input.nextInt(); // Number of vertices

            int[] A = new int[N + 1]; // Initial colors
            int[] B = new int[N + 1]; // Desired colors

            for (int i = 1; i <= N; i++) {
                A[i] = input.nextInt();
            }

            for (int i = 1; i <= N; i++) {
                B[i] = input.nextInt();
            }

            // Build the tree using adjacency list
            List<List<Integer>> tree = new ArrayList<>();
            for (int i = 0; i <= N; i++) {
                tree.add(new ArrayList<>());
            }

            for (int i = 0; i < N - 1; i++) {
                int u = input.nextInt();
                int v = input.nextInt();
                tree.get(u).add(v);
                tree.get(v).add(u);
            }

            // Perform DFS to calculate the minimum operations
            boolean[] visited = new boolean[N + 1];
            int[] result = new int[1]; // Use an array to store the result as we modify it during recursion
            dfs(1, -1, 0, 0, tree, A, B, visited, result);

            // Output the result for this test case
            System.out.println(result[0]);
        }

        input.close();
    }

    private static void dfs(int node, int parent, int parentFlip, int grandParentFlip, List<List<Integer>> tree, int[] A, int[] B, boolean[] visited, int[] result) {
        visited[node] = true;

        // Current flip state
        int currentFlip = (A[node] + parentFlip + grandParentFlip) % 2;

        // If current state doesn't match the desired state, flip the subtree
        if (currentFlip != B[node]) {
            result[0]++;
            parentFlip = 1 - parentFlip; // Toggle the flip state
        }

        // Traverse children
        for (int child : tree.get(node)) {
            if (!visited[child]) {
                dfs(child, node, grandParentFlip, parentFlip, tree, A, B, visited, result);
            }
        }
    }
}
🔍 Input/Output Examples
Example 1
Input:

1
5
1 0 1 0 1
0 1 0 1 0
1 2
1 3
2 4
2 5
Output:

2
```
---
## Explanation:

- Flip the subtree rooted at vertex 1 to match the desired colors.
- Flip the subtree rooted at vertex 2 for the final adjustments.

---
## 🧠 Key Learnings
- Tree Traversals:

- DFS is crucial for efficiently traversing and updating tree states.
- Dynamic Flip Propagation:

- Use parent and grandparent states to handle cumulative changes.
- Greedy Decisions:

- Local flips based on immediate mismatches lead to the globally optimal solution.

--- 
## 💡 Next Steps
- Explore more tree-based optimization problems.
- Dive deeper into advanced DFS applications for tree algorithms.

---
## 🤝 Let's Connect!
Feel free to reach out for questions or discussions! 😊

## #100DaysOfCode #Java #TreeTraversal #DFS #ProblemSolving
