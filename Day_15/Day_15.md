# Day 15 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 15** of my **100 Days of Code Challenge**! Today, I implemented a Java program that checks whether a given number is a **strong number** and also identifies all strong numbers within a specified range. This problem helped me understand **factorial calculations** and practice working with **loops** and **conditional statements**.

## ✅ What I did today
- Implemented a Java program to check if a number is a **strong number**.
- Extended the program to find all strong numbers within a given range.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Factorial Calculation, Strong Number, Conditional Statements

## 📖 Problem Description
- A **strong number** is a number in which the sum of the factorials of each digit equals the number itself. For example, `145` is a strong number because:
  \[
  1! + 4! + 5! = 1 + 24 + 120 = 145
  \]
- The task is to:
  - Check if a given number is a strong number.
  - Find all strong numbers within a specified range.

### Input/Output Example:
1. **Single Number Check**:
   - Input: `145`
   - Output: `145 is a strong number.`
2. **Range Check**:
   - Input: `1 to 200`
   - Output: `Strong numbers between 1 and 200: 1 2 145`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_26 {
    
    // Method to calculate the factorial of a digit
    public static int factorial(int n) {
        int fact = 1;
        for (int i = 1; i <= n; i++) {
            fact *= i;
        }
        return fact;
    }

    // Method to check if a number is a strong number
    public static boolean isStrongNumber(int number) {
        int sum = 0, temp = number;
        
        while (temp > 0) {
            int digit = temp % 10;
            sum += factorial(digit);
            temp /= 10;
        }
        
        return sum == number;
    }

    // Method to find and print all strong numbers in a given range
    public static void findStrongNumbersInRange(int start, int end) {
        System.out.println("Strong numbers between " + start + " and " + end + ":");
        for (int i = start; i <= end; i++) {
            if (isStrongNumber(i)) {
                System.out.print(i + " ");
            }
        }
        System.out.println();
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Taking user input for a single number check
        System.out.print("Enter a number to check if it's a strong number: ");
        int number = scanner.nextInt();
        
        if (isStrongNumber(number)) {
            System.out.println(number + " is a strong number.");
        } else {
            System.out.println(number + " is not a strong number.");
        }
        
        // Taking user input for range to find all strong numbers within it
        System.out.print("Enter the start of the range: ");
        int start = scanner.nextInt();
        
        System.out.print("Enter the end of the range: ");
        int end = scanner.nextInt();
        
        findStrongNumbersInRange(start, end);

        scanner.close();
    }
}
```
---

### 🖥️ Program Output

Enter a number to check if it's a strong number: 
145
145 is a strong number.

Enter the start of the range: 
1
Enter the end of the range: 
200
Strong numbers between 1 and 200:
1 2 145

---

### 📚 Lessons Learned
Learned to calculate factorials of digits and sum them to check for strong numbers.
Practiced writing modular methods to separate concerns (checking single numbers and finding numbers in a range).
Gained further experience with loops and conditional checks in Java.

---

### ⚡ Challenges
Calculating the factorial of each digit repeatedly required careful handling to ensure performance efficiency.

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/feed/update/urn:li:activity:7255627278414426113/)
- Twitter: @kiran4746

---

100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
