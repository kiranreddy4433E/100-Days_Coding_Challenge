# Day 3 of 100 - 100 Days of Code Challenge

## Overview
Welcome to **Day 3** of my **100 Days of Code Challenge**! Today, I worked on a Java program to find the **ASCII values for alphabets**. This exercise helped me understand character-to-ASCII conversions in Java.

## What I did today
- Solved the problem of determining the **ASCII values** for input alphabet characters.
- Practiced **data type conversion** and handling **character inputs**.

## Technologies Used
- **Programming Language:** Java
- **Concepts:** ASCII values, Character data types, Input/Output handling in Java

## Links to Code
- [Day 3 Code pro_12.java](#https://github.com/kiranreddy4433E/day3/blob/main/pro_12.java): This repository contains the code solution for the ASCII value problem.

## Lessons Learned
- Learned how to use Java to convert **characters** into their **ASCII values**.
- Improved my understanding of **character data types** and their corresponding integer values in Java.
- Practiced using the **Scanner class** for input and output in Java.

## Challenges
- Faced minor issues when handling non-alphabetic characters, but resolved them with input validation.

## Connect with me
- **Email:** [kiranreddy4746@gmail.com](mailto:kiranreddy4746@gmail.com)
- **LinkedIn:** [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- **Twitter:** [@kiran4746](https://twitter.com/kiran4746)

---


**[100 Days of Code](https://www.100daysofcode.com/)** is a challenge created by Ajinka Kulakarni, Amit Prabhu. You can find more information about it and join the community using the hashtag `#100DaysOfCode` on Linked in.

## Code Example

```java
package dsa;
import java.util.Scanner;
public class pro_12 {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Enter a  character");
		char ch = input.next().charAt(0);
		System.out.println("you entered character :- " + ch);
		int asciiValue = ch ;
		System.out.println("The ASCII value of " + ch + " is = " + asciiValue);		
	}
}


```
----

## Problem Description
- The problem I worked on today was to create a program that takes a single alphabet character as input and prints its corresponding **ASCII value**.
- **Input/Output Example**:
  - Input: `B`
  - Output: `66`
  - Input: `b`
  - Output: `98`
