https://msft3c.com/compete/
http://msft3c.com 

# Matrix multiplication | 3 point(s)
Computer graphics, artificial intelligence, and robotics, along with many other applications, rely very heavily on the ability to multiply matrices together. The modern computer game completes millions of matrix multiplications per second. While normally done in hardware, it is important for the game developer to have a deep understanding of how these multiplications work. For this problem, assume the role of a game developer looking to verify some graphics transformations and implement a matrix multiplier.

#### Input definition
The input will be a series of at least two matrices that need to be multiplied together. The Matrices will be bounded on the left and right by | characters and individual entries will be separated by at least one space character. To make things easier, we will stick with integer values (positive and negative).
For example, a 3x3 identity matrix would be represented as follows:
```
| 1 0 0 |
| 0 1 0 |
| 0 0 1 |
```
The multiplication of a 3x3 matrix with a 3x1 column vector matrix would be represented as:
```
| 1 0 0 | | 2 |
| 0 1 0 | | 4 |
| 0 0 1 | | 6 |
```
The | marking the start and end of a matrix will always line up in the input. Thus, a 2x3 matrix multiplied by a 3x2 matrix would be represented as:
```
| 1  2  3  | | -1 -2 |
| 11 12 13 | | 10 11 |
             | -9 -8 |
```
Remember that more than two matrices may be specified in the input.

#### Output definition
The output from the problem should be a matrix formatted in the same manner as the input matrices.

The left and right most character should be a | and all columns should be right aligned. The individual number entries should be separated by at least one space from the | character as well as any other number entry (where the exact number is determinded by column alignment). Negative numbers will be immediately preceeded by a - character.

For example, an output could be as follows:
```
| 1  -2 30 |
| 2 508  7 |
| 3  15 -5 |
| 0   0 18 |
```
Remember, the whitespace within each line must be exact to receive credit. Please ensure you have validated your solution against all practice input provided.

#### Example input
```
| 1 2 3 | |  7  8 |
| 4 5 6 | |  9 10 |
          | 11 12 |
```
#### Example output
```
|  58  64 |
| 139 154 |
```
# Pick your problems | 3 point(s)
  
Imagine for a moment that you are competing in a college coding competition (it's a bit of a stretch, but bear with us). You are given a set of programming problems to solve, and you may solve any number of them in any order before a strict time limit runs out. Each problem has a score and an estimated time to complete.

Typically, you will receive no points for a problem unless it is completely solved. For simplicity, assume that completely solving a problem requires its entire estimated time. However, there is a twist: you may receive partial credit on at most one problem. The partial credit is given in proportion to how close your solution comes to the full, correct solution, which of course depends on how much time you spend working on it. For example, if a problem is worth 5 points and is estimated to take 30 minutes, then if you spend 15 minutes on it, you will receive 2.5 points for it.

Your goal is to write a program to select a subset of problems to solve, such that the total time you would spend solving the problems does not exceed the competition time limit. You should seek to accomplish the following goals in decreasing order of priority:
1. The total score of the subset should be as large as possible. 
2. The subset should contain as many problems as possible. 
3. It is preferred that your solution not contain a partial-credit problem. If you do solve a problem for partial credit, its score should be as low as possible. 

#### Input definition
An input file for this problem will contain no more than 50 lines.

The first line will contain an unsigned integer representing the total duration of the competition in minutes. The following lines will specify the programming problems. A problem specification is three integers separated by commas: problemID,score,durationInMinutes. It is noted that no two problems will have both the same score and duration in minutes.

#### Output definition
An output file for this problem should contain two lines. The first line should show the total score you would receive for solving the problems you chose within the time limit. If the score is fractional, just round down to the nearest integer.

On the second line, list the ID's of the problems you chose to solve, separated by commas with no spaces, and sorted in increasing order. If you chose to solve one of the problems for partial credit, print an asterisk (*) after it in the list.

#### Example input
``` 
60
1,9,30
2,10,32
```
#### Example output
```
18
1*,2
```
# Happy numbers | 2 point(s)
Take any positive number, such as 28. The sum of the squares of its digits is 22 + 82 = 68. If we continue this process, we get the following sequence:

28, 68, 100, 1.

Since the sequence ends in 1, 28 is a happy number.

However, not all numbers are happy. For example, 45 is not a happy number, or is an unhappy number, since it produces the following sequence:

45, 41, 17, 50, 25, 29, 85, 89, 145, 42, 20, 4, 16, 37, 58, 89, ...

at which point the sequence has started to repeat. The process never results in a 1.

For this problem, we will determine if a number is happy or unhappy, and the degree to which it is happy or unhappy.

#### Input definition
The input to your solution will be a list of ten positive integers, one on each line. The smallest possible integer is 1; the largest possible integer is 500,000.

#### Output definition
The output from your solution should be one line per number. Each line should have one word and one number, in that order, separated by one whitespace character.

If the input integer for the line is happy (as defined above), the word happy should be followed by the number of integers in the sequence before a 1 is seen.

If the number is unhappy, the word unhappy should be followed by the number of integers in the sequence before the sequence starts to repeat.

The output should end with an empty line.

#### Example input
```
28
45
1
314159
100
25
4
500000
888
27182
```
#### Example output
```
happy 3
unhappy 15 
happy 0
happy 6
happy 1
unhappy 11
unhappy 8
unhappy 12
happy 4
unhappy 14
```
# Palindromic anagrams | 2 point(s)
A palindrome is a word, phrase, number, or other sequence of characters which reads the same backward or forward. An anagram is the result of rearranging the letters of a word or phrase to produce a new word or phrase, using all of the original letters exactly once.

This problem is a combination of both. You will be given a string and your program needs to check whether or not any of its anagrams contain a palindrome. If none of the anagrams is a palindrome, then you need to find the minimum number of characters to eliminate from the string in order for at least one of its anagrams to be a palindrome. In addition, your program needs to figure out the number of anagrams that are palindromes.

Consider this example: You are given the string "aabd". None of the anagrams of this string are palindrome. If you remove the letter "d", however, then "aba" is an anagram of the string that is a palindrome; if you remove the letter "b", then "ada" is an anagram that is a palindrome. In either case, there is only one anagram that is a palindrome.

#### Input definition
The input file will contain multiple lines. Each line will have a string of lowercase alphabetic characters ('a'-'z'). The length of the string will vary from 1 to 20.

#### Output definition
The output file should contain exactly the same number of lines as the input. Each line of the output should be of the following format: X,Y where X is the minimum number of characters you need to remove from the original string for any of its anagrams to be a palindrome and Y is the total number of anagrams that are palindromic after you remove X characters. Permutations of the same letter within a palindrome do not count; in particular, 'aaa' is 1 palindrome, not 6.

#### Example input
```
aba
acad
agabgb
agqagdt
```
#### Example output
```
0,1
1,1
0,6
2,2
```
# 4-sided figures | 1 point(s)
Given a 3-tuple of side lengths, it is known that one can form a triangle if the sum of any two sides is greater than the remaining side. Given a list of 4-tuples of side lengths, determine if one can form a non-degenerate convex quadrilateral (a strictly four sided figure with no internal angles greater than or equal to 180 degrees).

#### Input definition
The first line contains a positive integer indicating the number (N) of lines to read after the first. Each line after the first contains 4 positive integers separated by single spaces, representing the 4 side lengths.

#### Output definition
The output should contain N lines. Each line should contain either the string "Possible", or "Impossible". The line should say "Possible" if one can form a non-degenerate convex quadrilateral from the 4 given side lengths. Otherwise, it should say "Impossible".

#### Example input
```
8
26 3 13 9
22 39 3 21
34 38 35 7
14 7 10 19
26 36 20 15
33 16 14 11
1 25 26 31
10 27 5 7
```
#### Example output
```
Impossible
Possible
Possible
Possible
Possible
Possible
Possible
Impossible
```
# Bubble sort | 1 point(s)
Of all the classical sorting algorithms, Bubble Sort is likely the most simple to write and to understand.

For this problem we will be sorting a list of numbers using a left to right bubble sort. Starting at the beginning of the list, compare every adjacent pair of numbers. Swap their position if they are not in the right order (i.e. if the right number is smaller than the left number). After doing this with the entire list, start again from the beginning. Each time you start again at the beginning of the list, one less number (the last one compared in the previous iteration) is needed to be compared. Continue these iterations until there are no more elements left to be compared.

The goal of this problem is both to sort the list of numbers as well as to indicate how many times you had to swap a pair. For example, assume your initial list was 5 1 4 2 8. During the first pass, where you compare all pairs, there would be 3 swaps (5 and 1 then 5 and 4 then 5 and 2) resulting in a list of 1 4 2 5 8. During the second pass, there is one additional swap (4 and 2) and you would not compare the pair of 5 and 8. The third pass would result in no swaps and would only compare the first two pairs. The fourth pass would only look at the first pair and would not swap anything. The total number of swaps for this list, therefore, is 4.

#### Input definition
The input for this problem will be a single line of text with a list of non-negative integer numbers. Each number will be separated by a single whitespace character. The list may contain duplicates.

#### Output definition
The result should contain two lines. The first line will be a single number. This number will be the number of swaps you needed to perform in order to sort the list using bubble sort. The second line will be the sorted list of numbers with one space character between each number and no leading or trailing spaces.

#### Example input
`5 1 4 2 8`

#### Example output
```
4
1 2 4 5 8
```

# Radix conversion | 1 point(s)
You are this week's on-call engineer for the web servers managed by your team. One morning (it's still dark outside), you are awakened by a call that one of your services has gone down. You immediately log into the web management portal and download a memory dump of the process that crashed. Unfortunately, the bug that caused the crash has also garbled the memory dump. All of the values in memory have been converted into other numerical bases in the range of [2,36]: some are hexadecimal; some are binary; and some may not even appear on this lengthy list of named bases. Now, you must decipher them using a little radix conversion magic.

#### Input definition
An input file for this problem will contain an arbitrary number of lines.

Each line will contain three parts, separated by commas. The first part is a value from the memory dump. The second part is a decimal integer which represents the radix of the memory value. The third part is a decimal integer representing another radix. You must convert each memory value from the first radix into the second radix.

*Beware:* some inputs will be invalid. Valid radixes will be in the range [2, 36]. Valid memory dump values will contain only lower-case alphanumeric characters, and their decimal representations will fit in a 32-bit signed integer.

#### Output definition
An output file for this problem should contain the same number of lines as the input file.

On each line, print the corresponding memory value expressed in the given radix. The output string should contain only lower-case alphanumeric characters. If the input is invalid or the conversion is impossible, print "Invalid Input" on the line.

#### Example input
```
beef,16,10
10110010,2,16
2343001,8,17
```
#### Example output
```
48879
b2
7b654
```