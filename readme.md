# Overview

This repository is a part of the Java language training plan. Please read the following guidelines before start.

# Getting Start

## Basic Principals

Each repository contains a gradle java project with a number of unit tests. The initial state of all unit tests are *FAILED*. So the aim is to correct the failed test. Please follow the following steps to get the best experience:

* Read the test code and try to understand what it says.
* Trying to fix the test **WITHOUT RUNNING**. This is very important. Because once you run the test, you may find the failure message of the test telling you the expected result. That means you may lose the chance to figure it out by yourself. Note that you should **ONLY** be able to modify code within the **TODO AREA**. The code outside the **TODO AREA** is **NOT** changable.
* Run the test to examine if the fix is correct.
* Answer the following 4 questions after the test is passed.

The 4 questions are:

1. What is the knowledge point of the test? Where is the offical document to the knowledge point?
1. Why the test failed at first?
1. Why you corrected the test that way?
1. Do you have further questions on this knowledge point?

## Example

Let's take a look at an example:

```java
@Test
void should_pass_by_value() {
  int value = 5;

  tryingToUpdateValue(value);

  // TODO: please modify the following code to pass the test
  // <--start
  final int expected = 0;
  // --end-->

  assertEquals(expected, value);
}
```

First, read the test. From the title and code we can know that the test what to examine the behavior when passing an argument. We are not sure what `tryingToUpdateValue` does, so we can jump into its implementation:

```java
private static void tryingToUpdateValue(int value) {
  value += 2;
}
```

Now we have got the full context of the test. The argument is passed by value so the integer will be copied when passing into `tryingToUpdateValue`. Thus the value from the caller site will not change.

Notice that the todo area is in the test method. So we can modify codes within the todo area to pass the test:

```java
  // TODO: please modify the following code to pass the test
  // <--start
  final int expected = 5;
  // --end-->
```

Please note that not all todo areas are located in test method. And some todo area may have further restrictions, for example:

```java
  // TODO: You should not write concrete number here. Please find a property or constant instead.
  // <!--start
  final int maximumSymbol = 0;
  final int minimumSymbol = 0;
  // --end-->
```

The hint indicates that we should not write concrete number here. So I should not write `3` or `0xffffffff`, but write symbol (e.g. `Integer.MAX_VALUE`).

## Running Test

You could run unit tests with the help of IntelliJ. But it is also possible to run unit test via command line: `./gradlew build`.

If you just want to build your code without running test. Please use `./gradlew build -x test
`

String Test
1. should_be_immutable()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable predefined function String.replace() which replaces string with another string.
  b) Why the test failed at first?
   - list returns null when used list.empty().
  c) Why you corrected the test that way?
   - The list expects boolean.
  d) Do you have further questions on this knowledge point?
   - None
   
2. all_modification_method_will_create_new_string()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about the predefined function String.trim() which removes the trailing spaces.
  b) Why the test failed at first?
   - list returns null when used list.empty().
  c) Why you corrected the test that way?
   - The list expects boolean.
  d) Do you have further questions on this knowledge point?
   - None
   
3. will_create_new_string_when_concat()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about concatenation of strings which appends a string to another string.
  b) Why the test failed at first?
   - list returns null when used list.empty().
  c) Why you corrected the test that way?
   - The list expects boolean.
  d) Do you have further questions on this knowledge point?
   - None
   
4. should_taken_string_apart()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about predefined function of string called "Split" which separates the string based on a string/character.
  b) Why the test failed at first?
   - expected string is always null.
  c) Why you corrected the test that way?
   - The expected result expects a specific string.
  d) Do you have further questions on this knowledge point?
   - None
   
5. should_taken_string_apart_continued()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about predefined function of string called "Split" which separates the string based on a string/character.
  b) Why the test failed at first?
   - expected string is always null.
  c) Why you corrected the test that way?
   - The expected result expects a specific string.
  d) Do you have further questions on this knowledge point?
   - None
   
6. should_break_string_into_words()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about predefined function of string called "Split" which separates the string based on a string/character.
  b) Why the test failed at first?
   - expected string is always null.
  c) Why you corrected the test that way?
   - The expected result expects a specific string.
  d) Do you have further questions on this knowledge point?
   - None
   
7. should_break_string_into_words_customized()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about predefined function of string called "Split" which separates the string based on a string/character.
  b) Why the test failed at first?
   - expected string is always null.
  c) Why you corrected the test that way?
   - The expected result expects a specific string.
  d) Do you have further questions on this knowledge point?
   - None
   
8. should_create_ascii_art()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about predefined function of string builder append() which appends the string to the string builder.
  b) Why the test failed at first?
   - expected string is always null.
  c) Why you corrected the test that way?
   - The expected result expects a specific string using the given width and height.
  d) Do you have further questions on this knowledge point?
   - None
   
9. should_calculate_checksum_of_a_string()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about the predefined values of each character.
  b) Why the test failed at first?
   - expected string is always 0.
  c) Why you corrected the test that way?
   - The expected result is to get the sum per character.
  d) Do you have further questions on this knowledge point?
   - None
   
10. should_convert_unicode_escape()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about the predefined method replace of String.
  b) Why the test failed at first?
   - expected string is null.
  c) Why you corrected the test that way?
   - The expected result is to change the unicode per character.
  d) Do you have further questions on this knowledge point?
   - None
   
11. should_reverse_a_string()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about the predefined method reverse of a string builder
  b) Why the test failed at first?
   - expected string is null.
  c) Why you corrected the test that way?
   - The expected result is to reverse actual code.
  d) Do you have further questions on this knowledge point?
   - None
   
12. should_compare_string_with_different_cases()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about the predefined method checking of string (equals and equalsIgnoreCase)
  b) Why the test failed at first?
   - expected result is null.
  c) Why you corrected the test that way?
   - That is the expected answer to the result.
  d) Do you have further questions on this knowledge point?
   - None
   
13. should_format_string()
  a) What is the knowledge point of the test? Where is the offical document to the knowledge point?
   - To be knowledgeable about the predefined String function called "format".
  b) Why the test failed at first?
   - expected result is null.
  c) Why you corrected the test that way?
   - That is the expected answer to the result.
  d) Do you have further questions on this knowledge point?
   - None