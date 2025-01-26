# Day 98: Minimum Breakfast Adjustments

## 📝 Problem Description

Arun works at the "Fat Hut" restaurant, where there are `N` breakfasts. Each breakfast has:
- **Attractiveness**: `Ai`
- **Cost**: `Ci`

Customers avoid breakfast `j` if there exists a breakfast `i` such that:
- `Ai >= Aj` **and** `Ci < Cj`

Arun wants to ensure that every breakfast has a chance of being taken. While he cannot change the costs, he can adjust the **attractiveness** of a breakfast to fall within the range `[Li, Ri]`. 

### Goal
Minimize the number of breakfasts whose attractiveness needs to be adjusted.

---

## 🚀 Approach

### Key Observations
1. A breakfast `j` is ignored if:
   - Another breakfast `i` has both **higher or equal attractiveness** and **lower cost**.
2. To minimize adjustments:
   - **Prioritize cost**: Sort breakfasts by cost in ascending order.
   - Adjust attractiveness **only if required** to ensure it does not violate the rules.

### Steps:
1. **Input Parsing**:
   - Read the number of breakfasts, their attributes (`Ai`, `Ci`, `Li`, `Ri`).

2. **Sort by Cost**:
   - Sorting ensures that cheaper breakfasts are processed first.

3. **Adjust Attractiveness**:
   - Track the maximum attractiveness processed so far (`maxAttr`).
   - If the current breakfast's attractiveness is less than `maxAttr`:
     - Adjust it to lie within `[maxAttr, Ri]`.
     - Count this adjustment.

4. **Output the Result**:
   - Print the minimum number of adjustments required.

---

## 💻 Code

```java
package coading_Challange;

import java.util.*;

public class Day_98 {

    static class Breakfast {
        long attr, cost, l, r;

        Breakfast(long attr, long cost, long l, long r) {
            this.attr = attr;
            this.cost = cost;
            this.l = l;
            this.r = r;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int T = sc.nextInt(); // Number of test cases

        while (T-- > 0) {
            int n = sc.nextInt(); // Number of breakfasts
            Breakfast[] breakfasts = new Breakfast[n];

            // Input all breakfasts
            for (int i = 0; i < n; i++) {
                long a = sc.nextLong(); // Current attractiveness
                long c = sc.nextLong(); // Cost
                long l = sc.nextLong(); // Min allowed attractiveness
                long r = sc.nextLong(); // Max allowed attractiveness
                breakfasts[i] = new Breakfast(a, c, l, r);
            }

            // Solve the problem for this test case
            int result = minimizeAdjustments(breakfasts, n);
            System.out.println(result);
        }

        sc.close();
    }

    private static int minimizeAdjustments(Breakfast[] breakfasts, int n) {
        // Sort by cost in ascending order
        Arrays.sort(breakfasts, Comparator.comparingLong(b -> b.cost));

        long maxAttr = 0;
        int adjustments = 0;

        // Iterate over sorted breakfasts
        for (int i = 0; i < n; i++) {
            long currentAttr = breakfasts[i].attr;
            long l = breakfasts[i].l;
            long r = breakfasts[i].r;

            if (currentAttr < maxAttr) {
                // Try to adjust the current attractiveness
                if (r < maxAttr) {
                    // Impossible to adjust within the allowed range
                    return -1;
                } else {
                    // Adjust to the maximum allowed value
                    currentAttr = Math.max(currentAttr, maxAttr);
                    currentAttr = Math.min(currentAttr, r);
                    adjustments++;
                }
            }

            maxAttr = Math.max(maxAttr, currentAttr);
        }

        return adjustments;
    }
}
🔍 Input/Output Examples
Example 1
Input:

1
3
10 5 8 12
9 6 8 10
12 4 10 14
Output:
=
1
Explanation:

After sorting by cost: (12, 4, [10, 14]), (10, 5, [8, 12]), (9, 6, [8, 10]).
Adjust the second breakfast to attractiveness 12.
Only 1 adjustment is required.
Example 2
Input:

1
2
10 4 5 12
8 3 7 11
Output:

0
Explanation:

After sorting by cost: (8, 3, [7, 11]), (10, 4, [5, 12]).
No adjustments are required.
```
---
## 🧠 Key Learnings
Sorting:

Sorting by cost simplifies the process of checking and adjusting attractiveness values.
Greedy Approach:

Adjust only when necessary to maintain minimal operations.
Edge Cases:

Ensure valid intervals [Li, Ri] for adjustments.

---
## 💡 Next Steps
Explore dynamic programming extensions for similar problems.
Tackle problems with more complex constraints on intervals and sorting.

---
## 🤝 Let's Connect!
Feel free to reach out for questions or discussions! 😊

---
## #100DaysOfCode #Java #GreedyAlgorithm #Sorting #ProblemSolving
