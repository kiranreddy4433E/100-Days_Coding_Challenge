# Day 22 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 22** of my **100 Days of Code Challenge**! Today, I implemented a Java program that checks if a given number can be expressed as the **sum of two prime numbers**. This exercise helped me practice identifying prime numbers and using logic to verify the sum of two primes.

## ✅ What I did today
- Wrote a Java program to determine if a number can be expressed as the **sum of two prime numbers**.
- Practiced prime number detection and sum verification.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Prime Numbers, Loops, Conditional Statements

## 📖 Problem Description
- A number can sometimes be expressed as the sum of two prime numbers. For example:
  - \(10\) can be expressed as \(3 + 7\) or \(5 + 5\), both of which are sums of prime numbers.
  - \(15\) can be expressed as \(7 + 2\) and \(11 + 2\).

### Input/Output Example:
  - **Input**: `10`
    - **Output**: `10 can be expressed as 3 + 7 and 5 + 5.`
  
  - **Input**: `11`
    - **Output**: `11 cannot be expressed as the sum of two primes.`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_34 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter a number: ");
        int num = input.nextInt();
        
        boolean found = false;

        // Check if the number can be expressed as the sum of two primes
        for (int i = 2; i <= num / 2; i++) {
            if (isPrime(i) && isPrime(num - i)) {
                System.out.println(num + " can be expressed as " + i + " + " + (num - i));
                found = true;
            }
        }

        if (!found) {
            System.out.println(num + " cannot be expressed as the sum of two prime numbers.");
        }

        input.close();
    }

    // Helper method to check if a number is prime
    public static boolean isPrime(int n) {
        if (n <= 1) return false;
        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0) {
                return false;
            }
        }
        return true;
    }
}
```
---

### 🖥️ Program Output

- Enter a number: 
- 10
- 10 can be expressed as 3 + 7
- 10 can be expressed as 5 + 5

- Enter a number: 
- 11
- 11 cannot be expressed as the sum of two prime numbers.

--- 
### 📚 Lessons Learned
Practiced identifying prime numbers and checking possible prime pairs.
Reinforced using helper functions to isolate the prime-checking logic.

---
### ⚡ Challenges
Ensuring efficiency in checking both primes within each loop iteration was important for larger numbers.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746
---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
