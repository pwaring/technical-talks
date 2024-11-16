% Advent of Code
% Paul Waring (paul@xk7.net)
% 16th November 2024

# whoami

 - Freelance PHP developer and Linux system administrator
 - Specialise in legacy code/systems and financial services
 - I like trains, politics and technology (@pwaring@fosstodon.org)
 - You may know me from: Geek Walks, Currybeer (but not golf or moths)

# Topics

 - What is Advent of Code?
 - Language options
 - Tips
 - Testing
 - Examples in Go and C
 - Questions at any time

# What is Advent of Code?

 - Annual coding challenge every December
 - 1 puzzle (in two parts) per day in Advent
 - Every year since 2015
 - 100,000+ participants each year
 - Free to take part
 - Supported by sponsorship, donations and merchandise

# What is Advent of Code?

 - Puzzles get progressively (but not linearly) harder as time goes on
 - Your input and answer are unique (c.f. Project Euler)
 - Brute-force solutions often don't work
 - Don't have to solve puzzle n to unlock n+1
 - Puzzles are always available, can try previous years

# Leaderboards

 - Points based on who is first, second etc. to solve a puzzle
 - Puzzles released at midnight EST - 05:00 GMT
 - Global leaderboard fills up *very* quickly
 - Private leaderboards (one per account)

# Languages

 - Use any languages you want
 - Some languages might suit different puzzles
 - Familiar language: solve quickly
 - Choose a language you want to learn / improve
 - Maybe a different paradigm, e.g. functional vs imperative
 - C or Go are my choices most years

# Tips

 - Read the puzzle descriptions carefully
 - Edge cases often catch people out
 - Think about possible interpretations
 - Create a sensible filesystem structure

# Tips

 - Write tests
 - Read the input in one go (especially with C)
 - Build simple data structures - as many as you need
 - Don't worry about optimisation to start with

# Tips

 - Don't get disheartened - days >10 are usually difficult
 - Sometimes puzzles are ambiguous
 - Ambiguous: easy vs impossible
 - Focus on algorithms and data structures
 - Lots of support, especially /r/AdventOfCode and #AdventOfCode
 
# Testing

 - Testing really helps, even for seemingly simple puzzles
 - Break every step into a separate function for testing
 - Get test input working first - but beware of edge cases

# C

 - Challenge: Standard library only
 - Unity is an easy to use test framework
 - Write tests as C functions with 1+ assertions
 - Include as a submodule
 - A good Makefile is your friend - makes it almost rapid prototyping
 
# Go

 - Use the latest version: generics, slices etc.
 - One directory per puzzle part
 - [heredoc](https://github.com/MakeNowJust/heredoc): Embedding strings for tests
 - [testify](https://github.com/stretchr/testify): Better assertions / testing
 - [lo](https://github.com/samber/lo): Maps, filters, reduce etc.

# Examples

 - [2015 Day 2 in C](https://adventofcode.com/2015/day/2)
 - [2023 Day 6 in Go](https://adventofcode.com/2023/day/6)
 - [2023 Day 11 in Go](https://adventofcode.com/2023/day/11)

# Thanks for listening

  - Questions?
  - Slides at: phpdev.uk/talks

