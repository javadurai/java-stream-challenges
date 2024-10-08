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




