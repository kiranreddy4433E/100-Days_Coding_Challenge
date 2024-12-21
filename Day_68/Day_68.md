# Day 68 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 68** of my **100 Days of Code Challenge**! Today, I implemented a Java program to handle operations on a set based on queries. The program supports adding elements, removing elements, and checking for the presence of elements in a set.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple queries.
  2. For each query:
     - Add an element to the set.
     - Remove an element from the set if it exists.
     - Check if an element is present in the set and print `"Yes"` or `"No"`.
  3. Display the final state of the set.
- Practiced using Java's `HashSet` for efficient element operations.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** HashSet, Set Operations, Conditional Statements

## 📖 Problem Description
- **Input**:
  - `Q`: Number of queries.
  - For each query:
    - `n`: Type of operation (1, 2, or 3).
      - `1 x`: Add `x` to the set.
      - `2 x`: Remove `x` from the set.
      - `3 x`: Check if `x` is in the set and print `"Yes"` or `"No"`.
- **Output**:
  - For each query of type `3`, print `"Yes"` if the number is in the set, otherwise print `"No"`.
  - Display the final state of the set.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter a T number of test cases: 5 1 5 1 10 3 5 2 10 3 10


**Output**:
Yes No [5]


#### Example 2:
**Input**:
Enter a T number of test cases: 4 1 3 3 3 2 3 3 3



**Output**:
Yes No []



---

## 📝 Code Example

```java
package coading_Challange;

import java.util.*;

public class Day_68 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Enter a T number of test cases: ");
        int Q = input.nextInt(); // Number of queries

        // Create a set to store unique integers
        Set<Integer> set = new HashSet<>();

        // Process each query
        for (int i = 0; i < Q; i++) {
            int n = input.nextInt(); // Type of operation
            int num = input.nextInt(); // Number to operate on

            if (n == 1) {
                // Add number to the set
                set.add(num);
            } else if (n == 2) {
                // Remove number from the set if present
                set.remove(num);
            } else if (n == 3) {
                // Check if the number is present in the set
                if (set.contains(num)) {
                    System.out.println("Yes");
                } else {
                    System.out.println("No");
                }
            }
        }

        // Display the final state of the set
        System.out.println(set);

        input.close();
    }
}
🖥️ Program Output
Example 1:

Enter a T number of test cases: 
5
1 5
1 10
3 5
2 10
3 10
Yes
No
[5]
Example 2:

Enter a T number of test cases: 
4
1 3
3 3
2 3
3 3
Yes
No
```
---
## 📚 Lessons Learned
Learned the usage of Java's HashSet for efficient add, remove, and contains operations.
Practiced processing multiple queries with different types of operations.
Improved understanding of set manipulation and its applications in problem-solving.

---
## ⚡ Challenges
Ensuring that the remove operation handles cases where the element is not in the set.
Managing input for different query types efficiently.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746
---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
