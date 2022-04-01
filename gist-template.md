# Regular Expressions

Ah, Regular Expressions, the expressions used regularly that no one understands. The magic bit of code that looks like someone mashed their keyboard. Once you know what you're looking at, it does start to make sense. A bit like most other code, when you think about it. That said, most developers don't know how to write their own regex:

![Google search of regex](./assets/images/google.png "Google search of regex")
> 
## Summary

The function of the regex I'll be going through is this:

> /^[^\s@]+@[^\s@]+\.[^\s@]+$/

No, my child didn't decide to play *work* on my laptop. It actually makes sense, and it checks the formatting of emails. I know it works, because I copied and pasted it into one of my projects and it works. It isn't the finest example of regex, nor does it guarantee that an email address is valid, just that its basic structure meets the basic string pattern we've stipulated. 

## Table of Contents

- [Regular Expressions](#regular-expressions)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)

## Regex Components

### Anchors

Left and right, right and left: it makes a difference. Anchors are characters that are used to specify the position of the pattern in relation to the line of text it sits in:

> ^ is the anchor for the start of the line

> $ is the anchor for the end of the line

The order in which these are typed is important too, the ^ must be the first character, the $ must be the last. Typing 'S^' doesn't do anything special, it simply searches for S^ anywhere in the line. Likewise, '$S' isn't special either, it'll find $S anywhere in the line. Here is a table that may explain:

 | Regex  | Result   | 
 | :----: | :------- |
 |  ^X    | Will search for an 'X' at the start of the line |
 |  X$    | Will search for an 'X' at the end of the line |
 |  X^    | Will search for an 'X' anywhere in the line. |
 |  $X    | Will also search for an 'X' anywhere in the line |


### Quantifiers

Quantifiers stipulates how many instances of a character, group, or character class must be present in the line for a match to be identified. This may sound simple and straightforward, but it's not. Quantifiers can be like partners you don't want.... they can be lazy, they can be greedy, they can even be possessive. 

At a default, regex is greedy. It will match as many instances in a line as possible and the greedy part is essential in the match.

When lazy, regex will match as few instances as possible. This can be zero or more; if the nex part of the regex matches, then the lazy part isn't essential.

Possessive regex will take a character it matches, and the character cannot be matched in the next part of the search.

Generally speaking, a quantifier tells the regex engine to match a certhe specified quantity of the character, token or subexpression immediately to its left. For instance:

 | Regex  | Result   | 
 | :----: | :------- |
 |  X+    | the quantifier + applies to the character X |
 |  \x*   | the quantifier * applies to the token \x |
 |  star? | the quantifier ? applies to the character r, *not* to star |
 |  (?:star,\|wars,)+ | the quantifier + applies to the subexpression (?:star,\|wars,) |

### Grouping Constructs

Grouping constructs is

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
