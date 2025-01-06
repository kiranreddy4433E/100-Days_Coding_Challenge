# Day 82 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 82** of my **100 Days of Code Challenge**! Today, I solved a problem where the goal was to generate a **unique binary string** that differs from all given binary strings of the same length \( N \).

---

## ✅ Problem Description
You are given \( N \) binary strings of length \( N \). You need to find a binary string of length \( N \) that is **different** from all the given strings. 

### Notes:
- A **binary string** consists only of '0's and '1's.
- A string is considered different if:
  - It has a different length, or
  - It differs in at least one position.

### Example
#### Input:
Enter T test cases: 1 4 0101 1010 1111 0000


#### Output:
1100


---

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Binary Strings, String Manipulation, Diagonal Selection

---

## 📖 Code Example

```java
package practiceProb;

import java.util.*;

public class practice {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter T test cases: ");
        int num = input.nextInt();
        input.nextLine();
        for (int i = 0; i < num; i++) {
            int N = input.nextInt();
            input.nextLine();
            String[] str = new String[N];
            for (int j = 0; j < N; j++) {
                str[j] = input.nextLine().replace(" ", "");
            }
            String ans = unique(str, N);
            System.out.println(ans);
        }
        input.close();
    }

    private static String unique(String[] str, int N) {
        StringBuilder ans = new StringBuilder();
        for (int i = 0; i < N; i++) {
            char diagonalChar = str[i].charAt(i);
            if (diagonalChar == '0') {
                ans.append('1');
            } else {
                ans.append('0');
            }
        }
        return ans.toString();
    }
}
🖥️ Program Output
Input:

Enter T test cases: 
1
4
0101
1010
1111
0000
Output:

1100
```
---
## 📚 Lessons Learned
Learned how to work with binary strings and handle diagonal elements to generate a unique binary string.
Practiced using StringBuilder for efficient string manipulation.
Understood how to use simple conditions to flip binary values ('0' → '1', '1' → '0').

---
## ⚡ Challenges
Ensuring the program handles edge cases, such as strings with identical rows.
Maintaining efficient traversal through the binary strings for larger 
𝑁
N.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn:[Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
