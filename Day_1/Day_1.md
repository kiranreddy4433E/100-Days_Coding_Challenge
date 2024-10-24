# Day 1 of 100 - 100 Days of Code Challenge

## Overview
Welcome to **Day 1** of my **100 Days of Code Challenge**! In this challenge, I am committed to coding for at least an hour every day for the next 100 days. Throughout this journey, I'll be working on various projects, learning new technologies, and sharpening my programming skills.

## What I did today
Today, I worked on the following:
- I implemented a Java program to find vowels and consonants using arrays, `for` loops, and `if-else` statements.

## Technologies Used
- Java (DSA concepts)

## Lessons Learned
- Learned how to use arrays in Java to categorize characters.
- Practiced using `for` loops to iterate over strings.
- Strengthened understanding of `if-else` conditional statements.

## Challenges
- Initially struggled with identifying vowel and consonant logic for edge cases (like special characters), but I was able to resolve it by adding extra conditions in the `if-else` block.

---

### Connect with me
- [LinkedIn](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/) | [Instagram](https://www.instagram.com/kiran_reddy_00/?igsh=MWVueXptdmx4Nm5wZQ%3D%3D) | [Gmail](kiranreddy4746@gmail.com) 

---

**[100 Days of Code](https://www.100daysofcode.com/)** is a challenge created by Ajinka Kulakarni, Amit Prabhu. You can find more information about it and join the community using the hashtag `#100DaysOfCode` on Linked in.

```java
package dsa;

import java.util.Scanner;

public class pro_8 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		String vowel[] = {"a", "e", "i", "o", "u", "A", "E", "I", "O", "U"};
		Scanner input = new Scanner(System.in);
		System.out.println("enter a letter");
		String value;
		value = input.nextLine();
		boolean isVowel = false; 
		for (String v : vowel) {
			if(value.equalsIgnoreCase(v)) {
				isVowel = true;
				break;
				
			}
			
		
		}
		
		if (isVowel) {
			System.out.println("Vowel");
		}
		else if (value.length()!=1 || !Character.isLetter(value.charAt(0))) {
			System.out.println("Invalid input");
		}
		else {
			System.out.println("Consonent");
		}
		
	}

}

