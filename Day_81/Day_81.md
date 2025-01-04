# Day 81 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 81** of my **100 Days of Code Challenge**! Today, I solved a problem involving sorting a binary string using a specific operation. The goal was to determine the **minimum number of operations** required to sort the binary string, where an operation consists of selecting a substring and reversing it.

---

## ✅ Problem Description
You are given a binary string \( S \) of length \( N \). In one operation, you can select any substring of \( S \) and reverse it. 

The task is to find the **minimum number of operations** required to sort the binary string in non-decreasing order (all `0`s followed by all `1`s).

### Example
#### Input:
Enter a T test cases: 2 Enter a test case: 1 6 Enter a binary string: 110100 Enter a test case: 2 5 Enter a binary string: 01101


#### Output:
Minimum string: 1 Minimum string: 1


---

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** String Manipulation, Substring Operations, Blocks Counting

---

## 📖 Code Example

```java
package coading_Challange;

import java.util.*;

public class Day_81 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter a T test cases:- ");
        int num = input.nextInt();
        input.nextLine();
        for (int i = 0; i < num; i++) {
            System.out.println("Enter a test case:- " + (i + 1));
            int N = input.nextInt();
            input.nextLine();
            System.out.println("Enter a binary string:- ");
            String binary = input.nextLine();
            System.out.println("Minimum string:- " + MinimumString(binary));
        }
        input.close();
    }

    private static int MinimumString(String binary) {
        int onesBlock = 0;
        int zeroBlock = 0;
        char prev = ' ';
        for (int i = 0; i < binary.length(); i++) {
            char current = binary.charAt(i);
            if (current != prev) {
                if (current == '1') {
                    onesBlock++;
                } else {
                    zeroBlock++;
                }
            }
            prev = current;
        }
        return Math.min(onesBlock, zeroBlock);
    }
}
🖥️ Program Output
Input:

Enter a T test cases: 
1
Enter a test case: 1
6
Enter a binary string: 
110100
Output:

Minimum string: 1
```
---
## 📚 Lessons Learned
Learned how to analyze binary strings to identify blocks of consecutive 1s and 0s.
Improved efficiency by using a single traversal to count distinct blocks in the string.
Enhanced my problem-solving skills for working with minimal operation problems.

---
## ⚡ Challenges
Handling edge cases, such as strings that are already sorted or have no alternating blocks.
Ensuring the program handles varying string lengths efficiently without time or memory overhead.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
