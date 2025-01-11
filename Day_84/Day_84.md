# Day 84 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 84** of my **100 Days of Code Challenge**! Today, I implemented a solution to the **M-coloring problem** for an undirected graph. The goal was to determine if it's possible to color the graph using at most **M colors** such that no two adjacent vertices share the same color. This problem uses **backtracking** to explore all possible color assignments.

---

## ✅ Problem Description
Given:
- An **undirected graph** with \( N \) vertices and \( E \) edges.
- An integer \( M \), representing the maximum number of colors available.

The task is to determine if it is possible to color the graph such that:
1. No two adjacent vertices share the same color.
2. At most \( M \) colors are used.

### Input Format:
1. Number of vertices \( N \).
2. Number of colors \( M \).
3. Number of edges \( E \).
4. \( E \) edges in the format \( u \, v \), representing an edge between vertices \( u \) and \( v \).

### Output Format:
- Print `1` if the graph can be colored with at most \( M \) colors.
- Print `0` otherwise.

---

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Backtracking, Graph Theory, Adjacency List Representation

---

## 📖 Code Example

```java
package coading_Challange;

import java.util.*;

public class Day_84 {
    public static boolean graphColoring(List<Integer>[] graph, int[] colors, int m, int vertex) {
        int n = graph.length;

        // If all vertices are colored, return true
        if (vertex == n) {
            return true;
        }
        // Try all colors for the current vertex
        for (int color = 1; color <= m; color++) {
            if (isSafeToColor(graph, colors, vertex, color)) {
                colors[vertex] = color; // Assign color
                if (graphColoring(graph, colors, m, vertex + 1)) {
                    return true;
                }
                colors[vertex] = 0; // Backtrack
            }
        }
        return false; // No valid color found
    }

    public static boolean isSafeToColor(List<Integer>[] graph, int[] colors, int vertex, int color) {
        for (int neighbor : graph[vertex]) {
            if (colors[neighbor] == color) {
                return false; // Adjacent vertex has the same color
            }
        }
        return true;
    }

    public static int canColorGraph(int n, int m, int e, int[][] edges) {
        // Build the graph as an adjacency list
        List<Integer>[] graph = new ArrayList[n];
        for (int i = 0; i < n; i++) {
            graph[i] = new ArrayList<>();
        }
        for (int[] edge : edges) {
            graph[edge[0]].add(edge[1]);
            graph[edge[1]].add(edge[0]);
        }

        // Array to store colors of vertices
        int[] colors = new int[n];
        Arrays.fill(colors, 0);

        // Solve the graph coloring problem
        return graphColoring(graph, colors, m, 0) ? 1 : 0;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input
        System.out.println("Enter number of vertices (N): ");
        int n = sc.nextInt();
        System.out.println("Enter number of colors (M): ");
        int m = sc.nextInt();
        System.out.println("Enter number of edges (E): ");
        int e = sc.nextInt();
        sc.nextLine(); // Consume the leftover newline character

        System.out.println("Enter edges (in the format u v, one per line): ");
        int[][] edges = new int[e][2];
        for (int i = 0; i < e; i++) {
            edges[i][0] = sc.nextInt();
            edges[i][1] = sc.nextInt();
        }

        // Output
        System.out.println(canColorGraph(n, m, e, edges));
        sc.close();
    }
}
🖥️ Program Output
Input:

Enter number of vertices (N): 
4
Enter number of colors (M): 
3
Enter number of edges (E): 
5
Enter edges (in the format u v, one per line): 
0 1
1 2
2 3
3 0
0 2
Output:

1
```
---
## 📚 Lessons Learned
Learned how to represent graphs using adjacency lists for efficient edge traversal.
Implemented backtracking to explore all possible color assignments for graph vertices.
Gained deeper insights into solving graph problems with constraints.

---
## ⚡ Challenges
Efficiently handling graph representations for large input sizes.
Ensuring correctness of the backtracking logic for all edge cases.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
