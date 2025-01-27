# Day 99: Minimum Cleaning Time for a Hallway

## 📝 Problem Description

There is a hallway of length \( N-1 \) that needs to be cleaned. You have \( M \) workers, and each worker is responsible for cleaning a specific segment \([L_i, R_i]\) of the hallway. 

### Worker Constraints:
1. Each worker can clean continuously within their assigned segment.
2. Workers cannot skip portions of their segment or jump between segments.
3. All \( N-1 \) units of the hallway must be cleaned, and the segments might overlap.

### Objective:
Find the **minimum time required** to clean the hallway if all workers work simultaneously.

---

## 🚀 Approach

### Key Observations:
1. **Sorting by Starting Point**:
   - Sorting workers' segments by their starting points (and by their ending points if starting points are the same) allows for an efficient traversal of overlapping intervals.

2. **Tracking Coverage**:
   - Use a variable `coveredEnd` to track the furthest point of the hallway that has been cleaned.
   - Continuously extend the coverage using the workers' segments.

3. **Maximize Efficiency**:
   - For every interval used to extend coverage, calculate the time it takes for that worker to clean their segment. Track the maximum cleaning time among all intervals, as this determines the minimum time required.

4. **Incomplete Coverage**:
   - If, at any point, there are no workers available to extend coverage, the hallway cannot be fully cleaned, and the result is `-1`.

---

## 💻 Code

```java
package coading_Challange;

import java.util.*;

public class Day_99 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int T = sc.nextInt(); // Number of test cases

        while (T-- > 0) {
            int N = sc.nextInt(); // Length of the hallway
            int M = sc.nextInt(); // Number of workers

            int[][] workers = new int[M][2];
            for (int i = 0; i < M; i++) {
                workers[i][0] = sc.nextInt();
                workers[i][1] = sc.nextInt();
            }

            System.out.println(minimumCleaningTime(N, workers));
        }
        sc.close();
    }

    private static int minimumCleaningTime(int N, int[][] workers) {
        // Sort intervals by their starting point, and if equal, by their ending point
        Arrays.sort(workers, (a, b) -> (a[0] == b[0] ? Integer.compare(a[1], b[1]) : Integer.compare(a[0], b[0])));

        int coveredEnd = 0; // Tracks the end of the covered range
        int maxSegmentLength = 0; // Maximum time required
        int i = 0, M = workers.length;

        while (coveredEnd < N - 1) {
            int newCoveredEnd = coveredEnd;

            // Extend the coverage as much as possible
            while (i < M && workers[i][0] <= coveredEnd + 1) {
                newCoveredEnd = Math.max(newCoveredEnd, workers[i][1]);
                maxSegmentLength = Math.max(maxSegmentLength, workers[i][1] - workers[i][0] + 1);
                i++;
            }

            // If no extension is possible, the hallway cannot be fully covered
            if (newCoveredEnd == coveredEnd) {
                return -1;
            }

            coveredEnd = newCoveredEnd;
        }

        return maxSegmentLength;
    }
}
🔍 Input/Output Examples
Example 1
Input:

1
10 3
1 5
6 10
4 7
Output:

5
```
---
## Explanation:

- Workers clean the hallway in segments [1, 5], [4, 7], and [6, 10].
- The minimum time is determined by the longest segment cleaned by a single worker, which is 5.

---
## 🧠 Key Learnings
- Sorting Intervals:

- Sorting intervals simplifies problems involving overlapping segments, as it enables efficient traversal.
- Greedy Approach:

- Extend the coverage as much as possible at each step to minimize the number of workers needed or the time required.
- Edge Case Handling:

- Properly handle cases where the hallway cannot be fully covered.

---
## 💡 Next Steps
- Explore advanced interval problems with additional constraints.
- Dive deeper into optimization techniques for scheduling and resource allocation.

---
## 🤝 Let's Connect!
- Feel free to reach out for questions or discussions! 😊

## #100DaysOfCode #Java #GreedyAlgorithms #ProblemSolving
