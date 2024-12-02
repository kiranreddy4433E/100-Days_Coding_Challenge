# Day 50 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 50** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate the **sum of the squares of positive elements** in an array. This task helped me practice array traversal and arithmetic operations.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept an integer array as input.
  2. Calculate the square of each element.
  3. Add up the squares of all elements to find the total sum.
- Practiced using loops and arithmetic operations on arrays.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Loops, Arithmetic Operations

## 📖 Problem Description
- The task is to:
  1. Input the size and elements of an array.
  2. Calculate the square of each positive element.
  3. Compute and display the sum of the squared elements.

For example:
  - Input: `Array: [1, -2, 3, 4]`
  - Output:
    ```
    Squares of elements: [1, 4, 9, 16]
    Sum of positive squares: 30
    ```

---

### Input/Output Example:

- **Input**:
Size of the array: 4 Enter the elements: 1 -2 3 4

markdown
Copy code
- **Output**:
Squares of elements: 1 4 9 16 Sum of positive squares: 30

csharp
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_70 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Size of the array: ");
      int num = input.nextInt();

      int sum = 0;
      int[] array = new int[num];

      System.out.println("Enter the array elements: ");
      for (int i = 0; i < num; i++) {
          array[i] = input.nextInt();
          int multiply = array[i] * array[i];
          sum += multiply;
      }

      System.out.println("Squares of elements: ");
      for (int i = 0; i < num; i++) {
          System.out.println(array[i] * array[i]);
      }

      System.out.println("Sum of the squares of positive numbers: " + sum);
      input.close();
  }
}
🖥️ Program Output
Example 1:

Size of the array: 
4
Enter the array elements: 
1 -2 3 4
Squares of elements: 
1
4
9
16
Sum of the squares of positive numbers: 30
Example 2:

Size of the array: 
3
Enter the array elements: 
0 2 -5
Squares of elements: 
0
4
25
Sum of the squares of positive numbers: 29
```
---
## 📚 Lessons Learned
Practiced calculating the square of each array element.
Improved understanding of summing computed values in an array.

---
## ⚡ Challenges
Ensuring accurate results for mixed arrays containing positive, negative, and zero values.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
