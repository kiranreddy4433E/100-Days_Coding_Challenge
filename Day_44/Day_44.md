# Day 44 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 44** of my **100 Days of Code Challenge**! Today, I implemented a Java program to count the number of **even** and **odd** elements in an array. This exercise improved my understanding of array traversal and condition-based counting.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept an array of integers from the user.
  2. Count the number of even elements in the array.
  3. Count the number of odd elements in the array.
- Practiced conditional logic and array iteration.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Loops, Conditional Statements

## 📖 Problem Description
- The task is to:
  1. Input the size of an array and its elements.
  2. Count and display the number of even and odd elements in the array.

For example:
  - Input: `Array: [1, 2, 3, 4, 5]`
  - Output:
    ```
    Number of even numbers: 2
    Number of odd numbers: 3
    ```

---

### Input/Output Example:

- **Input**:
Enter the number of elements in the array: 5 Enter the elements: 1 2 3 4 5

markdown
Copy code
- **Output**:
Number of even numbers: 2 Number of odd numbers: 3

csharp
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_63 {

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

      System.out.println("Number of even numbers: " + evenCount);
      System.out.println("Number of odd numbers: " + oddCount);

      input.close();
  }
}
🖥️ Program Output
Example 1:

Enter the number of elements in the array: 5
Enter the array elements:
1 2 3 4 5
Number of even numbers: 2
Number of odd numbers: 3
Example 2:

Enter the number of elements in the array: 4
Enter the array elements:
2 4 6 8
Number of even numbers: 4
Number of odd numbers: 0
```
---
### 📚 Lessons Learned
Learned how to count specific types of elements in an array using loops.
Practiced implementing conditional checks for even and odd numbers.

---
### ⚡ Challenges
Ensuring that edge cases such as empty arrays or arrays with all even/odd numbers are handled correctly.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
