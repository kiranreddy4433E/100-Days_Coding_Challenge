
# Day 65 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 65** of my **100 Days of Code Challenge**! Today, I implemented a Java program to help Ajinkya choose the best tablet he can buy within his budget. The tablet is selected based on the largest screen area that fits within the budget.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple test cases.
  2. For each test case:
     - Input the number of available tablets (`N`) and Ajinkya's budget (`B`).
     - For each tablet, input its width (`Wi`), height (`Hi`), and price (`Pi`).
  3. Determine the tablet with the largest screen area (`Wi * Hi`) that fits within the budget (`Pi ≤ B`).
  4. Print the maximum screen area, or output `"No Tablet"` if no suitable tablet is found.
- Practiced nested loops and conditional logic to filter and compare options.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Nested Loops, Conditional Statements, Arithmetic Operations

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `N`: Number of available tablets.
    - `B`: Budget in rupees.
    - For each tablet:
      - `Wi`: Width of the tablet.
      - `Hi`: Height of the tablet.
      - `Pi`: Price of the tablet.
- **Output**:
  - Print the largest screen area for a tablet within the budget.
  - Print `"No Tablet"` if no tablet fits within the budget.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter a T number of test cases: 1 3 6 3 4 4 5 5 7 5 2 5



**Output**:
12



#### Example 2:
**Input**:
Enter a T number of test cases: 1 2 3 3 3 4 2 2 3



**Output**:
No Tablet

---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_65 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Enter a T number of test cases: ");
        int T = input.nextInt(); 

        for (int i = 0; i < T; i++) {
            int maxArea = 0;

            System.out.println("Enter N (number of tablets) and B (budget) for test case " + (i + 1) + ":");
            int N = input.nextInt(); // Number of tablets
            int B = input.nextInt(); // Budget of the tablet

            for (int n = 0; n < N; n++) {
                System.out.println("Enter Wi (width), Hi (height), and Pi (price) for tablet " + (n + 1) + ":");
                int Wi = input.nextInt(); // Width of the tablet
                int Hi = input.nextInt(); // Height of the tablet
                int Pi = input.nextInt(); // Price of the tablet

                if (Pi <= B) {
                    int area = Wi * Hi;
                    if (area > maxArea) {
                        maxArea = area;
                    }
                }
            }

            if (maxArea > 0) {
                System.out.println("Maximum screen area: " + maxArea);
            } else {
                System.out.println("No Tablet");
            }
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Enter a T number of test cases: 
1
Enter N (number of tablets) and B (budget) for test case 1:
3 6
Enter Wi (width), Hi (height), and Pi (price) for tablet 1:
3 4 4
Enter Wi (width), Hi (height), and Pi (price) for tablet 2:
5 5 7
Enter Wi (width), Hi (height), and Pi (price) for tablet 3:
5 2 5
Maximum screen area: 12
Example 2:

Enter a T number of test cases: 
1
Enter N (number of tablets) and B (budget) for test case 1:
2 3
Enter Wi (width), Hi (height), and Pi (price) for tablet 1:
3 3 4
Enter Wi (width), Hi (height), and Pi (price) for tablet 2:
2 2 3
No Tablet
```
---
## 📚 Lessons Learned
Practiced nested loops to evaluate multiple test cases and conditions.
Improved skills in filtering options based on multiple criteria (price and area).
Enhanced problem-solving abilities by simulating real-world decision-making processes.

---
## ⚡ Challenges
Ensuring accurate comparisons and updates for the maximum screen area.
Managing edge cases where no tablet fits the budget.

---
##  📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
