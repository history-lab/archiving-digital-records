---
marp: true
theme: gaia
class:
  - invert
paginate: true
---
<!-- _class: lead -->
# Text Analytics 101
---
# Text Analytics Defined
* Mostly about quantification (e.g. word counting)
* Augment reading vs replacing it        
---
# Common Text Analytics Techniques
---
# Text Analytics vs Natural Language Processing (NLP)


---
# Close Reading vs Distant Reading
* Close reading: careful study of a single text

* Distant reading: text analytics applied to a large text corpus
  * generally attributed to Franco Moretti (2003)

* Terms originated in literary studies 

---
# Text Files
* [Finding and preparing text files](https://voyanttools.github.io/hermeneutica/finding-preparing-text.htm)

---
# Text Matching
* What we do when we use the find command
* Exact matching: matches a single string
* Pattern matching: can match a set of strings
---
# Regular Expression (regex)
* sequence of characters that specify a match pattern
* each character in the regex is either a literal character or a metacharacter
  * literal character: exact match
  * metacharacter: a character with special meeting
---
# Regex Metacharacters
*  vertical bar for or: `gray|grey` matches "gray" or "grey"
*  parentheses used for scope: `gr(a|e)y` matches "gray" or "grey"
*  `.` wildcard matches any character: `a.c` matches "abc", "a1c", etc
*  quatification:
    *  `?` for 0 or 1: `colou?r` matches "color" and "colour"
    *  `*` for 0 or more: `ab*c` matches "ac", "abc", "abbc", "abbbc", etc
    *  `+` for 1 or more: `ab+c` matches "abc", "abbc", "abbbc", etc
---
# Regex Examples
* `wom[ae]n`: "woman" or women"
* `prince.*`: all strings starting with prince
* `(love|hate|whatever)`: matches "love", "hate", or "whatever"
* `s[ck]eptic. *`: matches different spellings and endings of sceptic
--- 
# Tokenization
* Process of breaking a text into words.
* `Columbia University is located in New York, NY.`
* 
* Part of parsing the text
---
# Parts of Speech Tagging
---
# Named Entity Recogniton (NRE)
* Identifying persons, organizations, locations, times, etc in unstructured text.
* `Columbia University is located in New York, NY.`
* `Columbia University` organization
* `New York, NY` place
* Ongoing History Lab research: Using NRE  