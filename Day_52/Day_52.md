# Day 52 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 52** of my **100 Days of Code Challenge**! Today, I implemented a Java program to **reverse an integer array**. This task helped me practice array traversal and understand reversing techniques.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept an integer array as input from the user.
  2. Reverse the array elements.
  3. Display the reversed array.
- Practiced array manipulation and iteration.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Loops, Reversal Logic

## 📖 Problem Description
- The task is to:
  1. Input the size of an integer array and its elements.
  2. Reverse the array such that the last element becomes the first, the second-last becomes the second, and so on.
  3. Display the reversed array.

For example:
  - Input: `Array: [1, 2, 3, 4, 5]`
  - Output:
    ```
    Reversed array: [5, 4, 3, 2, 1]
    ```

---

### Input/Output Example:

- **Input**:
Size of the array: 5 Enter the elements: 1 2 3 4 5

markdown
Copy code
- **Output**:
Reversed array: 5 4 3 2 1

java
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;
import java.util.Arrays;

public class pro_72 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Size of the array: ");
      int num = input.nextInt();

      int[] array = new int[num];

      System.out.println("Enter the array elements: ");
      for (int i = 0; i < num; i++) {
          array[i] = input.nextInt();
      }

      // Display the reversed array
      System.out.println("Reversed array: ");
      for (int i = array.length - 1; i >= 0; i--) {
          System.out.println(array[i]);
      }

      input.close();
  }
}
🖥️ Program Output
Example 1:

Size of the array: 
5
Enter the array elements: 
1 2 3 4 5
Reversed array: 
5
4
3
2
1
Example 2:

Size of the array: 
4
Enter the array elements: 
10 20 30 40
Reversed array: 
40
30
20
10
```
---
## 📚 Lessons Learned
Practiced iterating through an array in reverse order.
Learned how to manipulate array indices for reversal.

---
## ⚡ Challenges
Ensuring the program handles edge cases such as empty arrays or arrays with a single element.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
