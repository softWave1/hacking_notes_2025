# Binary Search

# Description
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/5/challenge.zip)

# Solution

-  We use the key principle of binary search algorithm dividing by two all the numbers for getting a complexity of O(log₂n)

``` bash
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 250
Lower! Try again.
Enter your guess: 125
Lower! Try again.
Enter your guess: 62
Higher! Try again.
Enter your guess: 93
Lower! Try again.
Enter your guess: 77
Higher! Try again.
Enter your guess: 85
Lower! Try again.
Enter your guess: 81
Higher! Try again.
Enter your guess: 83
Congratulations! You guessed the correct number: 83
Here's your flag: picoCTF{g00d_gu355_3af33d18}

```