# Day 26 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 26** of my **100 Days of Code Challenge**! Today, I implemented a Java program that calculates the **maximum number of handshakes** among a group of people. This problem was a great way to explore combinatorial mathematics and iterative loops.

## ✅ What I did today
- Wrote a Java program to calculate the maximum number of unique handshakes possible with a given number of people.
- Practiced implementing loops and applying mathematical formulas in Java.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Combinatorics, Summation

## 📖 Problem Description
- For `n` people in a room, the task is to find the maximum number of unique handshakes that can occur if each person shakes hands with every other person exactly once. The formula used to find the maximum number of handshakes is:
  \[
  \text{Handshakes} = \frac{n \times (n - 1)}{2}
  \]
  For example:
  - For `5` people, the maximum handshakes are `10`.

### Input/Output Example:
  - **Input**: `5`
  - **Output**:
    ```
    Maximum Number of Handshakes: 10
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_38 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter the number of people: ");
        int num = input.nextInt();
        
        // Calculate the maximum number of handshakes
        int handshakes = (num * (num - 1)) / 2;
        
        // Print the result
        System.out.println("Maximum Number of Handshakes: " + handshakes);
        
        input.close();
    }
}
```
---
### 🖥️ Program Output

- Enter the number of people: 
- 5
- Maximum Number of Handshakes: 10

---
### 📚 Lessons Learned
- Practiced using combinatorial formulas in Java.
- Reinforced my understanding of how loops and mathematical expressions can simplify real-world problems.

---
### ⚡ Challenges
Ensuring the program applied the correct formula and that calculations were accurate, especially for larger values of n.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
