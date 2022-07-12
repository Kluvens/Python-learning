# Python regular expression

## Python re package - useful functions

```re.search(regex, string, flags)```
- search for a regex match within string
- return object with information about match or None if match fails
- optional parameter modifies matching, e.g. make matching case-insensitive with: flags=re.I

```re.match(regex, string, flags)```
- only match at start of string
- same as re.search starting with ^

```re.fullmatch(regex, string, flags)```
- only match the full string
- same as re.search starting with ^ and ending with $

```re.sub(regex, replacement, string, count, flags)```
- return string with anywhere regex matches, substituted by replacement
- optional parameter count, if non-zero, sets maximum number of substitutions

```re.findall(regex, string, flags)```
- return all non-overlapping matches of pattern in string

```re.split(regex, string, maxsplit, flags)```
- split string everywhere regex matches
- optional parameter maxsplit, if non-zero, set maximum number of splits

## python character classes
- \d - matches any digit, for ASCII: [0-9]
- \D - matches any non-digit, for ASCII: [^0-9]
- \w - matches any word char, for ASCII: [a-zA-Z_0-9]
- \W - matches any non-word char, for ASCII: [^a-zA-Z_0-9]
- \s - matches any whitespace, for ASCII: [ \t\n\r\f]
- \S - matches any non-whitespace, for ASCII: [^ \t\n\r\f]
- \b - matches at a word boundary
- \B - matches except at a word boundary
- \A - matches at the start of the string, same as ^
- \Z - matches at the end of the string, same as $

## raw strings
python raw-string is prefixed with an r(for raw)

Therefore, r'Hello\nAndrew' == 'Hello\\nAndrew'
and print(r'Hello\nAndrew') should give Hello\nAndrew

## match objects
re.search, re.match, re.fullmatch return a match object if a match suceeds, None if it fails.

## capturing parts of a regex match
- brackets are used for grouping in extend regular expressions
- in python brackets also capture the part of the string matched
- group(n) returns part of the string matched by the nth-pair of brackets
- \number can be used to refer to group number in an re.sub replacement string

```
>>> m = re.search('(\w+)\s+(\w+)', 'Hello Andrew')
>>> m.groups()
('Hello', 'Andrew')
>>> m.group(1)
'Hello'
>>> m.group(2)
'Andrew'
```
```
>>> re.sub(r'(\d+) and (\d+)', r'\2 or \1', "The answer is 42 and 43?")
'The answer is 43 or 42?'
```

## back-referencing
- \number can be used further on in a regex - often called a back-reference
```
>>> re.search(r'^(\d+) (\d+)$', '42 43')
<re.Match object; span=(0, 5), match='42 43'>
>>> re.search(r'^(\d+) (\1)$', '42 43')
>>> re.search(r'^(\d+) (\1)$', '42 42')
<re.Match object; span=(0, 5), match='42 42'>
```
- back-references allow matching impossible with classical regular expressions
- python supports up to 99 back-references, \1, \2, \3, …, \99

## non-capturing group
(?:...) is a non-capturing group
- it has the same grouping behaviour as (...)
- it doesn’t capture the part of the string matched by the group
```
>>> m = re.search(r'.*(?:[aeiou]).*([aeiou]).*', 'abcde')
>>> m
<re.Match object; span=(0, 5), match='abcde'>
>>> m.group(1)
'e'
```
