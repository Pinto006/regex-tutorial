# Regex Tutorial

Regular expressions or Regex as they are commonly known is a way to search for specific matches.  It is more powerful then a "find" feature you are use to because it can search and match a very spefic group of characters insead of one exact word or number.  For example, if you wanted to find all the names that were Mark in a document you would want to find every spelling combination for that name and search once instead of multiple times for the different combinations. A Regex can help you accomplish this.  This is also how you can validate if a valid email or phone number was inputted on a form correctly.  

## Summary

The regex I will be explaing in this tutorial is a hex value expression.  The expression is used to find all the different combinations of a hastag string.  
A copy of the regex I will be descibing is below:
Matching a Hex Value – /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifier](#quantifier)
- [Capturing Groups](#capturing-groups)
- [Bracket Expressions](#bracket-expressions)
- [Alternation](#alternation)
- [Literals](#literals)

## Regex Components

### Anchors
<mark>/^</mark>#?([a-f0-9]{6}|[a-f0-9]{3})<mark>$/</mark>
The anchors in my expression are /^ and /$. These are to start and end the expression.  /^ indicates the beginning of the string and /$ indicates the end of the string. 

### Quantifier
/^#<mark>?</mark>([a-f0-9]<mark>{6}</mark>|[a-f0-9]<mark>{3}</mark>)$/
The next component is quantifiers. Quantifiers modify the previous charatcer in the expression in a certain way.  They can also considered "greedy" by default but can be changed to "lazy". A greedy quantifier tries to make that as many times as possible and lazy would try to make the match as few times as possible. The characters that used as quantifers are "+", "?", and "{}". The "+" means to match 1 or more.  The "?" means to match 0 or more. The 
"?" in our example is saying to match 0 or more # symbols.  When a number is placed inside "{}" that is he length of characters we are trying to match.  In our example, {6} characters should match [a-f0-9] and then later {3} characters should match [a-f0-9]. 

### Capturing Groups
/^#?<mark>([a-f0-9]{6}|[a-f0-9]{3})</mark>$/

The next component is capturing groups  This is when you want to target a specific group of the match.  The full regex statment is group 0.  Anything you place in () wil groupd that piece of the expression into a group.  You may want to do this to replace that piece of the match or look with group 0. 

### Bracket Expressions
/^#?(<mark>[a-f0-9]</mark>{6}|<mark>[a-f0-9]</mark>{3})$/

The next component is bracket expressions.  In our example they are seen twice as [a-f0-9]. You are asking the expression to match any character within that bracket.  In this example that would be any lower case letter between a and f and any digit between 0 and 9. 

### Alternation
<mark>/^#?([a-f0-9]{6}<mark>|</mark>[a-f0-9]{3})$/<mark>

Alternations give the expression the option to search one thing OR anther.  You can see it in our example with the vertical bar or pipe symbole "|", not to be confused with an uppercase I. In our example, the expression is saying to match [a-f0-9]{6} OR [a-f0-9]{3}.  

### Literals
/^<mark>#</mark>?([a-f0-9]{6}|[a-f0-9]{3})$/

I wanted to also point out the literal that is being using in this regex.  In our example, the literal is "#" meaning we are looking exactly for this character. The quantifiers later change how we want to match and want comes after the literal.  


## Author

My name is Mallorie Pinto.  I am currently working as a beneifts specialist and have taken on a new challenge by enrolling in a coding bootcamp. I am currently 2/3 of the way through my program with UCSD.  I am hoping to change the tergectery of my career and become a full stack web developer. Please see my Github link below. 

[My GitHub](https://github.com/Pinto006?tab=repositories) 
