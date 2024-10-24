# Day 4 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 4** of my **100 Days of Code Challenge**! Today, I implemented a simple Java program that checks whether a given number is **positive** or **negative**. This exercise helped me practice basic conditional statements and input handling in Java.

## ✅ What I did today
- Implemented a Java program that checks if a number is **positive**, **negative**, or **zero**.
- Improved my understanding of handling **conditional logic** in Java.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Conditional Statements, Input Handling

## 📖 Problem Description
- The task is to take a number as input and determine if the number is positive, negative, or zero.
- **Input/Output Example**:
  - Enter a Number: `-10`
    - Output: Negative Number
  
  - Enter a Number: `0`
    - Output: Neither Positive Nor Negative
  
  - Enter a Number: `15`
    - Output: Positive Number
---
  
**[100 Days of Code](https://www.100daysofcode.com/)** is a challenge created by Ajinka Kulakarni, Amit Prabhu. You can find more information about it and join the community using the hashtag `#100DaysOfCode` on Linked in.

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_14 {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Enter a Number");
		int num = input.nextInt();
	    if(num == 0) {
			System.out.println("The given number is neither positive nor negative: " + num);
		}
	    else if (num > 0) {
			System.out.println("The given number is positive: " + num);
		}
		else {
			System.out.println("The given number is negative: " + num);
		}
	    input.close();
	}
}
