# Day 6 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 6** of my **100 Days of Code Challenge**! Today, I implemented a Java program that determines which **quadrant** a point (x, y) lies in based on its coordinates. This problem helped me understand **coordinate geometry** and reinforced my knowledge of **conditional statements** in Java.

## ✅ What I did today
- Implemented a Java program to determine the quadrant of a point in the coordinate system based on the (x, y) values.
- Practiced using **conditional logic** to evaluate the sign of the x and y coordinates to find the correct quadrant.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Conditional Statements, Coordinate Geometry

## 📖 Problem Description
- The task is to take two inputs (x and y coordinates) and determine which quadrant the point lies in.
- **Input/Output Example**:
  - Input: `(4, 5)`
    - Output: First Quadrant (x > 0, y > 0)
  
  - Input: `(-3, 7)`
    - Output: Second Quadrant (x < 0, y > 0)

  - Input: `(-6, -4)`
    - Output: Third Quadrant (x < 0, y < 0)
  
  - Input: `(5, -8)`
    - Output: Fourth Quadrant (x > 0, y < 0)

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_18 {

	public static void main(String[] args) {		
		Scanner input = new Scanner(System.in);
		System.out.println("Enter co-ordinates");
		int x = input.nextInt();
		int y = input.nextInt();
		if (x>0 && y>0) {
			System.out.println(x +" "+ y + " The point lies in first quadrant");
		}
		else if(x<0 && y>0) {
			System.out.println(x +" "+ y + " The point lies in second quadrant");
		}
		else if(x>0 && y>0) {
			System.out.println(x +" "+ y + " The point lies in third quadrant");
		}
		else {
			System.out.println(x +" "+ y + " The point lies in third quadrant");
		}
		input.close();

	}

}

```

### 🖥️ Program Output

- Enter the x coordinate: 4
- Enter the y coordinate: 5
- The point lies in the First Quadrant.

- Enter the x coordinate: -3
- Enter the y coordinate: 7
- The point lies in the Second Quadrant.

- Enter the x coordinate: 0
- Enter the y coordinate: 5
- The point lies on the y-axis.

- Enter the x coordinate: 0
- Enter the y coordinate: 0
- The point is at the origin.
---
### 📚 Lessons Learned
Reinforced my understanding of conditional statements in Java and how to use them to check multiple conditions in a coordinate system.
Learned more about coordinate geometry and how to classify points based on their location in different quadrants.

---

### ⚡ Challenges
Had to carefully handle special cases where the point lies on one of the axes or at the origin.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
