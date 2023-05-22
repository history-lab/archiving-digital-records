---
marp: true
theme: gaia
class:
  - invert
paginate: true
---
<!-- _class: lead -->
# File Types and Formats
---
# Text Files vs. Binary Files
* Broadest classification 
* Every computer file is either _Text_ or _Binary_
* exclusive OR
---
# Text File Characteristics
* Sequence of lines of characters
* Elements of sequnence separated by EOL character
* Uses a character encoding 
   *  e.g. UTF-8, UTF-16, ASCII,   Latin-1, etc
* Human readable in a text editor 
* Valid input to command-line text processing utilities  
---
# UTF-8
* UTF = Unicode Transformation Format
* Web's most commonly used character encoding
* Represents all characters from all the world's writing systems and emojiis!
   * Unicode currently represents 150K characters
   * Capable of supporting 1.1M characters
* Backwards compatible with ASCII
* Variable length 1-4 bytes
---
# Text Formats
* Plain text files (.txt)
* Source code (.c, .py, .js)
* Presentation languages (.html, .md)
* XML  (.xml, .epub, etc)
* JSON (.json)
* Flat files (.csv, .tsv)
* Log & config files
---
# Binary File Characteristics
* Any file that's not a text file
* A sequence of bytes
* Must adhere to a specific type of format
    * Format often is part of embedded metadata
---
# Binary Formats
* Images (.tiff, jpg, png, etc)
* Audio & video format (.mp3, .mp4, .mov, .wav, etc)
* Documents (.pdf, .docx, .pptx, etc)
* Archive files (.zip, .tar)
* Executables (.exe, ELF)
---
# Determining File Type 
* `file <filename>`
* examples
```

```





