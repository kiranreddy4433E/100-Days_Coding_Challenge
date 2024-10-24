# Day 2 of 100 - 100 Days of Code Challenge

## Overview
Welcome to **Day 2** of my **100 Days of Code Challenge**! Today, I focused on strengthening my understanding of **Java Data Structures and Algorithms (DSA)** and implemented a new project. As part of this challenge, I’m committed to coding for at least one hour every day, working on real-world projects, and enhancing my problem-solving skills.

## What I did today
Today, I worked on the following:
- Deepened my understanding of **Arrays and Linked Lists** in Java.
- Solved some DSA problems using Java, focusing on time complexity.
- Worked on a small project related to **basic sorting algorithms**.

## Technologies Used
- **Programming Language:** Java
- **Concepts:** Data Structures (Arrays, Linked Lists), Sorting Algorithms

## Links to Code
- [Sorting Algorithms Code](#link-to-repository): A Java program that implements various sorting algorithms such as Bubble Sort, Selection Sort, and Insertion Sort.

## Lessons Learned
- Reinforced my understanding of the efficiency of **sorting algorithms** and the difference in time complexities between **O(n^2)** and better approaches.
- Practiced solving problems using **Arrays** and **Linked Lists**, learning how to optimize space usage and manage dynamic memory in Java.

## Challenges
- Struggled initially with implementing **Insertion Sort** and ensuring it was stable. Eventually overcame this by revisiting the basic theory behind the algorithm and applying it step-by-step.
- Encountered issues with **out-of-bounds exceptions** when working with dynamic arrays, but solved this by handling edge cases properly.

## Next Steps
- Tomorrow, I plan to work on improving the performance of my sorting algorithm implementation by implementing **Merge Sort** and **Quick Sort**.
- I will also begin solving **recursion-based problems** and practice writing test cases for my algorithms.

---

### Connect with me
- **Email:** [kiranreddy4746@gmail.com](mailto:kiranreddy4746@gmail.com)
- **LinkedIn:** [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- **Twitter:** [@kiran4746](https://twitter.com/kiran4746)

---

**[100 Days of Code](https://www.100daysofcode.com/)** is a challenge created by Ajinka Kulakarni, Amit Prabhu. You can find more information about it and join the community using the hashtag `#100DaysOfCode` on Linked in.

```java

package dsa;

import java.util.Scanner;

public class pro_11 {

	public static void main(String[] args) {
	Scanner input = new Scanner(System.in);
	System.out.println("Enter a charecter");
	char ch = input.next().charAt(0);	
	if(ch >= 'a'&& ch <= 'z' || ch >= 'A' && ch <= 'Z') 
		System.out.println("alphabit");

	else 
		System.out.println("not alphabit");
	
      }
}
```

---

### Output
- Enter a character: f
- Alphabet
- Do you want to continue? (y/n): y
- Enter a character: 4
- Not an Alphabet
- Do you want to continue? (y/n): n

