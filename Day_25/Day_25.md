# Day 25 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 25** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate the **area of a circle** given its radius. This exercise helped me practice using constants and applying mathematical formulas in Java.

## ✅ What I did today
- Wrote a Java program to calculate the area of a circle using the formula:
  \[
  \text{Area} = \pi \times \text{radius}^2
  \]
- Practiced working with variables and constants in Java.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Mathematical Calculations, Variables, Constants

## 📖 Problem Description
- The task is to compute the area of a circle given its radius. For example:
  - If the radius is `5`, the area will be \( \pi \times 5^2 = 78.5 \) (using \(\pi \approx 3.14\)).

### Input/Output Example:
  - **Input**: `5`
  - **Output**:
    ```
    Area of the circle with radius 5 is: 78.5
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_37 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.println("Enter the radius of the circle: ");
        int radius = input.nextInt();
        
        // Calculate the area of the circle
        float pi = 3.14f;
        float area = pi * radius * radius;
        
        // Print the result
        System.out.println("Area of the circle with radius " + radius + " is: " + area);
        
        input.close();
    }
}
```
---
### 🖥️ Program Output

- Enter the radius of the circle: 
- 5
- Area of the circle with radius 5 is: 78.5

--- 
### 📚 Lessons Learned
Practiced using mathematical formulas to calculate areas.
Gained a better understanding of variable declaration and the use of constants in Java.

---
### ⚡ Challenges
Ensuring accuracy with floating-point calculations, particularly when using constants like 
- 𝜋
- π

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
