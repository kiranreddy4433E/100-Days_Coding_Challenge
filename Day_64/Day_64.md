# Day 64 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 64** of my **100 Days of Code Challenge**! Today, I implemented a Java program to analyze binary strings and classify feedback as **Good** or **Bad**. The program checks if the string contains specific patterns (`010` or `101`) to determine the classification.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple test cases with binary string inputs.
  2. For each binary string, check if it contains the substring `010` or `101`.
  3. Output `"Good"` if the criteria are met, otherwise output `"Bad"`.
- Practiced substring operations and string analysis techniques.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** String Manipulation, Substrings, Loops

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - A binary string containing only `0` and `1`.
- **Output**:
  - Print `"Good"` if the string contains either substring `010` or `101`.
  - Print `"Bad"` otherwise.

---

### Input/Output Example:

#### Example 1:
**Input**:
Number of test cases: 2 Binary string as a feedback for testcase 1: 010101 Binary string as a feedback for testcase 2: 00000



**Output**:
Good Bad


#### Example 2:
**Input**:
Number of test cases: 3 Binary string as a feedback for testcase 1: 101 Binary string as a feedback for testcase 2: 010 Binary string as a feedback for testcase 3: 11111

makefile
Copy code

**Output**:
Good Good Bad

java
Copy code

---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day1_64 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Number of test cases (T): ");
        int T = input.nextInt();
        input.nextLine(); // Consume the leftover newline

        for (int i = 0; i < T; i++) {
            System.out.println("Binary string as feedback for testcase " + (i + 1) + ": ");
            String str = input.nextLine();

            boolean isGood = false;
            for (int j = 0; j < str.length() - 2; j++) {
                String sub = str.substring(j, j + 3);
                if (sub.equals("010") || sub.equals("101")) {
                    isGood = true;
                    break;
                }
            }

            if (isGood) {
                System.out.println("Good");
            } else {
                System.out.println("Bad");
            }
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Number of test cases: 
2
Binary string as feedback for testcase 1: 
010101
Binary string as feedback for testcase 2: 
00000
Good
Bad
Example 2:

Number of test cases: 
3
Binary string as feedback for testcase 1: 
101
Binary string as feedback for testcase 2: 
010
Binary string as feedback for testcase 3: 
11111
Good
Good
Bad
```
---
## 📚 Lessons Learned
Practiced working with substrings to extract and analyze parts of a string.
Improved logic-building skills for string pattern matching using substring.
Reinforced the use of nested loops and boolean flags for condition-based evaluations.

---
## ⚡ Challenges
Ensuring the correct substring length (3) to avoid StringIndexOutOfBoundsException.
Managing edge cases, such as very short binary strings ("0" or "1").

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
