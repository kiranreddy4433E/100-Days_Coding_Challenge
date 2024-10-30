# Day 19 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 19** of my **100 Days of Code Challenge**! Today, I wrote a Java program to determine if a given number is an **Armstrong number**. This exercise helped me improve my understanding of number manipulation, power calculations, and conditional logic.

## ✅ What I did today
- Implemented a Java program to check if a number is an **Armstrong number**.
- Practiced extracting and manipulating digits, and calculating powers.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Armstrong Number, Power Calculations

## 📖 Problem Description
- An **Armstrong number** (or **narcissistic number**) for a given number of digits is a number that is equal to the sum of its digits each raised to the power of the number of digits. For example:
  - \(153\) is an Armstrong number because \(1^3 + 5^3 + 3^3 = 153\).
  - \(9474\) is an Armstrong number because \(9^4 + 4^4 + 7^4 + 4^4 = 9474\).

### Input/Output Example:
  - **Input**: `153`
    - **Output**: `153 is an Armstrong number.`
  
  - **Input**: `123`
    - **Output**: `123 is not an Armstrong number.`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_31 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        // Input a number to check if it's an Armstrong number
        System.out.println("Enter a number");
        int num = input.nextInt();
        
        int sum = 0;
        int digits = String.valueOf(num).length(); // Get the number of digits
        int temp = num;
        
        // Calculate the sum of each digit raised to the power of the number of digits
        while(temp > 0) {
            int digit = temp % 10;
            sum += Math.pow(digit, digits);
            temp /= 10;
        }
        
        // Check if the sum equals the original number
        if (num == sum) {
            System.out.println(num + " is an Armstrong number.");
        } else {
            System.out.println(num + " is not an Armstrong number.");
        }
        
        input.close();
    }
}
```
---

### 🖥️ Program Output

Enter a number
153
153 is an Armstrong number.

Enter a number
123
123 is not an Armstrong number.

---
### 📚 Lessons Learned
Practiced using Math.pow() to raise each digit to the correct power.
Gained familiarity with extracting individual digits and working with powers in Java.
Reinforced the logic for checking special properties of numbers, like Armstrong numbers.

---
### ⚡ Challenges
Calculating powers for each digit accurately was crucial for identifying Armstrong numbers correctly.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
