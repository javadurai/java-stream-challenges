# java-stream-challenges

Here are some challenging Java Streams exercises that require deep understanding and creativity in solving:

1. Group and Transform Data

You are given a list of Person objects, each having properties like name, age, and city. Group the people by their city and then create a Map<String, List<String>> where the key is the city, and the value is the list of names of people in that city, sorted alphabetically.

class Person {
    String name;
    int age;
    String city;

    // constructor, getters, setters
}

2. Nested Streams Challenge

You have a list of orders, where each order has a list of items. Each item has a name and price. Calculate the total price of all orders combined, but only include items that start with the letter "A".

class Order {
    List<Item> items;
}

class Item {
    String name;
    double price;
}

3. Flatten and Collect

Given a list of employees, each having a list of projects they are working on, create a distinct list of all projects. Ensure there are no duplicate project names in the resulting list.

class Employee {
    String name;
    List<String> projects;
}

4. Chaining Stream Operations

Given a list of numbers, find the sum of all even numbers that are greater than 50, but only include numbers that are divisible by 7.

List<Integer> numbers = Arrays.asList(12, 54, 63, 77, 86, 98, 45, 73, 123, 56);

5. Complex Partitioning

You have a list of products, each having a price. Partition the products into two groups:

1. Products with prices less than $100.


2. Products with prices equal to or greater than $100.



Further, sort the products within each group by price in descending order.

class Product {
    String name;
    double price;
}

6. Find Longest Word in a Sentence

Given a sentence as a string, split it into words and use Streams to find the longest word. Ignore punctuation and consider a word as any sequence of characters separated by spaces.

String sentence = "Java streams are amazing, aren't they?";

7. Word Frequency Count

Given a list of sentences, calculate the frequency of each word appearing across all sentences. Ignore case and punctuation.

List<String> sentences = Arrays.asList("Hello World", "Hello Java", "Java Streams are powerful");

8. Find Duplicates in a List

Given a list of integers, use streams to find and return a list of all the duplicate numbers (numbers that appear more than once).

List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 2, 3, 7, 8, 9, 7);

9. Character Frequency in String

Write a program that takes a string and counts the frequency of each character (excluding spaces) using streams. Return a Map<Character, Long> with the character as the key and the count as the value.

String input = "Java Streams are cool!";

10. Custom Collector

Write a custom Collector that can accumulate the average of a stream of Person objects based on their age.

class Person {
    String name;
    int age;
}

These challenges cover advanced use cases of streams, including grouping, partitioning, custom collectors, and nested data structures. They require good knowledge of stream API features like filter(), map(), collect(), flatMap(), and custom collectors.

Here are additional challenging Java Streams exercises that will test your problem-solving skills with streams:

1. Top N Elements by Criteria

Given a list of students with their scores, find the top 3 students with the highest scores. If two students have the same score, prioritize the one with the lexicographically smaller name.

class Student {
    String name;
    int score;
}

2. Find the Most Frequent Element

Given a list of integers, find the most frequent number using streams. If there is a tie for the most frequent number, return the smallest one.

List<Integer> numbers = Arrays.asList(1, 3, 5, 3, 7, 5, 5, 1, 1);

3. Transform List of Maps to a Single Map

You have a list of maps where each map contains a key-value pair of type <String, Integer>. Combine all the maps into a single map where the keys remain unique, and the values are summed up.

List<Map<String, Integer>> listOfMaps = Arrays.asList(
    Map.of("a", 1, "b", 2),
    Map.of("a", 2, "c", 3),
    Map.of("b", 1, "d", 4)
);

4. Cartesian Product with Streams

Given two lists of integers, generate the Cartesian product of these lists, i.e., all possible pairs (x, y) where x is from the first list and y is from the second list. Collect the pairs into a list of int[] arrays.

List<Integer> list1 = Arrays.asList(1, 2, 3);
List<Integer> list2 = Arrays.asList(4, 5, 6);

5. Anagrams Grouping

Given a list of strings, group all anagrams together. For example, ["eat", "tea", "tan", "ate", "nat", "bat"] should be grouped as ["eat", "tea", "ate"], ["tan", "nat"], and ["bat"].

List<String> words = Arrays.asList("eat", "tea", "tan", "ate", "nat", "bat");

6. Remove Consecutive Duplicates

Given a list of strings, remove consecutive duplicate elements but keep other duplicates. For example, ["apple", "apple", "banana", "apple", "banana", "banana"] should become ["apple", "banana", "apple", "banana"].

List<String> words = Arrays.asList("apple", "apple", "banana", "apple", "banana", "banana");

7. Find the Median Using Streams

Given a list of integers, find the median. The list may or may not be sorted. If the list size is even, return the average of the two middle numbers.

List<Integer> numbers = Arrays.asList(12, 5, 8, 7, 3, 9, 10);

8. Palindrome Finder

Given a list of strings, use streams to find all palindromes (strings that are the same forwards and backwards) and collect them into a list.

List<String> words = Arrays.asList("madam", "racecar", "hello", "level", "world");

9. Longest Increasing Subsequence

Given a list of integers, use streams to find the longest increasing subsequence (a sequence where each number is greater than the previous one).

List<Integer> numbers = Arrays.asList(1, 3, 5, 4, 7, 6, 8, 9);

10. Duplicate Detection in a Stream

Given a stream of integers, determine if there is any duplicate number in the stream. Use a custom stateful operation with a Collector.

List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 3, 6);

11. Circular Permutations of a String

Given a string, generate all circular permutations of the string (rotations where the start of the string is moved to the end). For example, the string "abc" would result in ["abc", "bca", "cab"].

String input = "abc";

12. Summing Numbers by Prefix

Given a list of strings that represent numbers with prefixes (e.g., "A123", "B456", "A789"), sum the numbers by their prefix and return a map where the key is the prefix and the value is the sum of the numbers.

List<String> numbersWithPrefix = Arrays.asList("A123", "B456", "A789", "B111");

13. Longest Word Without Repeating Characters

Given a list of words, find the longest word that contains no repeating characters. Ignore words with repeated characters.

List<String> words = Arrays.asList("hello", "world", "stream", "java", "programming");

14. Sublist of Largest Sum

Given a list of integers, use streams to find the sublist that has the largest sum. This is a version of the maximum subarray problem (Kadane’s algorithm).

List<Integer> numbers = Arrays.asList(-2, 1, -3, 4, -1, 2, 1, -5, 4);

15. Reverse Each Word in a Sentence

Given a string representing a sentence, reverse each word in the sentence but keep the word order the same.

String sentence = "Java Streams are fun";

16. Find and Replace with Streams

Given a list of strings, find and replace all instances of a target substring with a replacement substring using streams. For example, replace all "foo" with "bar".

List<String> words = Arrays.asList("foo", "foobar", "barfoo", "bar");
String target = "foo";
String replacement = "bar";

17. Sum of First N Fibonacci Numbers

Write a program that generates the first N Fibonacci numbers and finds their sum using streams.

int N = 10;  // N can be any positive integer

18. Find Kth Largest Element

Given a list of integers, use streams to find the Kth largest element in the list.

List<Integer> numbers = Arrays.asList(12, 5, 8, 7, 3, 9, 10);
int k = 3;  // Kth largest

These exercises will deepen your understanding of Java Streams and require creative usage of stream operations such as flatMap(), groupingBy(), partitioningBy(), and custom collectors.

Here are more advanced Java Streams challenges that will further test your understanding and push your skills:

1. Finding Common Elements in Multiple Lists

Given a list of lists, where each list contains integers, find the common elements that are present in all lists using streams.

List<List<Integer>> listOfLists = Arrays.asList(
    Arrays.asList(1, 2, 3, 4),
    Arrays.asList(2, 3, 5, 7),
    Arrays.asList(3, 6, 7, 2)
);

2. Sum of Digits in String

Given a string containing alphanumeric characters, use streams to find the sum of all the digits in the string.

String input = "a1b2c3d4e5";

3. Grouping By Range

Given a list of integers, group them into different ranges (e.g., 0-10, 11-20, etc.) and return a map where the key is the range and the value is a list of integers in that range.

List<Integer> numbers = Arrays.asList(1, 5, 12, 19, 22, 7, 13, 9, 30);

4. Finding Longest Substring Without Repeating Characters

Given a string, use streams to find the longest substring that doesn’t contain any repeating characters.

String input = "abcabcbb";

5. Nested Map Grouping

You are given a list of employees, each having a department and a city as properties. Group employees by their department first and then by their city.

class Employee {
    String name;
    String department;
    String city;
}

List<Employee> employees = Arrays.asList(
    new Employee("Alice", "HR", "New York"),
    new Employee("Bob", "HR", "Boston"),
    new Employee("Charlie", "Finance", "New York"),
    new Employee("David", "Finance", "Boston")
);

6. Max Occurrence of Character in Each Word

Given a list of strings, for each string, find the character that occurs the most times. In case of a tie, return the lexicographically smallest character.

List<String> words = Arrays.asList("apple", "banana", "cherry");

7. Sum of Diagonals in a Matrix

Given a square matrix of integers represented as a list of lists, use streams to find the sum of both the main diagonal and the anti-diagonal elements.

List<List<Integer>> matrix = Arrays.asList(
    Arrays.asList(1, 2, 3),
    Arrays.asList(4, 5, 6),
    Arrays.asList(7, 8, 9)
);

8. Calculate Average Length of Words in Sentence

Given a sentence, use streams to calculate the average length of the words in the sentence. Ignore punctuation and special characters.

String sentence = "The quick brown fox jumps over the lazy dog.";

9. Substrings of Length N

Given a string and an integer N, use streams to generate all substrings of length N.

String input = "abcdef";
int N = 3;

10. Reversing Only Words of Specific Length

Given a sentence, reverse all words that are of a specific length N while leaving other words unchanged.

String sentence = "Java streams are really powerful and useful";
int N = 5;

11. Find the Mode (Most Frequent Number)

Given a list of integers, find the mode (the number that appears most frequently). In case of a tie, return the smallest number.

List<Integer> numbers = Arrays.asList(3, 5, 2, 3, 5, 7, 3, 5, 5);

12. Calculate Product of Non-Zero Numbers

Given a list of integers, use streams to calculate the product of all non-zero numbers.

List<Integer> numbers = Arrays.asList(1, 2, 3, 0, 4, 5, 0);

13. Replace Each Word with Its Length

Given a sentence, replace each word with its length. For example, "Java is fun" becomes "4 2 3".

String sentence = "Streams in Java are powerful";

14. Intersection of Two Lists

Given two lists of integers, find the intersection (common elements) of the two lists using streams.

List<Integer> list1 = Arrays.asList(1, 2, 3, 4, 5);
List<Integer> list2 = Arrays.asList(3, 4, 5, 6, 7);

15. Maximum Occurrence of a Character in a String

Given a string, find the character that occurs the most times. If two characters occur the same number of times, return the lexicographically smallest one.

String input = "success";

16. Count the Frequency of Words Starting with Vowel

Given a list of words, count how many words start with a vowel (A, E, I, O, U). Ignore case.

List<String> words = Arrays.asList("apple", "banana", "orange", "umbrella", "egg");

17. Sum of Odd-Indexed Numbers

Given a list of integers, find the sum of the elements that are located at odd indices (1, 3, 5, etc.).

List<Integer> numbers = Arrays.asList(10, 20, 30, 40, 50, 60);

18. Find All Subsets of a List

Given a list of integers, generate all possible subsets of the list using streams. Each subset should be represented as a list.

List<Integer> numbers = Arrays.asList(1, 2, 3);

19. First Non-Repeated Character in String

Given a string, use streams to find the first non-repeated character. If all characters are repeated, return an empty result.

String input = "swiss";

20. Count the Number of Palindromes

Given a list of strings, count how many of the strings are palindromes.

List<String> words = Arrays.asList("madam", "racecar", "hello", "level", "java");

21. Find Pairs of Integers That Add Up to a Target

Given a list of integers and a target value, find all pairs of integers that sum up to the target. Ensure that each pair is distinct (order does not matter, e.g., (3, 5) and (5, 3) should be considered the same).

List<Integer> numbers = Arrays.asList(2, 4, 3, 5, 6, 1);
int target = 7;

22. Sort Strings by Length and Alphabetically

Given a list of strings, sort them first by length and then alphabetically for strings of the same length.

List<String> words = Arrays.asList("apple", "pear", "banana", "kiwi", "grape");

23. Finding All Unique Triplets That Sum to Zero

Given a list of integers, find all unique triplets in the list that sum to zero.

List<Integer> numbers = Arrays.asList(-1, 0, 1, 2, -1, -4);

24. Sliding Window Average

Given a list of integers, compute the average of every sliding window of size N.

List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9);
int N = 3;

25. Merge Two Sorted Lists into One Sorted List

Given two sorted lists of integers, merge them into one sorted list using streams.

List<Integer> list1 = Arrays.asList(1, 3, 5);
List<Integer> list2 = Arrays.asList(2, 4, 6);

These challenges involve complex operations such as groupings, finding intersections, handling nested collections, manipulating substrings, and solving problems with sliding windows, subsets, and permutations. They will help deepen your proficiency with Java Streams.



tougher ones

Here are even tougher Java Streams challenges along with the expected results. These problems are designed to stretch your thinking and cover advanced topics.

1. Find Maximum Repeated Subsequence

Problem: Given a string, find the most repeated subsequence of characters. A subsequence is defined as any sequence derived from another sequence by deleting some or no elements without changing the order of the remaining elements.

Input:

String input = "abcabcbb";

Expected Result: "abc" (since "abc" appears twice as a subsequence).


---

2. Kth Largest Element in an Infinite Stream

Problem: Given an infinite stream of integers, find the K-th largest element at any given point using streams.

Input:

List<Integer> stream = Arrays.asList(5, 2, 9, 11, 3, 7);
int k = 3;

Expected Result: At the end of the stream, the 3rd largest element is 7.


---

3. Flatten Nested Map and Compute Sum

Problem: Given a deeply nested Map<String, Object>, where the values can be integers or other maps, flatten the map and compute the sum of all integers.

Input:

Map<String, Object> nestedMap = Map.of(
    "a", 5,
    "b", Map.of("c", 3, "d", Map.of("e", 7)),
    "f", 10
);

Expected Result: 25 (sum of 5, 3, 7, and 10).


---

4. Permutations with Constraints

Problem: Given a list of integers, generate all possible permutations of the list. However, ensure that permutations with any number repeating consecutively are excluded.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 2);

Expected Result: [[1, 2, 2], [2, 1, 2]] (permutations like [2, 2, 1] are excluded).


---

5. Lexicographically Smallest Substring After Removing k Characters

Problem: Given a string and an integer k, remove exactly k characters from the string such that the resulting string is lexicographically the smallest possible.

Input:

String input = "abcdxyz";
int k = 3;

Expected Result: "abcy" (after removing d, x, and z).


---

6. Find the Longest Arithmetic Subsequence

Problem: Given a list of integers, find the length of the longest arithmetic subsequence. An arithmetic subsequence is a subsequence of numbers where the difference between consecutive numbers is the same.

Input:

List<Integer> numbers = Arrays.asList(1, 7, 10, 13, 14, 19);

Expected Result: 4 (the longest arithmetic subsequence is 1, 7, 13, 19).


---

7. First Missing Positive Integer

Problem: Given a list of integers (both positive and negative), use streams to find the smallest positive integer that is missing from the list.

Input:

List<Integer> numbers = Arrays.asList(3, 4, -1, 1);

Expected Result: 2 (since 1 and 3 are present, the smallest missing positive integer is 2).


---

8. Find Maximum Product of Three Numbers

Problem: Given a list of integers, find the maximum product that can be obtained by multiplying any three numbers in the list.

Input:

List<Integer> numbers = Arrays.asList(-10, -10, 5, 2);

Expected Result: 500 (maximum product is -10 * -10 * 5 = 500).


---

9. Sum of the Elements Formed by Concatenating Pairs

Problem: Given a list of integers, generate all possible pairs of numbers by concatenating them and find the sum of all these concatenated values.

Input:

List<Integer> numbers = Arrays.asList(12, 34);

Expected Result: 1234 + 3412 = 4646.


---

10. Find All Anagrams of a Word in a List

Problem: Given a list of words, find all anagrams of a given word from the list.

Input:

List<String> words = Arrays.asList("enlist", "google", "inlets", "banana");
String target = "listen";

Expected Result: ["enlist", "inlets"].


---

11. Group Consecutive Integers Together

Problem: Given a list of integers, group all consecutive numbers together into sublists.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 3, 5, 6, 8, 9, 10);

Expected Result: [[1, 2, 3], [5, 6], [8, 9, 10]].


---

12. Find the Longest Palindromic Substring

Problem: Given a string, use streams to find the longest palindromic substring.

Input:

String input = "babad";

Expected Result: "bab" (or "aba", since both are palindromic).


---

13. Find Numbers Forming the Largest Possible Number

Problem: Given a list of non-negative integers, arrange them such that they form the largest possible number.

Input:

List<Integer> numbers = Arrays.asList(3, 30, 34, 5, 9);

Expected Result: "9534330" (since this is the largest possible number).


---

14. Find the Most Frequent Sum of Subsets

Problem: Given a list of integers, find the sum of all non-empty subsets and return the most frequently occurring sum.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 3);

Expected Result: 3 (subsets: {1}, {2}, {3}, {1,2}, {1,3}, {2,3}, {1,2,3}; sum 3 appears the most frequently).


---

15. K Largest Elements with Unique Digits

Problem: Given a list of integers, find the k largest numbers that have unique digits (i.e., no repeated digits).

Input:

List<Integer> numbers = Arrays.asList(123, 234, 112, 567, 654);
int k = 2;

Expected Result: [654, 567] (these are the two largest numbers without repeating digits).


---

16. Find the Smallest Window Containing All Characters of Another String

Problem: Given two strings S1 and S2, find the smallest substring in S1 that contains all characters of S2.

Input:

String S1 = "this is a test string";
String S2 = "tist";

Expected Result: "t stri" (this is the smallest window containing tist).


---

17. Find Longest Subarray with Sum Equal to K

Problem: Given an array of integers and a target K, find the length of the longest subarray that sums to K.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 3, 7, 5);
int K = 12;

Expected Result: 2 (subarray [7, 5] sums to 12).


---

18. Count the Number of Subsequences with Sum Greater Than K

Problem: Given a list of integers and a target K, count the number of subsequences whose sum is greater than K.

Input:

List<Integer> numbers = Arrays.asList(3, 1, 4, 2);
int K = 5;

Expected Result: 7 (possible subsequences: [3,4], [3,1,4], [3,1,4,2], [3,2], [4,2], [1,4,2], [3,4,2]).


---

Here are additional challenging Java Streams problems, complete with expected results:

20. Find All Unique Pairs with a Given Sum

Problem: Given a list of integers and a target sum, find all unique pairs that add up to the target sum. Each pair should be returned only once, regardless of the order.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 3, 2, 4, 5);
int target = 5;

Expected Result: [(2, 3), (1, 4)] (the pairs that sum to 5).


---

21. Calculate Frequency of Each Character in a String

Problem: Given a string, calculate the frequency of each character and return a map of characters to their respective frequencies.

Input:

String input = "programming";

Expected Result: {'p': 1, 'r': 2, 'o': 1, 'g': 2, 'a': 1, 'm': 2, 'i': 1, 'n': 1}.


---

22. Sort List of Employees by Name and Salary

Problem: Given a list of employees with names and salaries, sort the employees first by their names alphabetically and then by their salaries in descending order.

Input:

List<Employee> employees = Arrays.asList(
    new Employee("Alice", 50000),
    new Employee("Bob", 60000),
    new Employee("Alice", 70000),
    new Employee("David", 60000)
);

Expected Result: [(Alice, 70000), (Alice, 50000), (Bob, 60000), (David, 60000)].


---

23. Find the Longest Consecutive Sequence

Problem: Given a list of integers, find the length of the longest consecutive elements sequence.

Input:

List<Integer> numbers = Arrays.asList(100, 4, 200, 1, 3, 2);

Expected Result: 4 (the longest consecutive sequence is [1, 2, 3, 4]).


---

24. Group Anagrams

Problem: Given a list of strings, group the anagrams together in a list of lists.

Input:

List<String> words = Arrays.asList("eat", "tea", "tan", "ate", "nat", "bat");

Expected Result: [[eat, tea, ate], [tan, nat], [bat]].


---

25. Find the Most Frequent Character in a String

Problem: Given a string, find the character that appears the most and its frequency.

Input:

String input = "successes";

Expected Result: ('s', 5) (character 's' appears 5 times).


---

26. Generate Combinations of Elements

Problem: Given a list of elements, generate all possible combinations of these elements.

Input:

List<String> elements = Arrays.asList("a", "b", "c");

Expected Result: [[], [a], [b], [c], [a, b], [a, c], [b, c], [a, b, c]] (all combinations including the empty set).


---

27. Find Missing Number in Array

Problem: Given an array containing n distinct numbers taken from 0, 1, 2, ..., n, find the one number that is missing.

Input:

List<Integer> numbers = Arrays.asList(3, 0, 1);

Expected Result: 2 (the missing number).


---

28. Count Distinct Subsequences of a Given String

Problem: Given a string, find the number of distinct subsequences it has.

Input:

String input = "aba";

Expected Result: 5 (the distinct subsequences are "", "a", "b", "ab", "aa").


---

29. Find Palindrome Pairs

Problem: Given a list of words, find all pairs of unique indices (i, j) such that the concatenation of words[i] + words[j] is a palindrome.

Input:

List<String> words = Arrays.asList("bat", "tab", "cat");

Expected Result: [(0, 1), (1, 0)] (both "bat" + "tab" and "tab" + "bat" form palindromes).


---

30. Find the N-th Fibonacci Number Using Streams

Problem: Calculate the N-th Fibonacci number using Java Streams.

Input:

int n = 10;

Expected Result: 55 (the 10th Fibonacci number).


---

31. Count the Number of Valid Parentheses Combinations

Problem: Given an integer n, return all combinations of well-formed parentheses.

Input:

int n = 3;

Expected Result: ["((()))", "(()())", "(())()", "()(())", "()()()"].


---

32. Find the Intersection of Two Lists

Problem: Given two lists, find their intersection without duplicates.

Input:

List<Integer> list1 = Arrays.asList(1, 2, 2, 1);
List<Integer> list2 = Arrays.asList(2, 2);

Expected Result: [2].


---

33. Find Pairs with a Specific Difference

Problem: Given a list of integers and a number k, find all unique pairs of integers in the list that have a difference of k.

Input:

List<Integer> numbers = Arrays.asList(1, 5, 3, 4, 2);
int k = 2;

Expected Result: [(1, 3), (3, 5), (2, 4)].


---

34. Calculate Cumulative Sum of a List

Problem: Given a list of integers, compute the cumulative sum (running total) at each position in the list.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 3, 4);

Expected Result: [1, 3, 6, 10].


---

35. Remove Duplicates from a List while Maintaining Order

Problem: Given a list of integers, remove duplicates without changing the order of elements.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 3, 2, 1, 4);

Expected Result: [1, 2, 3, 4].


---

36. Longest Substring Without Repeating Characters

Problem: Given a string, find the length of the longest substring without repeating characters.

Input:

String input = "abcabcbb";

Expected Result: 3 (the longest substring is "abc").


---

37. Count Vowels and Consonants in a String

Problem: Given a string, count the number of vowels and consonants.

Input:

String input = "Hello World!";

Expected Result: Vowels: 3, Consonants: 7.


---

38. Find All Triplets with a Given Sum

Problem: Given an array of integers, find all unique triplets that sum up to zero.

Input:

List<Integer> numbers = Arrays.asList(-1, 0, 1, 2, -1, -4);

Expected Result: [[-1, -1, 2], [-1, 0, 1]].


---

39. Generate All Valid Parentheses

Problem: Given n pairs of parentheses, generate all combinations of valid parentheses.

Input:

int n = 3;

Expected Result: ["((()))", "(()())", "(())()", "()()()"].


---

40. Find the Median of Two Sorted Arrays

Problem: Given two sorted arrays, find the median of the two sorted arrays.

Input:

List<Integer> nums1 = Arrays.asList(1, 3);
List<Integer> nums2 = Arrays.asList(2);

Expected Result: 2.0



Here are more challenging Java Streams problems, including expected results:

41. Flatten a List of Lists

Problem: Given a list of lists, flatten it into a single list.

Input:

List<List<Integer>> listOfLists = Arrays.asList(
    Arrays.asList(1, 2, 3),
    Arrays.asList(4, 5),
    Arrays.asList(6, 7, 8, 9)
);

Expected Result: [1, 2, 3, 4, 5, 6, 7, 8, 9].


---

42. Count Distinct Elements in a List

Problem: Given a list, count the number of distinct elements.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 2, 3, 4, 4, 4);

Expected Result: 4 (distinct elements are 1, 2, 3, 4).


---

43. Sum of Even and Odd Numbers Separately

Problem: Given a list of integers, calculate the sum of even numbers and the sum of odd numbers.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);

Expected Result: Even Sum: 6, Odd Sum: 9.


---

44. Reverse Words in a String

Problem: Given a string, reverse the order of words.

Input:

String input = "Java is fun";

Expected Result: "fun is Java".


---

45. Calculate the Average of a List

Problem: Given a list of integers, calculate the average.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);

Expected Result: 3.0.


---

46. Count Characters in a String (Ignoring Spaces)

Problem: Given a string, count the number of characters excluding spaces.

Input:

String input = "Hello World!";

Expected Result: 10.


---

47. Find Second Largest Number in a List

Problem: Given a list of integers, find the second largest number.

Input:

List<Integer> numbers = Arrays.asList(3, 1, 4, 4, 2, 5);

Expected Result: 4.


---

48. Group by Length of Strings

Problem: Given a list of strings, group them by their lengths.

Input:

List<String> words = Arrays.asList("a", "abc", "ab", "abcd", "ab");

Expected Result: {"1": ["a"], "2": ["ab", "ab"], "3": ["abc"], "4": ["abcd"]}.


---

49. Check if a String is a Palindrome

Problem: Given a string, check if it is a palindrome.

Input:

String input = "A man a plan a canal Panama";

Expected Result: true.


---

50. Find All Combinations of a Given Length

Problem: Given a list of characters, find all combinations of a specified length.

Input:

List<Character> chars = Arrays.asList('a', 'b', 'c');
int length = 2;

Expected Result: ["ab", "ac", "ba", "bc", "ca", "cb"].


---

51. Count Words in a Sentence

Problem: Given a sentence, count the number of words.

Input:

String sentence = "Count the words in this sentence.";

Expected Result: 7.


---

52. Check for Anagram

Problem: Given two strings, check if they are anagrams of each other.

Input:

String str1 = "listen";
String str2 = "silent";

Expected Result: true.


---

53. Calculate Product of All Elements in a List

Problem: Given a list of integers, calculate the product of all elements.

Input:

List<Integer> numbers = Arrays.asList(1, 2, 3, 4);

Expected Result: 24.


---

54. Find Unique Characters in a String

Problem: Given a string, find all unique characters.

Input:

String input = "programming";

Expected Result: ['p', 'o', 'g', 'r', 'a', 'm', 'i', 'n'].


---

55. Generate Fibonacci Series Up to N

Problem: Generate the Fibonacci series up to a given number n.

Input:

int n = 10;

Expected Result: [0, 1, 1, 2, 3, 5, 8].


---

56. Find Minimum and Maximum in a List

Problem: Given a list of integers, find the minimum and maximum values.

Input:

List<Integer> numbers = Arrays.asList(3, 5, 1, 9, 2);

Expected Result: Min: 1, Max: 9.


---

57. Sort Strings by Length

Problem: Given a list of strings, sort them by length.

Input:

List<String> words = Arrays.asList("short", "longer", "tiny", "medium");

Expected Result: ["tiny", "short", "medium", "longer"].


---

58. Find the First Non-Repeated Character

Problem: Given a string, find the first non-repeated character.

Input:

String input = "swiss";

Expected Result: 'w'.


---

59. Check if a Number is Prime

Problem: Given an integer, check if it is a prime number.

Input:

int number = 29;

Expected Result: true.


---

60. Find All Subsets of a Set

Problem: Given a set of distinct integers, return all possible subsets.

Input:

List<Integer> nums = Arrays.asList(1, 2, 3);

Expected Result: [[], [1], [2], [3], [1, 2], [1, 3], [2, 3], [1, 2, 3]].



