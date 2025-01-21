# Day 93: Friendship Suggestions in a Social Network

## 📝 Problem Description

Ilya is working on a social network, "TheScorpyBook.com", which has `N` registered users.  
- Users can be friends, represented by an **adjacency matrix** where `matrix[u][v] = 1` if `u` and `v` are friends and `0` otherwise.  
- A **friendship suggestion** is made if:
  - Users `u` and `v` are not friends, and
  - There exists a user `w` who is friends with both `u` and `v`.  

Ilya needs to count the total number of **friendship suggestions** to make his network more connected.

---

## 🚀 Approach

1. **Input Representation**:
   - An **adjacency matrix** represents friendships between `N` users.

2. **Key Observations**:
   - A pair `(u, v)` gets a friendship suggestion if `matrix[u][v] == 0` and there exists a **mutual friend** `w` such that `matrix[u][w] == 1` and `matrix[v][w] == 1`.

3. **Algorithm**:
   - Iterate over all user pairs `(u, v)`.
   - For each pair, count the number of **mutual friends** `w`.
   - Add the count of mutual friends to the total suggestions.

4. **Complexity**:
   - **Time Complexity**: `O(N^3)` due to the nested loops for `(u, v, w)`.

---

## 💻 Code

```java
package coading_Challange;

import java.util.Scanner;

public class Day_93 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input: Number of users in the network
        int n = sc.nextInt();
        sc.nextLine(); // Consume newline character

        // Input: Friendship adjacency matrix
        int[][] matrix = new int[n][n];
        for (int i = 0; i < n; i++) {
            String line = sc.nextLine();
            for (int j = 0; j < n; j++) {
                matrix[i][j] = line.charAt(j) - '0';
            }
        }

        // Count friendship suggestions
        System.out.println(countFriendshipSuggestions(n, matrix));
    }

    private static int countFriendshipSuggestions(int n, int[][] matrix) {
        int suggestions = 0;

        // Iterate over all pairs of users (u, v)
        for (int u = 0; u < n; u++) {
            for (int v = 0; v < n; v++) {
                if (u != v && matrix[u][v] == 0) { // Not friends
                    // Count mutual friends
                    int mutualFriends = 0;
                    for (int w = 0; w < n; w++) {
                        if (w != u && w != v && matrix[u][w] == 1 && matrix[v][w] == 1) {
                            mutualFriends++;
                        }
                    }
                    suggestions += mutualFriends; // Add mutual friends for this pair
                }
            }
        }

        return suggestions;
    }
}
🔍 Input/Output Examples
Input:

4
0110
1001
1001
0100
Output:

4
Explanation:
For the given adjacency matrix:


User 1: Friends with 2, 4  
User 2: Friends with 1, 3  
User 3: Friends with 2, 4  
User 4: Friends with 1, 3  
Suggestions:
(1, 3) via user 2
(1, 3) via user 4
(2, 4) via user 1
(2, 4) via user 3
Total = 4
```
---
## 🧠 Key Learnings
Adjacency Matrix Representation:
Efficient for small to medium-sized graphs.
Triple Nested Loops:
While costly, they are necessary for problems requiring pairwise relationships in graphs.
Mutual Friends Logic:
Real-world application of graph algorithms.

---
## 📬 Let's Connect!
Feel free to reach out for questions or discussions. 😊

---
## #100DaysOfCode #Java #CodingChallenge #GraphTheory #SocialNetwork
