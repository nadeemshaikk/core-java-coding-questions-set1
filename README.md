### Java Coding Questions (Arrays & String Manipulations)

---

#### **Problem 1: Array Sum**

**Problem Statement:**
Given an array of integers, calculate and return the **sum of all its elements**.

**Explanation:**
This is a foundational problem to ensure understanding of array traversal. You need to access each element of the array and add it to a running total.

**Hints:**
* Use a loop (e.g., `for` loop or enhanced `for` loop) to iterate through the array.
* Initialize a variable to `0` to store the sum.
* In each iteration, add the current array element to your sum variable.

**Example:**
Input: `int[] arr = {1, 2, 3, 4, 5};`
Output: `15`

---

#### **Problem 2: Find Maximum in Array**

**Problem Statement:**
Write a function that takes an array of integers and returns the **largest element** in the array. Assume the array is not empty.

**Explanation:**
This problem tests your ability to compare elements within an array and keep track of the maximum value encountered so far.

**Hints:**
* Initialize a variable `max` with the first element of the array.
* Iterate through the rest of the array starting from the second element.
* In each iteration, compare the current element with your `max` variable. If the current element is greater, update `max`.

**Example:**
Input: `int[] arr = {10, 5, 20, 8, 15};`
Output: `20`

---

#### **Problem 3: Count Occurrences of Character**

**Problem Statement:**
Given a string and a character, **count how many times the character appears** in the string (case-sensitive).

**Explanation:**
This problem requires you to iterate through a string and perform a comparison for each character. It's a good introduction to basic string traversal.

**Hints:**
* Convert the string to a character array using `String.toCharArray()` or use `String.charAt(index)` in a loop.
* Initialize a counter variable to `0`.
* Iterate through each character of the string.
* If the current character matches the target character, increment the counter.

**Example:**
Input: `String str = "hello world"; char target = 'o';`
Output: `2`

---

#### **Problem 4: Reverse a String**

**Problem Statement:**
Write a function that takes a string as input and returns a new string with the characters in **reverse order**.

**Explanation:**
This tests your understanding of string immutability and how to build a new string from existing characters in a different order.

**Hints:**
* Strings in Java are **immutable**. You cannot change them in place. You'll need to create a new string.
* You can iterate through the original string from end to beginning.
* Append each character to a `StringBuilder` (recommended for efficiency when building strings in a loop) or concatenate them to a new `String` (less efficient but works for small strings).
* Alternatively, convert the string to a `char[]`, reverse the array, and then convert it back to a `String`.

**Example:**
Input: `String str = "Java";`
Output: `avaJ`

---

#### **Problem 5: Check for Palindrome (String)**

**Problem Statement:**
Determine if a given string is a **palindrome**. A palindrome is a word, phrase, number, or other sequence of characters that reads the same forward and backward (ignoring case).

**Explanation:**
This combines string reversal logic with comparison. You'll need to consider how to ignore case.

**Hints:**
* First, convert the input string to **lowercase** to handle case-insensitivity.
* You can either reverse the string (as in Problem 4) and compare it with the original lowercase string.
* Or, use **two pointers**: one starting at the beginning and one at the end. Move them inwards, comparing characters at each step. If any pair doesn't match, it's not a palindrome.

**Example:**
Input: `String str = "Racecar";`
Output: `true`
Input: `String str = "hello";`
Output: `false`

---

#### **Problem 6: Array Contains Element**

**Problem Statement:**
Given an array of integers and a target integer, **determine if the target integer is present** in the array. Return `true` if found, `false` otherwise.

**Explanation:**
A straightforward search problem, good for practicing linear search.

**Hints:**
* Iterate through each element of the array.
* In each iteration, compare the current element with the target element.
* If a match is found, immediately return `true`.
* If the loop finishes without finding a match, then return `false`.

**Example:**
Input: `int[] arr = {1, 5, 8, 12, 15}; int target = 8;`
Output: `true`
Input: `int[] arr = {1, 5, 8, 12, 15}; int target = 7;`
Output: `false`

---

#### **Problem 7: Remove Spaces from String**

**Problem Statement:**
Write a function that takes a string and returns a new string with **all whitespace characters removed**.

**Explanation:**
This focuses on character filtering within a string.

**Hints:**
* Iterate through the input string character by character.
* For each character, check if it is a whitespace character (e.g., using `Character.isWhitespace(char)`) or just directly compare it to a space character `' '`.
* If it's not a whitespace character, append it to a `StringBuilder`.
* Finally, convert the `StringBuilder` to a `String`.

**Example:**
Input: `String str = "Hello World Java";`
Output: `HelloWorldJava`

---

#### **Problem 8: Count Words in a String**

**Problem Statement:**
Given a sentence (string), **count the number of words** in it. Assume words are separated by single spaces and there are no leading or trailing spaces.

**Explanation:**
This problem introduces the concept of splitting a string based on a delimiter.

**Hints:**
* The easiest way is to use the `String.split()` method. You can split the string by the space character.
* The length of the resulting array will be the number of words.
* Be mindful of empty strings or strings with only spaces if those are edge cases you want to handle (though the problem statement simplifies this).

**Example:**
Input: `String sentence = "This is a sample sentence";`
Output: `5`

---

#### **Problem 9: Find Second Largest in Array**

**Problem Statement:**
Given an array of distinct integers, find and return the **second largest element**. Assume the array has at least two elements.

**Explanation:**
This is slightly more complex than finding the maximum, requiring you to keep track of two largest values.

**Hints:**
* Initialize two variables: `largest` and `secondLargest`.
* Initialize both to a very small number (e.g., `Integer.MIN_VALUE`) or to the first two elements after comparing them.
* Iterate through the array:
    * If the current element is greater than `largest`, then `secondLargest` becomes `largest`, and `largest` becomes the current element.
    * Else if the current element is greater than `secondLargest` (but not `largest`), then `secondLargest` becomes the current element.

**Example:**
Input: `int[] arr = {10, 5, 20, 8, 15};`
Output: `15`

---

#### **Problem 10: Check Anagrams**

**Problem Statement:**
Given two strings, determine if they are **anagrams of each other**. Anagrams are words or phrases formed by rearranging the letters of another, using all the original letters exactly once (case-insensitive).

**Explanation:**
This problem requires a way to normalize the strings (e.g., sort them) to compare their underlying character compositions.

**Hints:**
* First, convert both strings to **lowercase**.
* Check if the lengths of the two strings are equal. If not, they cannot be anagrams.
* Convert both strings to character arrays.
* **Sort** both character arrays.
* Compare the sorted character arrays. If they are identical, the strings are anagrams.

**Example:**
Input: `String s1 = "listen"; String s2 = "silent";`
Output: `true`
Input: `String s1 = "hello"; String s2 = "world";`
Output: `false`
