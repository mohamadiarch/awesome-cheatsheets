


https://quickref.me/regex.html
https://github.com/aloisdg/awesome-regex?tab=readme-ov-file

exampls of world programing:
https://github.com/mmkjony/awesome-regex-1
https://stackoverflow.com/questions/1449817/what-are-some-of-the-most-useful-regular-expressions-for-programmers
---------------




https://gist.github.com/vitorbritto/9ff58ef998100b8f19a0

# Regular Expressions


## Basic Syntax

- `/.../`: Start and end regex delimiters
- `|`: Alternation
- `()`: Grouping


## Position Matching

- `^`: Start of string or start of line in multi-line mode
- `\A`: Start of string
- `$`: End of string or end of line in multi-line mode
- `\Z`: End of string
- `\b`: Word boundary
- `\B`: Not word boundary
- `\<`: Start of word
- `\>`: End of word


## Character Classes

- `\s`: Whitespace
- `\S`: Not whitespace
- `\w`: Word
- `\W`: Not word
- `\d`: Digit
- `\D`: Not digit
- `\x`: Hexade­cimal digit
- `\O`: Octal digit


## Special Characters

- `\n`: Newline
- `\r`: Carriage return
- `\t`: Tab
- `\v`: Vertical tab
- `\f`: Form feed
- `\xxx`: Octal character xxx
- `\xhh`: Hex character hh


## Groups and Ranges

- `.`: Any character except newline (\n)
- `(a|b)`: a or b
- `(…)`: Group
- `(?:…)`: Passive (non-c­apt­uring) group
- `[abc]`: a, b or c
- `[^abc]`: Not a, b or c
- `[a-z]`: Letters from a to z
- `[A-Z]`: Uppercase letters from A to Z
- `[0-9]`: Digits from 0 to 9

> Note: Ranges are inclusive.


## Quantifiers

- `*`: 0 or more
- `+`: 1 or more
- `?`: 0 or 1
- `{3}`: Exactly 3
- `{3,}`: 3 or more
- `{3,5}`: 3, 4 or 5

> Note: Quantifiers are greedy - they match as many times as possible. Add a ? after the quantifier to make it ungreedy.


## Escape Sequences

- `\`:Escape following character. Used to escape any of the following metacharacters: {}[]()^$.|*+?\.
- `\Q`: Begin literal sequence
- `\E`: End literal sequence


## String Replacement

- `$1`: 1st group
- `$2`: 2nd group
- `$n`: nth group
- `$``: Before matched string
- `$'`: After matched string
- `$+`: Last matched string
- `$&`: Entire matched string

> Note: Some regex implem­ent­ations use \ instead of $.


## Assertions

- `?=`: Lookahead assertion
- `?!`: Negative lookahead
- `?<=`: Lookbehind assertion
- ``?!=, ?<!``: Negative lookbehind
- `?>`: Once-only subexp­ression
- `?()`: Condition if-then
- `?()|`: Condition if-then-else
- `?#`: Comment


## POSIX

- `[:upper:]`: Uppercase letters
- `[:lower:]`: Lowercase letters
- `[:alpha:]`: All letters
- `[:alnum:]`: Digits and letters
- `[:digit:]`: Digits
- `[:xdigit:]`: Hexade­cimal digits
- `[:punct:]`: Punctu­ation
- `[:blank:]`: Space and tab
- `[:space:]`: Blank characters
- `[:cntrl:]`: Control characters
- `[:graph:]`: Printed characters
- `[:print:]`: Printed characters and spaces
- `[:word:]`: Digits, letters and underscore


## Pattern Modifiers

- `g`: Global match
- `i`: Case-i­nse­nsitive
- `m`: Multi-line mode. Causes ^ and $ to also match the start/end of lines.
- `s`: Single-line mode. Causes . to match all, including line breaks.
- `x`: Allow comments and whitespace in pattern
- `e`: Evaluate replac­ement
- `U`: Ungreedy mode


--------------------------------------

https://github.com/niklongstone/regular-expression-cheat-sheet


# Regular Expression Cheat Sheet - PCRE 

|Anchor|Description|Example|Valid match|Invalid|
:---|:---|:---|:---|---
^|start of string or line|^foam|foam|bath foam|
\A|start of string in any match mode|\Afoam|foam|bath foam|
$|end of string or line|finish$|finish|finnish|
\Z|end of string, or char before last new line in any match mode|finish\Z|finish|finnish|
\z|end of string, in any match mode.|
\G|end of the previous match or the start of the string for the first match|\^(get\|set)\|\G\w+$|setValue|seValue
\b|word boundary; position between a word character (\w), and a nonword character (\W)|\bis\b|This island is beautiful|This island isn't beautiful
\B|not-word-boundary.|\Bland|island|peninsula

|Assertion|Description|Example|Valid match|Invalid|
:---|:---|:---|:---|---
(?=...)|positive lookahead|question(?=s)|questions|question
(?!...)|negative lookahead|answer(?!s)|answer| answers
(?<=...)|positive look-behind|(?<=appl)e|apple|application
(?<!...)|negative look-behind|(?<!goo)d|mood|good

|Char class|Description|Example|Valid match|Invalid|
:---|:---|:---|:---|---
[ ]|class definition|[axf]|a, x, f|b
[ - ]|class definition range|[a-c]|a, b, c|d
[ \ ]|escape inside class|[a-f\.]|a, b, .| g
[^ ]|Not in class|[^abc]|d, e| a
[:class:]|POSIX class|[:alpha:]|string|0101
.|match any chars except new line|b.ttle|battle, bottle| bttle
\s|white space, [\n\r\f\t ]|good\smorning|good morning|good.morning
\S|no-white space, [^\n\r\f\t]|good\Smorning|good.morning|good morning
\d| digit|\d{2}|23|1a
\D| non-digit|\D{3}|foo, bar|fo1
\w| word, [a-z-A-Z0-9_]|\w{4}|v411|v4.1
\W|non word, [^a-z-A-Z0-9_]|.$%?|.$%?|.ab?

|Special character|Description
:---|:---
\\|general escape|
\n|new line|
\r|carriage return|
\t|tab|
\v|vertical tab|
\f|form feed|
\a|alarm|
[\b]|backspace|
\e|escape|
\cchar|Ctrl + char(ie:\cc is Ctrl+c)
\ooo|three digit octal (ie: \123)
\xhh|one or two digit hexadecimal (ie: \x10)
\x{hex}|any hexadecimal code (ie: \x{1234})
\p{xx}|char with unicode property (ie: \p{Arabic}
\P{xx}|char without unicode property

|Sequence|Description|Example|Valid match|Invalid|
:---|:---|:---|:---|---
\||alternation|apple\|orange|apple, orange|melon
( )| subpattern |foot(er\|ball)|footer or football|footpath
(?P\<*name*>...)|subpattern, and capture submatch into *name*|`(?P<greeting>hello)`|hello|hallo
(?:...)|subpattern, but does not capture submatch|(?:hello)|hello|hallo
+| one or more quantifier|ye+ah|yeah, yeeeah|yah  
*| zero or more quantifier|ye*ah|yeeah, yeeeah, yah|yeh 
?| zero or one quantifier|yes?|yes, ye|yess  
??| zero or one, as few times as possible (lazy)|yea??h|yeah|yeaah|
+?| one or more  lazy |`/<.+?>/g`|`<P>foo</P>` matches only `<P>` and `</P>`|  
*?| zero or more, lazy|`/<.*?>/g`|`<html>`|
{n}|n times exactly|fo{2}|foo|fooo
{n,m}|from n to m times|go{2,3}d|good,goood|gooood
{n,}|at least n times|go{2,}|goo, gooo|go
(?(condition)...)|if-then pattern|`(<)?[p](?(1)>)`|`<p>`, p|<p
(?(condition)...\|...)|if-then-else pattern|`^(?(?=q)que|ans)`|question, answer|quote

|Pattern modifier|Description|
:---|:---
g| global match
i| case-insensitiv, match both uppercase and lowercase
m| multiple lines
s| single line (by default)
x| ingore whitespace allows comments
A| anchored, the pattern is forced to ^
D| dollar end only, a dollar metacharacter matches only at the end 
S| extra analysis performed, useful for non-anchored patterns
U| ungreedy, greedy patterns becomes lazy by default
X| additional functionality of PCRE (PCRE extra)
J| allow duplicate names for subpatterns
u| unicode, pattern and subject strings are treated as UTF-8



---------------------------------------
https://gist.github.com/jonlabelle/3893f6ac9447f7ee27fe


Regular Expression Cheatsheet
=============================

## Anchors

	^   Matches at the start of string or start of line if multi-line mode is
		enabled. Many regex implementations have multi-line mode enabled by
		default.

	$   Matches at the end of string or end of line if multi-line mode is enabled.
		Many regex implementations have multi-line mode enabled by default.

	\A  Matches at the start of the search string.

	\Z  Matches at the end of the search string, or before a newline at the end of the string.

	\z  Matches at the end of the search string.

	\b  Matches at word boundaries.

	\B  Matches anywhere but word boundaries.

## Character Classes

Character classes can be used in ranges.

	.         Matches any character except newline (matches newline in single-line)
	\s        Matches white space characters.
	\S        Matches anything but white space characters.
	\d        Matches digits. Equivalent to [0-9].
	\D        Matches anything but digits. Equivalent to [^0-9].
	\w        Matches letters, digits and underscores. Equivalent to [A-Za-z0-9_].
	\W        Matches anything but letters, digits and underscores.
	\xff      Matches ASCII hexadecimal character ff.
	\x{ffff}  Matches UTF-8 hexadecimal character ffff.
	\A        Matches ASCII control character ^A (case insensitive).
	\132      Matches ASCII octal character 132.

## POSIX Character Classes

*POSIX* Character Classes must be used in bracket expressions, e.g. `[a-z[:upper:]]`.

	[:upper:]   Matches uppercase letters. Equivalent to A-Z.
	[:lower:]   Matches lowercase letters. Equivalent to a-z.
	[:alpha:]   Matches letters. Equivalent to A-Za-z.
	[:alnum:]   Matches letters and digits. Equivalent to A-Za-z0-9.
	[:ascii:]   Matches ASCII characters. Equivalent to \x00-\x7f.
	[:word:]    Matches letters, digits and underscores. Equivalent to \w.
	[:digit:]   Matches digits. Equivalent to 0-9.
	[:xdigit:]  Matches characters that can be used in hexadecimal codes.
	[:punct:]   Matches punctuation.
	[:blank:]   Matches space and tab. Equivalent to [ \t].
	[:space:]   Matches space, tab and newline. Equivalent to \s.
	[:cntrl:]   Matches control characters. Equivalent to [\x00-\x1F\x7F].
	[:graph:]   Matches printed characters. Equivalent to [\x21-\x7E].
	[:print:]   Matches printed characters and spaces. Equivalent to [\x21-\x7E].

## Groups

	(foo|bar)    Matches pattern foo or bar.

	(foo)        Define a group (or subpattern) consisting of pattern foo.
				 Matches within the group can be referenced in a replacement
				 using a backreference.

	(?<foo>bar)  Define a named group named "foo" consisting of pattern bar.
				 Matches within the group can be referenced in a replacement using
				 the backreference $foo.

	(?:foo)      Define a passive group consisting of pattern foo. Passive
				 groups cannot be referenced in a replacement using a
				 backreference.

	(?>foo+)bar  Define an atomic group consisting of pattern foo+. Once foo+ has
				 been matched, the regex engine will not try to find other variable
				 length matches of foo+ in order to find a match followed by a
				 match of bar. Atomic groups may be used for perforamce reasons.

## Bracket Expressions

	[adf]   Matches characters a or d or f.
	[^adf]  Matches anything but characters a, d and f.
	[a-f]   Match any lowercase letter between a and f inclusive.
	[A-F]   Match any uppercase letter between A and F inclusive.
	[0-9]   Match any digit between 0 and 9 inclusive.

## Quantifiers

	*?      Zero or more, lazy. Matches will be as small as possible.
	+       One or more. Matches will be as large as possible.
	+?      One or more, lazy. Matches will be as small as possible.
	?       Zero or one. Matches will be as large as possible.
	??      Zero or one, lazy. Matches will be as small as possible.
	{2}     Two exactly.
	{2,}    Two or more. Matches will be as large as possible.
	{2,}?   Two or more, lazy. Matches will be as small as possible.
	{2,4}   Two, three or four. Matches will be as large as possible.
	{2,4}?  Two, three or four, lazy. Matches will be as small as possible.

## Special Characters

	\   Escape character.
	\n  Matches newline.
	\t  Matches tab.
	\r  Matches carriage return.
	\v  Matches form feed/page break.

## Assertions

	foo(?=bar)   Lookahead assertion. The pattern foo will only match if followed
				 by a match of pattern bar.

	foo(?!bar)   Negative lookahead assertion. The pattern foo will only match if
				 not followed by a match of pattern bar.

	(?<=foo)bar  Lookbehind assertion. The pattern bar will only match if preceded
				 by a match of pattern foo.

	(?<!foo)bar  Negative lookbehind assertion. The pattern bar will only match if
				 not preceded by a match of pattern foo.

## Back References

Back references are used in replacements.

	$3        Matched string within the third non-passive group.
	$0 or $&  Entire matched string.
	$foo      Matched string within the group named "foo".

## Case Modifiers

Case modifiers are used in replacements.

	\u  Make the next character in the replacement uppercase.
	\l  Make the next character in the replacement lowercase.
	\U  Make the remaining characters in the replacement uppercase.
	\L  Make the remaining characters in the replacement lowercase.

## Modifiers

Modifiers can be grouped together, e.g. `(?ixm)`.

	(?i)  Case insensitive mode. Make the remainder of the pattern or subpattern
		  case insensitive.

	(?m)  Multi-line mode. Make $ and ^ in the remainder of the pattern or
		  subpattern match before/after newline.

	(?s)  Single-line mode. Make the . (dot) in the remainder of the pattern or
		  subpattern match newline.

	(?x)  Free spacing mode. Ignore white space in the remainder of the pattern
		  or subpattern.
