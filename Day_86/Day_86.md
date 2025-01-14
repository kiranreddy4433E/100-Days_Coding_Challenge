# Day 86 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 86** of my **100 Days of Code Challenge**! Today, I solved a unique and challenging problem involving **subsets** and **rebuilding an array** from given subset sums. This problem required using concepts of **frequency maps**, **set theory**, and **combinatorics**.

---

## ✅ Problem Description
Mahesh received a beautiful array \( A \) of size \( N \) as a birthday gift. He loved it so much that he calculated all possible subsets of \( A \) and wrote down their **sums** on a piece of paper. Unfortunately, Mahesh lost the original array \( A \) but still has the subset sums. 

Your task is to help Mahesh **rebuild the original array \( A \)** given the subset sums.

### Input:
1. \( T \) — Number of test cases
2. For each test case:
   - \( N \) — Size of the original array \( A \)
   - \( 2^N \) subset sums — A list of all subset sums of \( A \)

### Output:
- For each test case, print the reconstructed array \( A \) in non-decreasing order.

---

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Sorting, Subsets, Frequency Map, TreeMap, and ArrayList

---

## 📖 Code Example

```java
package coading_Challange;

import java.util.*;

public class Day_86 {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int T = in.nextInt(); // Number of test cases

        while (T-- > 0) {
            int N = in.nextInt(); // Size of the array A
            int subsetSize = 1 << N; // Total subset sums = 2^N

            // Read the subset sums
            int[] subsetSums = new int[subsetSize];
            for (int i = 0; i < subsetSize; i++) {
                subsetSums[i] = in.nextInt();
            }

            // Sort the subset sums
            Arrays.sort(subsetSums);

            // Multiset to store frequency of each subset sum
            Map<Integer, Integer> frequencyMap = new TreeMap<>();
            for (int sum : subsetSums) {
                frequencyMap.put(sum, frequencyMap.getOrDefault(sum, 0) + 1);
            }

            // Remove the empty subset (0 sum) from the map
            frequencyMap.put(0, frequencyMap.get(0) - 1);
            if (frequencyMap.get(0) == 0) {
                frequencyMap.remove(0);
            }

            List<Integer> result = new ArrayList<>();

            for (int i = 0; i < N; i++) {
                // Get the smallest non-zero element from the map
                int smallest = frequencyMap.keySet().iterator().next();
                result.add(smallest);

                // Update the frequency map by removing all subsets that include this element
                List<Integer> newSubsets = new ArrayList<>();
                for (int x : result) {
                    newSubsets.add(smallest + x);
                }

                // Update frequency map safely
                for (int subsetSum : newSubsets) {
                    if (frequencyMap.containsKey(subsetSum)) {
                        frequencyMap.put(subsetSum, frequencyMap.get(subsetSum) - 1);
                        if (frequencyMap.get(subsetSum) == 0) {
                            frequencyMap.remove(subsetSum);
                        }
                    }
                }
            }

            // Sort the result to maintain non-decreasing order
            Collections.sort(result);
            for (int num : result) {
                System.out.print(num + " ");
            }
            System.out.println();
        }
        in.close();
    }
}
🖥️ Program Output
Input:

2
3
0 1 1 2 2 2 3 4
2
0 5 5 10
Output:

1 1 2
5 5
```
---
## 📚 Lessons Learned
Learned how to use TreeMap to efficiently manage frequency maps for updating subset sums.
Gained deeper insight into subsets, bitmasking, and their applications.
Improved my understanding of rebuilding structures (like arrays) from derived data.

---
## ⚡ Challenges
Efficiently handling the frequency map while removing elements corresponding to each subset sum.
Ensuring that all subsets are accounted for in the correct order.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

--- 
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
