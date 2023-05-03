## Chapter 2 Stuffs
- Language is a set of finite strings
- Language itself can be infinite
- For eery character, a, in language V1, A is a language. It ise a set of 1 string
- r1 and r2 are languages constructed from regular expressions
- L1(r1) u L2(r2) is a language
- L1(r1) concat L2(r2) is a language
- L1(r1)\* is a language - Kleene closure
- Alpha belongs to L(r) where r is a rexpr. How do we test that
- a\*b\* = {a^n b^m | n >= 0, m >= 0} is a language
- Context sensitive grammar needed for something like alpha belongs to {a^n b^n c^n | n >= 0}
- {a}\* = {a}^0 u {a}^1 u {a}^2 ...
- epsilon is empty string
- null is empty set
- What is alpha?
- Star means take all the elements, make every combination in every order, in every length.

Regex | Description | Example
------|-------------|----------
c | Matches char C | \*
\c | Matches char literally | \\\[ or \( where \[ and \( are in the regular language and not used as meta-symbols
"\~\~\~\~\~\~" | Literal match | "\[" or "Begin" == b e g i n
Concat | Matches any character except for new line | // concant \n - commands in C and c++ Pattern matches any characters up until the new line character
\[\] | Character set/class | \[abc\] == a ∪ b ∪ c
{} | Occurrences of a pattern | \[0-9\]{7,7} have to have a 0-9, 7 times. First number determines the minimum the second number determines the maximum
r? | 0 or 1 or r optional | So something like (+|-)?number could have either a +, a - or nothing at all before the number
\+ | Need to have at least one | \[0-9\]\+ needs to have at least 1 of the numbers between 0-9
\* | Any lenght string of the preceding expression | a\* means that there could either be 0 or any other number of a's
^ | Matches position right after the previous newline. That is matches the first column of the next line.| idk how to show this one tbh
$  | Matches a new line | idk how to show this one either tbh
\\ meta symbol | Escape character | can show \( in a regex expression without it counting as the \( symbol
/ | Matches previous expression if expression after the / is there. Does not match the expression after / | r1/r2

- Identifiers could be written as [a-z]
- 