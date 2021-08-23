## Regex-Tutorial


Regex is a method of extracting information from string data. Data is extracted through a process of creating search parameters for patterns and characters. These processed aid in various needs like validating passwords, emails, and urls as well as pulling our specific pieces of data from a string of characters. 


Example of Regex - 

This regex, or regular expression is for validating and matching a URL ^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$

 `^(https?:\/\/)` = `https://` or `http://` 


## Table of Contents
Anchors
Quantifiers
OR Operator
Character Classes
Flags
Grouping and Capturing
Bracket Expressions
Greedy and Lazy Match
Quick References 
References 


`abc` indicators in the following examples are used to mark true values.*

## Anchors

The important of the ^ Carrot and $ dollar sign characters - 

`^` = begins with 
`$` = ends with 
`^Exact Match$` = Exact Match



## Quantifiers

A quantifier defines the order of sequence of the search pattern you are looking for.

Quantifiers are symbolized  `*, +, ? and {}`

Defines the order of what you want to match. Quantifiers are used to designated the kind of match you would like to create to a string input into your app. For example. 

The asterisk `*` will match a string in a string `abc*`, will match ab and c, in case of ab, abc or even abcc but not the b in ‘babc’
`abc*` = `ab` `abc` `abcc` b`abc` `abccccccccc`
ab matches the characters ab literally (case sensitive)
c matches the character c with index 99 x 10

an asterisk that appears after a sequence in parenthesis indicates a group that follows the same logic of the above example 
`a(bc)*` = `a` `abc` abcc `abcbc` `abcbcbc`

The plus `+` will match a string in a  `abc+`, will match the exact string abc or abccc but not 
`abc+  ` = ab `abc` `abcc` `abccc`

The question mark `?` will match a string in `aabc?`, will match the exact string (ab + c) but only 1 c, but not  `‘abccc’`
`abc?` = `ab` `abc` abcc

The curly braces `{ }` indicate an index of iterations of a certain character. 
`abc{2}` = `abcc` abc abcccc


The number inside the curly braces, or index, can be set to match a range, for example  `{2,5}`
`abc{2,5}` = abc `abcc`, `abccc`,`abccc`, or `abccccc`.

For the asterisk * quantifier, the URL 



## OR Operator

the `(|)` or `[ ]` brackets

=either or  
`a(b|c)` = `abc ac acb aob`

`a[ab]` = `abc ac acb aob`


An example of the | used for a(b|c) will match with ab or ac but not aa, bb, cc, ba or ca

An example of the [ ] used for a[bc] will match with ab or ac but not aa, bb, cc, ba or ca.

the brackets [ ] seem to do the same thing as the | but there’s something about the way it groups these matches,


## Character Classes

\d matches a digit (equivalent to [0-9])
`\d`= abc ac acb aob a`2`b a`42`c

`\D` is equivalent to the opposite of the \d command or equal to an non-digit character. 

\w matches any word character (equivalent to [a-zA-Z0-9_])
`\w` = `abc ac acb aob a2b a42c`

\s matches any whitespace character 

`\s` = ` `, `tab`, `space`

. matches any type of character

`.` = 


In order to understand a special character as it's literal meaning they need to be encased in backslashes `\`
`\$\20` = $20 


## Flags

Regex uses slashes to define their search patterns for example `/abc/` in order to create commands that apply to these patterns flags are used outside of these slashes 

`/abc/g` = global = don't return after first match 

`/abc/x` = extended = ignore whitespace 

`/abc/i` = insensitive  = insensitive to uppercase vs lowercase 


## Grouping and Capturing

Grouping and capturing is done with parenthesis ( ) to create a capture group
`a(bc)` = `abc` ac acb aob a2b a42c A87d

Using a(?:bc)* disables the capturing group, though the abc is still a match, a by itself or ‘acf’ is still a match but only if the expression contains the asterisk *. Without the asterisk * only abc will be matched.
`a(?:bc)*` = `abc` `a`c `a`cb `a`ob `a`2b `a`42c A87d



## Bracket Expressions

Bracket Expressions define an array or characters to search for, thy represent the equivalent of `a` or `b` or `c` in the following example:

`[abc]` = `[a|b|c]` = `[a-c]` = `abc` `ac` `acb` `a`o`b` `a`2`b` `a`42`c` A87d



## Greedy and Lazy Match

These are symbolized by `*, +, < >` 

Greedy and Lazy matches are characterized by expanding a search as needed, or a more generalized search 
`<.*?>` = This is a `<Anything Inside this element>` test `</Anything inside this element>` test

## Quick References

• Matching a Hex Value -- /^#?([a-f0-9]{6}|[a-f0-9]{3})$/
• Matching an Email -- /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
• Matching a URL -- /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
• Matching an HTML Tag -- /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

## References

For more information please look to my references: 

https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285

https://regex101.com/

