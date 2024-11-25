# Day 43 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 43** of my **100 Days of Code Challenge**! Today, I wrote a Java program to determine whether an array is composed entirely of even numbers, odd numbers, or a mix of both. This exercise enhanced my understanding of arrays and conditional checks.

## ✅ What I did today
- Wrote a Java program to classify an array as:
  - **Even** (all elements are even numbers).
  - **Odd** (all elements are odd numbers).
  - **Mixed** (a combination of even and odd numbers).
- Practiced iterating through arrays and using conditional logic for classification.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Loops, Conditional Statements

## 📖 Problem Description
- The task is to:
  1. Accept an array of integers as input from the user.
  2. Determine if the array is:
     - **Even**: All elements are even.
     - **Odd**: All elements are odd.
     - **Mixed**: Contains both even and odd numbers.
  3. Display the array and its classification.

### Input/Output Example:
  - **Input**:
    ```
    Enter the number of elements: 5
    Enter the elements: 2 4 6 8 10
    ```
  - **Output**:
    ```
    Array elements: 2, 4, 6, 8, 10
    This is an Even array.
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_62 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.print("Enter the number of elements in the array: ");
        int num = input.nextInt();
        int[] arrays = new int[num];
        int evenCount = 0;
        int oddCount = 0;

        System.out.println("Enter the array elements:");
        for (int i = 0; i < num; i++) {
            arrays[i] = input.nextInt();
        }

        // Count even and odd numbers
        for (int i = 0; i < num; i++) {
            if (arrays[i] % 2 == 0) {
                evenCount++;
            } else {
                oddCount++;
            }
        }

        // Print the array
        System.out.print("Array elements: ");
        for (int i = 0; i < num; i++) {
            System.out.print(arrays[i] + (i < num - 1 ? ", " : ""));
        }
        System.out.println();

        // Classify the array
        if (evenCount == num) {
            System.out.println("This is an Even array.");
        } else if (oddCount == num) {
            System.out.println("This is an Odd array.");
        } else {
            System.out.println("This is a Mixed array.");
        }

        input.close();
    }
}
🖥️ Program Output
Example 1: Even Array

Enter the number of elements in the array: 5
Enter the array elements: 
2 4 6 8 10
Array elements: 2, 4, 6, 8, 10
This is an Even array.

Example 2: Odd Array

Enter the number of elements in the array: 5
Enter the array elements: 
1 3 5 7 9
Array elements: 1, 3, 5, 7, 9
This is an Odd array.

Example 3: Mixed Array

Enter the number of elements in the array: 5
Enter the array elements: 
1 2 3 4 5
Array elements: 1, 2, 3, 4, 5
This is a Mixed array.
```
---
### 📚 Lessons Learned
Practiced classifying arrays based on their elements.
Gained experience in counting and conditionally evaluating array elements.

---
### ⚡ Challenges
Handling edge cases such as an empty array or invalid input values.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

--- 
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
