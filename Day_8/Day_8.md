# Day 8 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 8** of my **100 Days of Code Challenge**! Today, I implemented a Java program to find the **roots of a quadratic equation**. This exercise helped me strengthen my knowledge of mathematical computations and working with the **quadratic formula**.

## ✅ What I did today
- Wrote a Java program to find the **roots** of a quadratic equation using the quadratic formula.
- Improved my understanding of **discriminants** and how they determine the nature of the roots.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Quadratic Equation, Discriminant, Math.sqrt(), Conditional Logic

## 🔗 Links to Code
- [Day 8 Code Repository](https://github.com/kiranreddy4433E/Day_8/blob/main/pro_20.java): This repository contains the code solution for finding the roots of a quadratic equation.

## 📖 Problem Description
- The task is to find the **roots of a quadratic equation** of the form `ax^2 + bx + c = 0`.
- The roots are calculated using the **quadratic formula**:
  \[
  x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
  \]
- Depending on the **discriminant** (`b^2 - 4ac`), the equation may have:
  - Two real roots
  - One real root (if the discriminant is zero)
  - No real roots (if the discriminant is negative)

### Input/Output Example:
  - Input: `a = 1`, `b = -7`, `c = 12`
    - Output: Two Real Roots: `x1 = 4.0`, `x2 = 3.0`
  
  - Input: `a = 1`, `b = -6`, `c = 9`
    - Output: One Real Root: `x = 3.0`
  
  - Input: `a = 1`, `b = 2`, `c = 5`
    - Output: No Real Roots (Imaginary roots)

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_20 {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		int a = input.nextInt();
		int b = input.nextInt();
		int c = input.nextInt();
		double decrement = ((b*b)-(4*a*c));
		double x_1 = ((-b+Math.sqrt(decrement))/2*a);
		double x_2 = ((-b-Math.sqrt(decrement))/2*a);
		if (x_1 == x_2) {
			System.out.println("The roots are Equal");
			System.out.println("The roots are :- "+x_1);
		}
		else {
		System.out.println("The roots are :- "+x_1);
		System.out.println("The roots are :- "+x_2);
		}
		input.close();

	}

}

```

### 🖥️ Program Output
- 1
- -6
- 9
- The roots are Equal
- The roots are :- 3.0

---

### 📚 Lessons Learned
Strengthened my understanding of the quadratic formula and how to compute the roots of a quadratic equation.
Practiced working with the discriminant to determine if the equation has real or imaginary roots.
Enhanced my skills in using the Math.sqrt() function for square root calculations in Java.

---

### ⚡ Challenges
The main challenge was handling imaginary roots and ensuring the correct implementation of complex numbers when the discriminant was negative.

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/
- Twitter: @kiran4746

---
100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
