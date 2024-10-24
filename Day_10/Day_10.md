# Day 10 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 10** of my **100 Days of Code Challenge**! Today, I implemented a Java program that calculates the **factorial** of a given number. This problem helped me practice **recursive** and **iterative** approaches to solving problems in Java.

## ✅ What I did today
- Implemented a Java program to calculate the **factorial** of a number.
- Practiced using both **recursive** and **iterative** methods to solve the problem.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Recursion, Loops, Factorial Calculation

## 🔗 Links to Code
- [Day 10 Code Repository](https://github.com/kiranreddy4433E/Day_10/blob/main/pro_22.java): This repository contains the code solution for finding the factorial of a number.

## 📖 Problem Description
- The task is to take an integer as input and calculate its **factorial**.
- The factorial of a number \(n\) is calculated as:
  \[
  n! = n \times (n-1) \times (n-2) \times \ldots \times 1
  \]
  - Example:
    - \(5! = 5 \times 4 \times 3 \times 2 \times 1 = 120\)
    - \(0! = 1\) (by definition)

### Input/Output Example:
  - Input: `5`
    - Output: `The factorial of 5 is 120`
  
  - Input: `0`
    - Output: `The factorial of 0 is 1`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_22 {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Enter number:- ");
		int num = input.nextInt();	
		int factorial = 1;
		for (int i=num; i>0; i--) {
			factorial *= i;
		}
		System.out.println("factorial of number is :- " + factorial);
		input.close();

	}

}

```
---

### 🖥️ Program Output

- Enter number:- 
- 4
- factorial of number is :- 24

- Enter number:- 
- 8
- factorial of number is :- 40320

---

### 📚 Lessons Learned
Learned how to calculate the factorial of a number using both recursive and iterative approaches.
Reinforced my understanding of recursive functions, particularly the importance of base cases.
Practiced using loops to implement an iterative solution for calculating factorial.

---

### ⚡ Challenges
The main challenge was ensuring that the recursion terminates correctly with the base case to avoid a stack overflow error.

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---

100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
