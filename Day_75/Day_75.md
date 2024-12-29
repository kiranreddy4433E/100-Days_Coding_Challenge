# Day 75 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 75** of my **100 Days of Code Challenge**! Today, I worked on solving a problem to determine if a candy of a given length \( N \) can be completely eaten in bites of length \( K \). The challenge involves verifying whether \( N \) is divisible by \( K \), and if so, calculating the exact number of bites required.

## ✅ What I did today
- Designed a Java program to:
  1. Take the length of the candy (\( N \)) and the bite size (\( K \)) as input.
  2. Determine if \( N \) can be evenly divided into bites of \( K \).
  3. Calculate the number of bites if the candy can be completely eaten, or return `-1` otherwise.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Modulus Operation, Conditional Statements, Input Handling

## 📖 Problem Description
- **Input**:
  - \( T \): Number of test cases.
  - For each test case:
    - \( N \): Length of the candy.
    - \( K \): Length of each bite.
- **Output**:
  - If the candy can be eaten completely, print the number of bites required.
  - If the candy cannot be eaten completely, print `-1`.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter a T test case: 3 8 2 5 3 9 3


**Output**:
4 -1 3


#### Explanation:
1. **Test Case 1**: \( N = 8, K = 2 \). The candy can be evenly divided into \( 8 / 2 = 4 \) bites.
2. **Test Case 2**: \( N = 5, K = 3 \). The remaining candy length is less than \( K \) after one bite, so the result is `-1`.
3. **Test Case 3**: \( N = 9, K = 3 \). The candy can be evenly divided into \( 9 / 3 = 3 \) bites.

---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_75 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter a T test case:- ");
        int num = input.nextInt();
        
        for (int i = 0; i < num; i++) {
            int N = input.nextInt(); // Length of the candy
            int K = input.nextInt(); // Bite size
            
            if (N == 0) {
                System.out.println("0"); // No candy to eat
            } else if (K > N || N % K != 0) {
                System.out.println("-1"); // Cannot divide evenly
            } else {
                System.out.println(N / K); // Number of bites required
            }
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Enter a T test case: 
3
Enter N and K for test case 1:
8 2
4
Enter N and K for test case 2:
5 3
-1
Enter N and K for test case 3:
9 3
3
```
---
## 📚 Lessons Learned
Gained a deeper understanding of modulus and integer division operations for problem-solving.
Practiced handling conditional logic to address various edge cases (e.g., 
𝑁
=
0
N=0, 
𝐾
>
𝑁
K>N).
Strengthened input-handling skills in scenarios with multiple test cases.

---
## ⚡ Challenges
Addressing cases where 
𝑁
=
0
N=0 or 
𝐾
>
𝑁
K>N to ensure the output adheres to problem constraints.
Managing test cases with large values of 
𝑁
N and 
𝐾
K to confirm the solution scales efficiently.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
