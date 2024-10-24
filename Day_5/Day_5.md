# Day 5 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 5** of my **100 Days of Code Challenge**! Today, I implemented a simple Java program that checks whether a given number is **even** or **odd**. This exercise allowed me to further strengthen my knowledge of **conditional statements** and handling **integer inputs** in Java.

## ✅ What I did today
- Wrote a Java program to check if a number is **even** or **odd**.
- Practiced using the **modulus operator** (`%`) to determine whether a number is divisible by 2.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Conditional Statements, Modulus Operator, Input Handling

## 📖 Problem Description
- The task is to take a number as input and determine if the number is even or odd.
- **Input/Output Example**:
  - Enter a Number: `12`
    - Output: Even Number
  
  - Enter a Number: `7`
    - Output: Odd Number

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_17 {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Enter a number");
		char ch = input.next().charAt(0);
		if (ch%2 == 0) {
			System.out.println("Even");
		}
		else {
			System.out.println("Odd");
		}
		input.close();

	}

}

```

### 🖥️ Program Output
- Enter a number
- 5
- Odd

- Enter a number
- 10
- Even

### 📚 Lessons Learned
Reinforced my knowledge of using conditional statements in Java, such as if-else.
Gained further experience handling integer inputs and using the modulus operator (%) to check divisibility by 2.

### ⚡ Challenges
Initially faced an issue with handling negative numbers but resolved it by testing with both positive and negative inputs.
📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

---

100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
