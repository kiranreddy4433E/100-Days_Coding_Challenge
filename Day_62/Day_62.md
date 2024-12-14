# Day 62 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 62** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate whether Anusree and his friends can collectively carry all the gold from a mine in a single trip based on their individual carrying capacity.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple test cases.
  2. For each test case:
     - Input the number of friends (`N`), total gold required (`X`), and the carrying capacity per person (`Y`).
  3. Determine if the total gold can be carried in one trip by Anusree and his friends together.
- Practiced arithmetic operations and conditional logic for decision-making.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arithmetic Operations, Loops, Conditional Statements

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - `N`: Number of Anusree's friends.
    - `X`: Total gold in kilograms that needs to be carried.
    - `Y`: Carrying capacity of each person in kilograms.
- **Output**:
  - Print `"Yes"` if Anusree and his friends can carry all the gold in one trip.
  - Print `"No"` otherwise.

---

### Input/Output Example:

#### Example 1:
**Input**:
Number of test cases: 2 Enter N, X, and Y for test case 1: 3 10 3 Enter N, X, and Y for test case 2: 4 50 10



**Output**:
Yes No



#### Example 2:
**Input**:
Number of test cases: 1 Enter N, X, and Y for test case 1: 5 30 6



**Output**:
Yes



---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_62 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Number of test cases (T): ");
        int T = input.nextInt();

        for (int i = 0; i < T; i++) {
            System.out.println("Enter N (members), X (required gold), and Y (gold per member) for test case " + (i + 1) + ":");
            int N = input.nextInt(); // Number of Anusree's friends
            int X = input.nextInt(); // Total gold required
            int Y = input.nextInt(); // Gold each person can carry

            int totalGold = Y * (N + 1); // Total gold they can carry
            if (totalGold >= X) {
                System.out.println("Yes");
            } else {
                System.out.println("No");
            }
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Number of test cases: 
2
Enter N, X, and Y for test case 1: 
3 10 3
Enter N, X, and Y for test case 2: 
4 50 10
Yes
No
Example 2:

Number of test cases: 
1
Enter N, X, and Y for test case 1: 
5 30 6
Yes
```
---
## 📚 Lessons Learned
Practiced calculating the total carrying capacity based on individual limits and the number of participants.
Improved my skills in handling multiple test cases and logical comparisons.
Reinforced the use of loops and arithmetic operations for problem-solving.

---
## ⚡ Challenges
Ensuring accurate calculations when X (required gold) is close to or exceeds the maximum carrying capacity.
Handling edge cases such as N = 0 (only Anusree carries the gold).

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
