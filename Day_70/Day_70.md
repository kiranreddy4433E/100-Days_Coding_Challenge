# Day 70 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 70** of my **100 Days of Code Challenge**! Today, I implemented a program to rotate an array by one position in a clockwise direction. This problem emphasizes array manipulation and loop-based shifting techniques.

## ✅ What I did today
- Implemented a Java program to:
  1. Accept an array as input.
  2. Rotate the array elements one position to the right (clockwise).
  3. Output the rotated array.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Loop Manipulation, Array Shifting

## 📖 Problem Description
- **Input**:
  - `T`: Number of elements in the array.
  - An array of size `T` with integer elements.
- **Output**:
  - Rotated array after one clockwise shift.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter a T number of test cases: 5 1 2 3 4 5



**Output**:
5 1 2 3 4


#### Example 2:
**Input**:
Enter a T number of test cases: 3 10 20 30


**Output**:
30 10 20


---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_70 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Enter a T number of test cases: ");
        int T = input.nextInt(); // Number of elements in the array

        // Initialize the array
        int[] array = new int[T];
        System.out.println("Enter the elements of the array: ");
        for (int i = 0; i < T; i++) {
            array[i] = input.nextInt();
        }

        // Rotate the array by one position (clockwise)
        int last = array[array.length - 1]; // Store the last element
        for (int j = array.length - 1; j > 0; j--) {
            array[j] = array[j - 1]; // Shift elements to the right
        }
        array[0] = last; // Place the last element at the start

        // Output the rotated array
        System.out.println("Rotated Array: ");
        for (int i = 0; i < T; i++) {
            System.out.print(array[i] + " ");
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Enter a T number of test cases: 
5
1 2 3 4 5
Rotated Array: 
5 1 2 3 4
Example 2:

Enter a T number of test cases: 
3
10 20 30
Rotated Array: 
30 10 20
```
---
## 📚 Lessons Learned
Practiced array manipulation by shifting elements.
Reinforced loop-based operations for solving array rotation problems.
Gained a better understanding of handling edge cases like small arrays or arrays with duplicate values.

---
## ⚡ Challenges
Handling edge cases where the array has only one element (rotation is trivial).
Ensuring all elements are correctly shifted in the correct order.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn:[Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
