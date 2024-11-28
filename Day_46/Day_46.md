# Day 46 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 46** of my **100 Days of Code Challenge**! Today, I implemented a Java program to calculate the **sum of all elements in an array**. This task helped me practice iterating through arrays and performing cumulative calculations.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept an array of integers from the user.
  2. Calculate and display the sum of all elements in the array.
- Practiced array traversal and cumulative addition.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Loops, Arithmetic Operations

## 📖 Problem Description
- The task is to:
  1. Input the size of an array and its elements.
  2. Calculate the sum of all elements in the array.
  3. Display the total sum.

For example:
  - Input: `Array: [1, 2, 3, 4, 5]`
  - Output:
    ```
    Sum of array elements: 15
    ```

---

### Input/Output Example:

- **Input**:
Enter the size of the array: 5 Enter the elements: 1 2 3 4 5

markdown
Copy code
- **Output**:
Sum of array elements: 15

csharp
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_65 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Enter the size of the array: ");
      int num = input.nextInt();

      int sum = 0;
      int[] arrays = new int[num];

      System.out.println("Enter the array elements: ");
      for (int i = 0; i < num; i++) {
          arrays[i] = input.nextInt();
          sum += arrays[i];
      }

      System.out.println("Sum of array elements = " + sum);

      input.close();
  }
}
🖥️ Program Output
Example 1:

Enter the size of the array: 
5
Enter the array elements: 
1 2 3 4 5
Sum of array elements = 15
Example 2:

Enter the size of the array: 
4
Enter the array elements: 
10 20 30 40
Sum of array elements = 100
```
---
### 📚 Lessons Learned
Practiced iterating through an array using loops.
Learned how to calculate cumulative values using a running sum.

---
### ⚡ Challenges
Ensuring the program handles edge cases such as an empty array or negative numbers.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
