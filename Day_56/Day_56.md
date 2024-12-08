# Day 56 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 56** of my **100 Days of Code Challenge**! Today, I implemented a Java program to determine whether the elements of an array can be made equal by repeatedly dividing them by **2** and/or **3**. This problem allowed me to practice number manipulation and array traversal.

## ✅ What I did today
- Wrote a Java program to:
  1. Input an array of integers.
  2. Reduce each element by dividing it by **2** and/or **3** until it can no longer be divided.
  3. Check if all elements can be made equal after this reduction.
- Practiced array manipulation and logical comparison.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Loops, Number Manipulation

## 📖 Problem Description
- The task is to:
  1. Input the size and elements of an integer array.
  2. Divide each element repeatedly by **2** and/or **3** until it can no longer be divided.
  3. Check if all elements become the same after this operation.
  4. Output whether it's possible to make all elements equal.

For example:
  - Input:
    ```
    Array: [50, 25, 75]
    ```
  - Output:
    ```
    No, it's not possible to make all elements equal.
    ```

  - Input:
    ```
    Array: [8, 16, 4]
    ```
  - Output:
    ```
    Yes, it's possible to make all elements equal.
    ```

---

### Input/Output Example:

- **Input**:
Size of the array: 3 Enter the elements of the array: 8 16 4

markdown
Copy code
- **Output**:
Yes, it's possible to make all elements equal.

markdown
Copy code

- **Input**:
Size of the array: 3 Enter the elements of the array: 50 25 75

markdown
Copy code
- **Output**:
No, it's not possible to make all elements equal.


---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_56 {
  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      // Input the size of the array
      System.out.println("Size of the array: ");
      int num = input.nextInt();
      int[] array = new int[num];

      // Input the array elements
      System.out.println("Enter the elements of the array:");
      for (int i = 0; i < num; i++) {
          array[i] = input.nextInt();
      }

      // Step 1: Reduce each element by dividing by 2 and/or 3
      for (int i = 0; i < num; i++) {
          while (array[i] % 2 == 0) {
              array[i] /= 2;
          }
          while (array[i] % 3 == 0) {
              array[i] /= 3;
          }
      }

      // Step 2: Check if all elements are equal
      boolean isEqual = true;
      for (int i = 1; i < num; i++) {
          if (array[i] != array[0]) {
              isEqual = false;
              break;
          }
      }

      // Output the result
      if (isEqual) {
          System.out.println("Yes, it's possible to make all elements equal.");
      } else {
          System.out.println("No, it's not possible to make all elements equal.");
      }

      // Close the Scanner
      input.close();
  }
}
🖥️ Program Output
Example 1: Possible to Make Equal

Size of the array: 
3
Enter the elements of the array: 
8 16 4
Yes, it's possible to make all elements equal.
Example 2: Not Possible to Make Equal

Size of the array: 
3
Enter the elements of the array: 
50 25 75
No, it's not possible to make all elements equal.
```
---
###  📚 Lessons Learned
Practiced reducing numbers using divisors 2 and 3.
Learned how to check equality across all elements of an array.

---
### ⚡ Challenges
Ensuring the logic handles arrays with a mix of large and small numbers effectively.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
