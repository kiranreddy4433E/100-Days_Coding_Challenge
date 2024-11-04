# Day 24 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 24** of my **100 Days of Code Challenge**! Today, I implemented a Java program to print a **pyramid pattern** using stars (`*`). This exercise helped me understand nested loops and how to control alignment for creating a symmetrical pattern.

## ✅ What I did today
- Created a Java program to print a pyramid pattern based on user input.
- Practiced using nested loops and alignment techniques for pattern printing.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Pattern Printing, Nested Loops

## 📖 Problem Description
- The task is to generate a pyramid pattern with stars based on the number of rows specified by the user. For example, if the user inputs `4`, the pyramid will look like this:
markdown
Copy code
 *
* *
csharp
Copy code

### Input/Output Example:
- **Input**: `4`
- **Output**:
  ```
  *
  * *
  * * *
  * * * *
  ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_36 {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Enter a number:- ");
		int num = input.nextInt();
		for (int i=num; i>0; i--) {
			for (int j=i; j<=num; j++) {
				System.out.print(" *");
			}
			System.out.println( " ");
		}
		input.close();
	}

}

```
---
### 🖥️ Program Output
```
- Enter the number of rows:
- 4
- * 
- * * 
- * * * 
- * * * *
```
--- 
### 📚 Lessons Learned
Practiced using nested loops to manage structure and alignment for pattern creation.
Reinforced my understanding of row and space management to achieve symmetrical output.

---
### ⚡ Challenges
Aligning spaces precisely to create the correct pyramid shape required adjusting loop conditions.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
