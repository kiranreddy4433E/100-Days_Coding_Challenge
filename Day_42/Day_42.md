# Day 42 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 42** of my **100 Days of Code Challenge**! Today, I implemented a Java program to compare two arrays and determine if they are the same. This task helped me understand how to iterate through arrays and compare their elements efficiently.

## ✅ What I did today
- Wrote a Java program to check if two arrays have the same elements in the same order.
- Practiced iterating through arrays and comparing their elements.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Loops, Conditional Statements

## 📖 Problem Description
- The task is to:
  1. Take two arrays as input from the user.
  2. Compare their elements to determine if they are identical in length and content.
  3. Print whether the arrays are the same or not.
  
For example:
  - Input: 
    ```
    Array 1: [1, 2, 3, 4]
    Array 2: [1, 2, 3, 4]
    ```
  - Output: `"The arrays are matching."`

### Input/Output Example:
  - **Input**:
    ```
    Enter the number of elements in the arrays: 4
    Enter elements of Array 1: 1 2 3 4
    Enter elements of Array 2: 1 2 3 4
    ```
  - **Output**:
    ```
    The arrays are matching.
    Matching array is: [1, 2, 3, 4]
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;
import java.util.Arrays;

public class pro_61 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Enter the number of elements in the arrays:");
        int num = input.nextInt();

        int[] array = new int[num];
        int[] array1 = new int[num];

        System.out.println("Enter elements of Array 1:");
        for (int i = 0; i < num; i++) {
            array[i] = input.nextInt();
        }

        System.out.println("Enter elements of Array 2:");
        for (int i = 0; i < num; i++) {
            array1[i] = input.nextInt();
        }

        boolean isMatching = true;
        for (int i = 0; i < num; i++) {
            if (array[i] != array1[i]) {
                isMatching = false;
                break;
            }
        }

        if (isMatching) {
            System.out.println("The arrays are matching.");
            System.out.println("Matching array is: " + Arrays.toString(array));
        } else {
            System.out.println("The arrays are not matching.");
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Enter the number of elements in the arrays: 
4
Enter elements of Array 1: 
1 2 3 4
Enter elements of Array 2: 
1 2 3 4
The arrays are matching.
Matching array is: [1, 2, 3, 4]
Example 2:

Enter the number of elements in the arrays: 
4
Enter elements of Array 1: 
1 2 3 4
Enter elements of Array 2: 
1 2 5 6
The arrays are not matching.
```
---
### 📚 Lessons Learned
Practiced comparing arrays element-by-element using loops.
Learned how to handle user input for arrays and print formatted output.

---
### ⚡ Challenges
Ensuring the program handled arrays of different sizes gracefully (though size input is restricted in this implementation).

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
