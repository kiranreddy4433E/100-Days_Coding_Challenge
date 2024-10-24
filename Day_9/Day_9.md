# Day 9 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 9** of my **100 Days of Code Challenge**! Today, I wrote a Java program that calculates the **number of digits** in a given integer input from the user. This task helped me practice handling user input, working with loops and basic mathematical operations in Java.

## ✅ What I did today
- Implemented a Java program that takes an integer input and calculates the number of digits in that input.
- Improved my understanding of how to use **loops** and **integer division** to count digits.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Input Handling, Integer Division, String Length

## 📖 Problem Description
- The task is to take an integer input from the user and calculate how many digits the number contains. The program should work for both positive and negative numbers.
  
### Input/Output Example:
  - Input: `12345`
    - Output: `The number of digits is 5`
  
  - Input: `-456`
    - Output: `The number of digits is 3`
  
  - Input: `0`
    - Output: `The number of digits is 1`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_21 {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		int num = input.nextInt();
		int count = 0;
		if(num==0)
		System.out.print("Number of Digits = 1");
		else{
		while(num != 0)
		{
		count++;
		num = num / 10;
		}
		System.out.print("Number of Digits is "+count);
		}

	}

}

```

### 🖥️ Program Output

3241
Number of Digits is 4

6
Number of Digits is 1

---

### 📚 Lessons Learned
Learned how to convert integers to strings and count the number of digits using String.length().
Practiced handling negative numbers using Math.abs() to work with absolute values.
Explored how to handle user input with the Scanner class in Java.

---

### ⚡ Challenges
The challenge was correctly handling negative numbers and ensuring that the minus sign (-) is not counted as a digit.
Another challenge was handling the edge case of 0, which should correctly be counted as one digit.

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/
- Twitter: @kiran4746
---
100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
