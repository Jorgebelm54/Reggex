# Title (replace with your title)

Regex Email tutorial 

## Summary

<!-- Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary. -->
Regex is a regular expression ,a pattern that the regular expression engine attempts to match to in input text. A pattern consists  of one or more character literals,operators,or constructors. This is used to help locate thing when in your code by creating patterns that help match,locate and manage text.We some times use a form of a regex patern when using [Command +F ] when searching for something and that is because we are searching for it with specific characters or "literal" characters.

Tutorial on the email regex function on how you would type it out to find it  

example this is one that can pull up an email :
"jorgebelm54@gmail.com" which translates to :"/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g" in Reggex

the letters and all look confusing but worry not its alot simpler than what it may appear.

Lets break it down to the basics-----------------------
/
^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$
/
g
^ asserts position at start of the string
1st Capturing Group ([a-z0-9_\.-]+)
Match a single character present in the list below [a-z0-9_\.-]
+ matches the previous token between one and unlimited times, as many times as possible, giving back as needed (greedy)
a-z matches a single character in the range between a (index 97) and z (index 122) (case sensitive)
0-9 matches a single character in the range between 0 (index 48) and 9 (index 57) (case sensitive)
_ matches the character _ with index 9510 (5F16 or 1378) literally (case sensitive)
\. matches the character . with index 4610 (2E16 or 568) literally (case sensitive)
- matches the character - with index 4510 (2D16 or 558) literally (case sensitive)
@ matches the character @ with index 6410 (4016 or 1008) literally (case sensitive)
2nd Capturing Group ([\da-z\.-]+)
Match a single character present in the list below [\da-z\.-]
+ matches the previous token between one and unlimited times, as many times as possible, giving back as needed (greedy)
\d matches a digit (equivalent to [0-9])
a-z matches a single character in the range between a (index 97) and z (index 122) (case sensitive)
\. matches the character . with index 4610 (2E16 or 568) literally (case sensitive)
- matches the character - with index 4510 (2D16 or 558) literally (case sensitive)
\. matches the character . with index 4610 (2E16 or 568) literally (case sensitive)
3rd Capturing Group ([a-z\.]{2,6})
Match a single character present in the list below [a-z\.]
{2,6} matches the previous token between 2 and 6 times, as many times as possible, giving back as needed (greedy)
a-z matches a single character in the range between a (index 97) and z (index 122) (case sensitive)
\. matches the character . with index 4610 (2E16 or 568) literally (case sensitive)
$ asserts position at the end of the string, or before the line terminator right at the end of the string (if any)
Global pattern flags 
g modifier: global. All matches (don't return after first match) 

-So really every sign and or bracket pulls from a specific piece 
from "literal characters, to numbers, special characters and some cild (wild) which can basically mean anything"



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
A family of Reggex tokens that done really match any character,yet they still say something about the string or the matching process.It does thjo make sure that the engine's current position about the string mtches a well-determined location(example the beggening or the end ) 
### Quantifiers
Quantifiers jow is to  specify how many instances of a character class must be present in the input for the match to be found. 
-Examples of some : --------------------------------------- 
Greedy   /  Lazy 
*	        *?	 {Both a mix of both Greedy and Lazy quantifiers}
+	        +?	    
?	        ??	
{ n }	    { n }?	
{ n ,}	    { n ,}?	
{ n , m }	{ n , m }?
.
The standard quantifiers in regular expressions are greedy, meaning they match as much as they can, only giving back as necessary to match the remainder of the regex. By using a lazy quantifier, the expression tries the minimal match first.
### OR Operator
Logical “or” is more difficult to achieve using tools external to the regular expression engine itself, but it is achievable by combining results of multiple regular expressions using the native “or” logical feature of your programming language of choice. This can sometimes be simpler and easier for others to maintain in the future, with only minimal performance impacts over moderate data-sets

### Character Classes
I=In the contextt of a regular expression, a character is a set or group of characters that are in between a group of squared brackets [] 
Example-------------------------

If you want to match an a or an e, use [ae]

### Flags
Flags in Regex is a paramater that is optional in orer to modify its behavior of searching .The Flag changes the defaulted search behavior of a regular expression a flag is denoted using a single lower case alphabetical character



Example------------------------

i	Ignore Casing	Makes the expression search case-insensitively.
g	Global	Makes the expression search for all occurrences.
s	Dot All	Makes the wild character . match newlines as well.
m	Multiline	Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.
y	Sticky	Makes the expression start its searching from the index indicated in its lastIndex property.
u	Unicode	Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.


### Grouping and Capturing
Grouping is a for or way to attack or treat multiple characters as a whole.They are created by placing the characters to be grouped inside a set of (). for example the regular expression (cat) creates a single group of letters containing "c" "a" "t" 
### Bracket Expressions
A bracket Expression is either a mathing list expression or a non matching list expression .Usually it will consisit of one or more expressions ("ordinary characters ,collating characters , collating symbols,equivalence classes , character classes, or range expressions)      []
Example----------------------------

'elephant'.match(/[abcd]/) // -> matches 'a'


### Greedy and Lazy Match
Regex matching is when a regular expression is a sequence of characters that defines a search pattern,mainly for use in pattern matching with strings, or  string matching, i.e "find and replace operations"


'Greedy' means match longest possible string. 'Lazy' means match shortest possible string.


### Boundaries
The metacharacter \b is an anchor like the caret and the dollar sign. It matches at a position that is called a “word boundary”. This match is zero-length.
the three different positions that qualify as word boundaries ---
example 1 :before the first character in the string , if the first character is a word 

example 2: after the last character in the string , the the last character is a word character 

example 3: between  two characters in the string, where one is a worc character and the other a not word character  
### Back-references
 A bakc-reference in a regex is a expression that identifies a previously matches group and looks for exactly the same text again.  An example is when y you try to search for repeated words in some text . The first part of the match could use a pattern that extracts a single word. 
 Example ---------------------------

 Backreferences match the same text as previously matched by a capturing group. Suppose you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag. Here’s how: <([A-Z][A-Z0-9]*)\b[^>]*>.*?</\1>
### Look-ahead and Look-behind
This is what tells the regex engine to temporarily step backwards in the string , to check if the text inisde the look behind can be matched there 


Example --------------------



<!DOCTYPE html>
<script>
"use strict";

let str = "1 turkey costs 30€";

alert( str.match(/\d+(?=€)/) ); // 30, the number 1 is ignored, as it's not followed by €
</script>

The syntax is: X(?=Y), it means "look for X, but match only if followed by Y". There may be any pattern instead of X and Y.

For an integer number followed by €, the regexp will be \d+(?=€):
## Author
My name is Jorge and if you need to rechout make sure to reach me at jorgebelm54@gmail.com or /Jorgebelm54 on GitHub.
