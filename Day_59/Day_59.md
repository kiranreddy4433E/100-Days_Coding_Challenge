# Day 59 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 59** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate the **Body Mass Index (BMI)** and classify it into specific categories based on the value. This task enhanced my understanding of conditional logic and mathematical calculations.

## ✅ What I did today
- Wrote a Java program to:
  1. Input the height (`H` in meters) and mass (`M` in kilograms) of Anusree for multiple test cases.
  2. Compute the **BMI** using the formula:
     \[
     \text{BMI} = \frac{M}{H^2}
     \]
  3. Categorize the BMI into:
     - **Category 1**: Underweight (BMI ≤ 18)
     - **Category 2**: Normal weight (19 ≤ BMI ≤ 24)
     - **Category 3**: Overweight (25 ≤ BMI ≤ 29)
     - **Category 4**: Obesity (BMI ≥ 30)
  4. Print the category number for each test case.
- Practiced loops and floating-point calculations.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Conditional Statements, Loops, Mathematical Operations

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `M`: Mass in kilograms.
    - `H`: Height in meters.
- **Output**:
  - For each test case, print the category number corresponding to the calculated BMI.

---

### Input/Output Example:

#### Example 1:
**Input**:
Number of test cases: 2 Enter M (kgs) and H (mts) for test case 1: 60 2 Enter M (kgs) and H (mts) for test case 2: 75 1


**Output**:
1 4



#### Example 2:
**Input**:
Number of test cases: 1 Enter M (kgs) and H (mts) for test case 1: 70 1.8



**Output**:
2



---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_59 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Number of test cases (T): ");
        int T = input.nextInt();

        for (int i = 0; i < T; i++) {
            System.out.println("Enter M (kgs) and H (mts) for test case " + (i + 1) + ": ");
            int M = input.nextInt();
            int H = input.nextInt();

            double BMI = M / Math.pow(H, 2);

            if (BMI <= 18) {
                System.out.println("1"); // Underweight
            } else if (BMI >= 19 && BMI <= 24) {
                System.out.println("2"); // Normal weight
            } else if (BMI >= 25 && BMI <= 29) {
                System.out.println("3"); // Overweight
            } else if (BMI >= 30) {
                System.out.println("4"); // Obesity
            }
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Number of test cases: 
2
Enter M (kgs) and H (mts) for test case 1: 
60 2
Enter M (kgs) and H (mts) for test case 2: 
75 1
1
4
Example 2:

Number of test cases: 
1
Enter M (kgs) and H (mts) for test case 1: 
70 1.8
2
```
---
## 📚 Lessons Learned
Learned to compute BMI using mathematical formulas.
Practiced using conditional statements to classify numerical values into categories.
Enhanced skills in handling multiple test cases in one program.

---
## ⚡ Challenges
Ensuring accurate BMI calculation when working with floating-point numbers.
Handling edge cases, such as values of H = 0 (division by zero).

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
