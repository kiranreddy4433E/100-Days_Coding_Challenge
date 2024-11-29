# Day 47 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 47** of my **100 Days of Code Challenge**! Today, I implemented a Java program to identify the **longest palindrome** in an array of integers. This task enhanced my understanding of palindrome logic and array traversal.

## ✅ What I did today
- Wrote a Java program to:
  1. Check each number in an array to determine if it is a palindrome.
  2. Find the palindrome with the maximum length in the array.
  3. Display the longest palindrome or indicate if none exist.
- Practiced reversing numbers and comparing them for palindromic properties.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Palindrome Logic, Loops

## 📖 Problem Description
- The task is to:
  1. Input an array of integers.
  2. Identify which numbers in the array are palindromes.
  3. Find the longest palindrome among them (based on the number of digits).

For example:
  - Input: `Array: [121, 131, 12321, 456, 22]`
  - Output:
    ```
    The longest palindrome in the array is: 12321
    ```

---

### Input/Output Example:

- **Input**:
Enter the number of elements in the array: 5 Enter the elements: 121 131 12321 456 22

markdown
Copy code
- **Output**:
The longest palindrome in the array is: 12321

java
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_66 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Enter the number of elements in the array: ");
      int num = input.nextInt();

      int[] arrays = new int[num];

      System.out.println("Enter the array elements: ");
      for (int i = 0; i < num; i++) {
          arrays[i] = input.nextInt();
      }

      int longestPalindrome = -1;
      int maxLength = 0;

      for (int i = 0; i < num; i++) {
          int originalNum = arrays[i];
          int reversedNum = 0;
          int temp = originalNum;

          // Reverse the number
          while (temp != 0) {
              int digit = temp % 10;
              reversedNum = reversedNum * 10 + digit;
              temp /= 10;
          }

          // Check if the number is a palindrome
          if (originalNum == reversedNum) {
              int length = String.valueOf(originalNum).length();
              if (length > maxLength) {
                  maxLength = length;
                  longestPalindrome = originalNum;
              }
          }
      }

      // Output the result
      if (longestPalindrome != -1) {
          System.out.println("The longest palindrome in the array is: " + longestPalindrome);
      } else {
          System.out.println("There is no palindrome found in the array.");
      }

      input.close();
  }
}
🖥️ Program Output
Example 1: Palindrome Found

Enter the number of elements in the array: 5
Enter the elements: 
121 131 12321 456 22
The longest palindrome in the array is: 12321
Example 2: No Palindrome Found

Enter the number of elements in the array: 3
Enter the elements: 
123 456 789
There is no palindrome found in the array.
```
---
## 📚 Lessons Learned
Practiced reversing numbers to check for palindromic properties.
Gained experience in identifying specific patterns (palindromes) in arrays.

---
## ⚡ Challenges
Handling edge cases, such as arrays with no palindromes or single-digit numbers.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
