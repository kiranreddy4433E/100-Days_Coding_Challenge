# Day 80 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 80** of my **100 Days of Code Challenge**! Today's problem involved determining if two people, Alice and Bob, can equally split a collection of animals from a pet store such that they end up with the same multiset of animals.

---

## ✅ Problem Description
### Input:
- \( T \): Number of test cases.
- For each test case:
  - \( N \): Total number of animals in the store.
  - \( A \): An array of integers, where \( A[i] \) represents the type of the \( i \)-th animal.

### Output:
- Print `Yes` if Alice and Bob can equally split the animals into two identical multisets.
- Print `No` otherwise.

---

### Example
#### Input:
Enter a T test cases: 2 Enter a test case: 1 6 1 2 2 1 3 3 Enter a test case: 2 4 1 2 2 3



#### Output:
Yes No


#### Explanation:
- **Test Case 1**: Each animal type appears an even number of times, so it's possible to split.
- **Test Case 2**: The animal of type `1` appears an odd number of times, so it's not possible to split equally.

---

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** HashMaps, Frequency Counters, Arrays

---

## 📖 Code Example

```java
package coading_Challange;

import java.util.*;

public class Day_80 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter a T test cases: ");
        int num = input.nextInt();
        for (int i = 0; i < num; i++) {
            System.out.println("Enter a test case: " + (i + 1));
            int N = input.nextInt(); // Total number of pets
            int animals[] = new int[N];
            for (int j = 0; j < N; j++) {
                animals[j] = input.nextInt();
            }
            if (canSplit(animals)) {
                System.out.println("Yes");
            } else {
                System.out.println("No");
            }
        }
    }

    private static boolean canSplit(int[] animals) {
        Map<Integer, Integer> freq = new HashMap<>();
        for (int animal : animals) {
            freq.put(animal, freq.getOrDefault(animal, 0) + 1);
        }
        for (int count : freq.values()) {
            if (count % 2 != 0) {
                return false;
            }
        }
        return true;
    }
}
🖥️ Program Output
Input:

Enter a T test cases: 
1
Enter a test case: 1
6
1 2 2 1 3 3
Output:

Yes
```
---
## 📚 Lessons Learned
Learned to use HashMaps to track frequency counts in arrays.
Gained practice in solving problems that require checking conditions across array elements.
Improved efficiency in determining split feasibility using frequency analysis.

---
## ⚡ Challenges
Ensuring the program handles edge cases, such as empty arrays or arrays with all identical elements.
Managing large arrays efficiently without exceeding memory or time constraints.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

--- 
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
