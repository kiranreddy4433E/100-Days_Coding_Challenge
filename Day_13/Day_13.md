 ### Day 13 of 100 - 100 Days of Code Challenge
---
## 📝 Overview
Welcome to **Day 13** of my **100 Days of Code Challenge**! Today, I implemented a Java program that calculates the **sum of N natural numbers** using a mathematical formula. This problem helped me explore efficient ways to solve summation problems with minimal iterations.
---
## ✅ What I did today
- Wrote a Java program to calculate the **sum of N natural numbers** using the formula:
  \[
  \text{Sum of N} = \frac{n(n+1)}{2}
  \]
- Practiced using **integer arithmetic** and handling **user input**.
---
## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arithmetic Operations, Input Handling
---
## 📖 Problem Description
- The task is to take an integer `n` as input and calculate the **sum of N natural numbers** using the formula:
  \[
  \text{Sum of N} = \frac{n(n+1)}{2}
  \]
- For example:
  - \( n = 5 \)
    - Sum = \( 1 + 2 + 3 + 4 + 5 = 15 \)
  - \( n = 10 \)
    - Sum = \( 1 + 2 + 3 + \ldots + 10 = 55 \)

### Input/Output Example:
  - Input: `5`
    - Output: `Sum of N natural numbers is 15`
  
  - Input: `10`
    - Output: `Sum of N natural numbers is 55`

---

## 📝 Code Example

```java
package demo;

import java.util.Scanner;

public class demo_3 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        // Taking user input for N
        System.out.println("Enter a number :- ");
        int n = input.nextInt();
        
        // Calculate the sum using the formula
        int sum = (n * (n + 1)) / 2;
        
        // Output the result
        System.out.println("Sum of " + n + " natural numbers is: " + sum);
        
        input.close();
    }
}
```
---

### 🖥️ Program Output
mathematica
Copy code
Enter a number :- 
5
Sum of 5 natural numbers is: 15

Enter a number :- 
10
Sum of 10 natural numbers is: 55
### 📚 Lessons Learned
Learned how to use a simple formula to calculate the sum of natural numbers without looping.
Reinforced the importance of mathematical formulas for optimizing code execution.
Practiced using the Scanner class for taking user input and handling basic arithmetic in Java.
### ⚡ Challenges
Handling large values of n could potentially result in an overflow, so using larger data types (like long) for very large numbers is advisable.
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746
---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
