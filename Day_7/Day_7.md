# Day 7 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 7** of my **100 Days of Code Challenge**! Today, I implemented a Java program that finds the **number of days in a given month** for a specific year. This problem helped me practice working with **date-related logic**, including **leap year** calculations.

## ✅ What I did today
- Implemented a Java program to calculate the number of days in a month for a given year.
- Worked with **conditional logic** to handle **leap years** and determine the correct number of days in **February**.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Leap Year Calculation, Conditional Statements, Input Handling

## 📖 Problem Description
- The task is to take two inputs: a **month** and a **year**, and return the number of days in that month for the given year. For February, the program should check if the year is a leap year.
- **Input/Output Example**:
  - Input: `February 2020`
    - Output: 29 days (Leap Year)
  
  - Input: `April 2021`
    - Output: 30 days
  
  - Input: `February 2021`
    - Output: 28 days (Non-Leap Year)

---

## 📝 Code Example

```java

 package dsa;

import java.util.Scanner;

public class pro_19 {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Enter month:- ");
		int month = input.nextInt();
		System.out.println("Enter year:- ");
		int year = input.nextInt();
		int leap = (year % 4 == 0 && (year % 100!= 0|| year % 400 == 0))?1:0;
		if (month == 1) {
			System.out.println(31 + "-Days");
		}
		else if (month == 2) {
			if (leap == 1) {
				System.out.println(29 + "-Days");
			}
			else {
				System.out.println(28 + "-Days");
			}
			
		}
		else if(month == 3) {
			System.out.println(31 + "-Days");
		}
		else if(month == 4) {
			System.out.println(30 + "-Days");
		}
		else if(month == 5) {
			System.out.println(31 + "-Days");
		}
		else if(month == 6) {
			System.out.println(30 + "-Days");
		}
		else if (month == 7) {
			System.out.println(31 + "-Days");
		}
		else if(month == 8) {
			System.out.println(31 + "-Days");
		}
		else if(month == 9) {
			System.out.println(30 + "-Days");
		}
		else if(month == 10) {
			System.out.println(31 + "-Days");
		}
		else if(month == 11) {
			System.out.println(30 + "-Days");
		}
		else if(month == 12) {
			System.out.println(31 + "-Days");
		}
		input.close();
	}

}



```
---

### 🖥️ Program Output

- Enter month: 
- 2
- Enter year: 
- 2000
- 29 Days



---

### 📚 Lessons Learned
Learned how to check for leap years and handle February appropriately in the calendar system.
Improved my understanding of switch-case statements and how they can simplify multiple conditions.
Practiced handling integer inputs and implementing basic logic to calculate days in a month.

---

### ⚡ Challenges
The main challenge was ensuring that the leap year logic was correctly implemented, especially for edge cases like the year 2000 (which is a leap year because it's divisible by 400).

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/
- Twitter: @kiran4746

---

100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
