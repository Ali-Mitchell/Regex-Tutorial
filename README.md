## Regex-Tutorial


<!-- ----------------------------- -->


What is Regex - character are used to defind these search parameters

Why use Regex - used to extract information from input strings through a process of creating parameters for matches to known elements in strings of text, for exmaple, emails, passowrd, urls's, ect. 
These search paramaters are based on pattern recognition 

validating passwords, passing specific pieces of data onto other fucntions from a string of text, applicable to almost all programming languages 


Example of Regex - 
This regex, or regular expression is for validating and matching a URL ^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$

Table of Contents
Anchors
Quantifiers
OR Operator
Character Classes
Flags
Grouping and Capturing
Bracket Expressions
Greedy and Lazy Match
Regex Components


#Anchors#

The important of the ^ Carrot and $ dollar sign characters - 

^ = begins with 
$ = ends with 
^Exact Match$ = Exact Match



The use of the first component ^(https?:\/\/) is equivalent to `https://` or `http://` 

question mark in Regex- 

The use of the second component `([\/\w \.-]*)*\/?$`

 matches with //www.google.com/photos The question mark ? right before the dollar sign $ allows for the match of photos in the URL as that allows for optional search patterns after the slash / no match is found if the question mark ? is removed from the expression component or until photo in the URL is removed from the string.

#Quantifiers


defines the sequence of letters and number 
What is a quantifier, 
What is the use of the quantifier- 

Quantifiers are symbolized  `*, +, ? and {}`

Defines the order of what you want to match. Quantifiers are used to designated the kind of match you would like to create to a string input into your app. For example. 

The asterisk `*` will match a string in a string `abc*`, will match ab and c, in case of ab, abc or even abcc but not the b in ‘babc’

The plus `+` will match a string in a  `abc+`, will match the exact string abc or abccc but not 

The question mark `?` will match a string in `aabc?`, will match the exact string (ab + c) but only 1 c, but not  `‘abccc’`

The curly braces `{ }` will match a string  `abc{2}`, will match the exact string `abcc` but not a 3rd or more c or a single c in case of `abc` or `abcccc`, 
The numer 2 inside of these curly braces indicates the number of `c` in the search ans is equal to abcc but not `abc` or `abccc`

The number inside the curly braces, or index, can be set to match a range, for example  `{2,5}` wherein you can match `abcc`, `abccc`,`abccc`,or `abccccc`.

For the asterisk * quantifier, the URL 
 followed by the regex component expression `([\/\w \.-]*)*`. This component expression uses a combination of parts seperated by slashes `/` matches in the slashes in a URL, \w, matches with alpha numeric characters in case of URL string www1 as well as \.- in case of string URL with .com/. The inclusion of `.` and `-` allows for matches before those characters instead of only after those characters in the URL string. The exclusion of the asterisk `*` would prevent any match to the URL to be found or the exclusion of the conditions in the [] would also prevention any matches from being found in the URL string.

#OR Operator

the `(|)` or `[ ]` brackets

=either or  
`a(b|c)` = `abc ac acb aob`

`a[ab]` = `abc ac acb aob`


An example of the | used for a(b|c) will match with ab or ac but not aa, bb, cc, ba or ca

An example of the [ ] used for a[bc] will match with ab or ac but not aa, bb, cc, ba or ca.

the brackets [ ] seem to do the same thing as the | but there’s something about the way it groups these matches,


##Character Classes

\d matches a digit (equivalent to [0-9])
`\d`= abc ac acb aob a`2`b a`42`c

\D is equavalent to the opposite of the \d command or qeual to an non-digit character. 

\w matches any word character (equivalent to [a-zA-Z0-9_])
`\w` = `abc ac acb aob a2b a42c`

\s matches any whitespace character 

`\s` = ` `, `tab`, `space`

. matches any type of character

`.` = 


in order to understand a special character as it's literal meaning they need to be encased in backslaches `\`
`\$\20` = $20 


Character classes \d, \w, and \s
\d matches a number in any string, for example ab2c, 2 is found or de56fghi, 5 and 6 are are found in this string.

\w finds any letter, number and underscore, for example 2bc3_a, or a 1 _ by themselves is found.

\. matches any type of character, event special characters like &, $, *, >, / and .

##Flags

Regex uses slashes to define their search patterns for example `/abc/` in order to create commands that apply to these patterns flags are used outside of these slashes 

`/abc/g` = global = don't return after first match 

`/abc/x` = extended = ignore whitespace 

`/abc/i` = insensitive  = insensitive to uppercase vs lowercase 

##Grouping and Capturing

Grouping and capturing is done with parenthesis ( ) to create a capture group
`a(bc)` = `abc` ac acb aob a2b a42c A87d


Using a(?:bc)* disables the capturing group, though the abc is still a match, a by itself or ‘acf’ is still a match but only if the expression contains the asterisk *. Without the asterisk * only abc will be matched.

Bracket Expressions
Bracket expressions can be as the following [abc], which will match with the string containing either a,b or c singularly like a, b, or c, but also ab, bc or ac for example. You can also use [a-c] which is the same as [abc],Bracket expressions can be as the following [abc], which will match with the string containing either a,b or c singularly like a, b, or c, but also ab, bc or ac for example.

You can also use [a-c] which is the same as [abc], meaning, it will find a match a through c. Think of brackets as a search through a range or spectrum, [a-zA-Z0-9] this will find any characters, from lower case a to lowercase z as well as their uppercase characters, while also finding the numbers 0 through 9.

Greedy and Lazy Match
These are symbolized by *, + and { }. These are greedy operators. For example, this expression <.+> will match with <div> any text between </div>, whereas the question mark ? added to the expression will turn into a lazy one, <.+?>, making this only able to match, just the 2 <div> and </div> but none of the text in-between.
Author
I’m a student learning to code for full stack web development with 6 weeks left in the program. It’s been tough, and it’s been fun with moments of brilliance and getting thigs to work.


David Crockett / CastroOlympias @ GitHub
Thoughts
I wanted to be thorough, but not over do it since I can easily over think things. I can get very detailed about any subject, even in the case of Regex, and don’t want to get lost in the weeds of trial and error. I hope this much is at least adequate to get the ball rolling, but either way. You have to put it into practice, so I do recommend some of these sources, to try it out.

https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285 and https://regex101.com/. Here are some additional sample expressions to try out

• Matching a Hex Value -- /^#?([a-f0-9]{6}|[a-f0-9]{3})$/
• Matching an Email -- /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
• Matching a URL -- /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
• Matching an HTML Tag -- /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/