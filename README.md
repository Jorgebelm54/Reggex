# Regex Tutorial Starter Code

A quick tutorial on regex that shos you how you can break it down to learn how to use a regex piece of code to find a set or words a text and or a number 


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

