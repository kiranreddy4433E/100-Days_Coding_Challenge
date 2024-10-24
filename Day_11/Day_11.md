# Day 11 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 11** of my **100 Days of Code Challenge**! Today, I implemented a Java program that generates the **Fibonacci series**. This problem helped me understand how to implement both **iterative** and **recursive** approaches for generating the Fibonacci sequence.

## ✅ What I did today
- Wrote a Java program to generate the Fibonacci series up to a specified number of terms.
- Implemented both **recursive** and **iterative** methods to generate the Fibonacci sequence.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Recursion, Iteration, Fibonacci Sequence

## 🔗 Links to Code
- [Day 11 Code Repository](https://github.com/kiranreddy4433E/Day_11/blob/main/pro_23.java): This repository contains the code solution for generating the Fibonacci series.

## 📖 Problem Description
- The task is to generate the **Fibonacci series** up to a specified number of terms. The Fibonacci series is defined as:
  \[
  F(0) = 0, \ F(1) = 1, \ F(n) = F(n-1) + F(n-2) \ \text{for} \ n \geq 2
  \]
- The first few terms of the Fibonacci sequence are: `0, 1, 1, 2, 3, 5, 8, 13, 21, ...`

### Input/Output Example:
  - Input: `7`
    - Output: `0 1 1 2 3 5 8`
  
  - Input: `10`
    - Output: `0 1 1 2 3 5 8 13 21 34`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_23 {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Enter a number:- ");
		int num = input.nextInt();
		int n1 = 0, n2 = 1, n3;
		System.out.print(n1+" "+n2);
		for (int i=2; i<num; ++i) {
			n3 = n1+n2; 
			System.out.print(" "+n3);
			n1 = n2;
			n2 = n3;
		}
		input.close();

	}

}

```
---

### 🖥️ Program Output

- Enter a number:- 
- 5
- 0 1 1 2 3
- Enter a number:- 
- 8
- 0 1 1 2 3 5 8 13
---

### 📚 Lessons Learned
Learned how to generate the Fibonacci series using both iteration and recursion.
Reinforced my understanding of recursive functions and how they are useful for problems like Fibonacci.
Practiced using loops for an iterative approach to generate a sequence of numbers.

---

### ⚡ Challenges
The challenge with the recursive approach was ensuring the correct base cases to avoid stack overflow errors for large inputs.
Handling large Fibonacci numbers is easier using the iterative method, which is more efficient compared to recursion.

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---

100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
