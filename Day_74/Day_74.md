# Day 74 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 74** of my **100 Days of Code Challenge**! Today, I worked on solving a grid-tiling problem where the objective is to minimize the number of **1x1 tiles** used to cover a grid while maximizing the use of **2x2 tiles**.

## ✅ What I did today
- Designed a Java program to:
  1. Calculate the total number of cells in a grid of dimensions `N x M`.
  2. Determine the maximum number of **2x2 tiles** that can fit in the grid.
  3. Calculate the remaining uncovered cells, which require **1x1 tiles**.
- Practiced efficient arithmetic operations and logic for tiling problems.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Grid Tiling, Integer Arithmetic, Looping Structures

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `N`: Number of rows in the grid.
    - `M`: Number of columns in the grid.
- **Output**:
  - For each test case, print the minimum number of **1x1 tiles** required to completely fill the grid.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter T (number of test cases): 2 Enter test case 1 (N M): 4 5 Enter test case 2 (N M): 6 6


**Output**:
5 0


#### Explanation:
- **Test Case 1**: A 4x5 grid has 20 cells. Using four **2x2 tiles**, we can cover 16 cells, leaving 4 cells uncovered, which require 1x1 tiles.
- **Test Case 2**: A 6x6 grid has 36 cells. Using nine **2x2 tiles**, we can cover all 36 cells, so no 1x1 tiles are required.

---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_74 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter T (number of test cases): ");
        int T = input.nextInt(); // Number of test cases
        
        for (int i = 0; i < T; i++) {
            System.out.println("Enter test case " + (i + 1) + " (N M): ");
            int N = input.nextInt(); // Rows of the grid
            int M = input.nextInt(); // Columns of the grid
            
            // Total cells in the grid
            int totalCells = N * M;
            // Maximum 2x2 tiles that can fit
            int max2x2Tiles = (N / 2) * (M / 2);
            // Cells covered by 2x2 tiles
            int coveredCells = max2x2Tiles * 4;
            // Remaining cells (1x1 tiles required)
            int remainingCells = totalCells - coveredCells;
            // Output the result
            System.out.println(remainingCells);
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Enter T (number of test cases): 
2
Enter test case 1 (N M): 
4 5
5
Enter test case 2 (N M): 
6 6
0
```
---
## 📚 Lessons Learned
Practiced logical reasoning and integer arithmetic for grid-based problems.
Understood how to optimize tiling to minimize the use of smaller tiles.
Reinforced the importance of calculating areas and remainder cells for efficient solutions.

---
## ⚡ Challenges
Ensuring that the solution works efficiently for edge cases like small grids (1x1, 2x2, etc.) and non-square grids.
Accounting for grids where no 2x2 tiles fit, which require all 1x1 tiles.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

--- 
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
