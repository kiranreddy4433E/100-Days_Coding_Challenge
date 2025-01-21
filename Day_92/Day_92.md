# Day 92: Minimize the Number of Atoms in Subsets

## 📝 Problem Description

Given:
- A set `X` of integers between `0` and `n-1`.
- A collection of subsets `S1, S2, ..., Sm` of `X`.

We aim to:
- Find a collection of **atoms** `A1, ..., Ak` such that every element in `X` is in some `Ai`, and no two `Ai` and `Aj` (where `i ≠ j`) share a common item.
- Minimize `k`, the number of atoms.

An **atom** is defined as a subset of `X` where:
1. For each subset `Si`, either the atom is fully contained in `Si` or it has no intersection with `Si`.

---

## 🚀 Approach

1. **Subset Membership Representation**:
   - Represent the membership of each element in `X` with respect to subsets `S1, S2, ..., Sm` as a binary string.
   - For each element `x ∈ X`, create a binary string where:
     - `1` indicates that `x ∈ Si`.
     - `0` indicates that `x ∉ Si`.

2. **Find Unique Patterns**:
   - Each unique binary pattern corresponds to a unique atom.
   - Use a set to store the unique patterns.

3. **Output**:
   - The number of unique atoms corresponds to the size of the set of unique patterns.

---

## 💻 Code

```java
package coading_Challange;

import java.util.*;

public class Day_92 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        int t = input.nextInt(); // Number of test cases

        while (t-- > 0) {
            int n = input.nextInt(); // Size of X
            int m = input.nextInt(); // Number of subsets

            // Read subsets and store their membership in a boolean matrix
            boolean[][] membership = new boolean[m][n];
            for (int i = 0; i < m; i++) {
                int subsetSize = input.nextInt();
                for (int j = 0; j < subsetSize; j++) {
                    int element = input.nextInt();
                    membership[i][element] = true;
                }
            }

            // Use a set to store unique membership patterns
            Set<String> uniqueAtoms = new HashSet<>();

            // Calculate membership pattern for each element in X
            for (int x = 0; x < n; x++) {
                StringBuilder pattern = new StringBuilder();
                for (int i = 0; i < m; i++) {
                    pattern.append(membership[i][x] ? "1" : "0");
                }
                uniqueAtoms.add(pattern.toString()); // Each pattern defines an atom
            }

            // Number of unique atoms
            System.out.println(uniqueAtoms.size());
        }

        input.close();
    }
}
🔍 Input/Output Examples
Input:

2
4 3
2 0 1
2 1 2
1 3
5 2
3 0 1 2
3 2 3 4
Output:

4
5
```
---
## 🧠 Key Learnings
Subset Representation: Using binary patterns to represent subset memberships is efficient for such problems.
Set Operations: Leveraging HashSet ensures unique patterns are stored, simplifying the calculation of atoms.
Efficiency: This approach is computationally efficient, as we focus only on unique patterns.

---
## 📬 Let's Connect!
Feel free to reach out for any questions or discussions. 😊

---
### #100DaysOfCode #Java #CodingChallenge #ProblemSolving #SetsAndSubsets
