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

