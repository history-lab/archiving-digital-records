---
marp: true
theme: gaia
class:
  - invert
paginate: true
---
<!-- _class: lead -->
# Command line lab
---
# Cloning the workshop repo
Type the following on the command line:

 `git clone https://github.com/history-lab/archiving-digital-records.git`

And you'll see output like this:
```
Cloning into 'archiving-digital-records'
remote: Enumerating objects: 116, done.
.
.
Resolving deltas: 100% (60/60), done.
```
---
# Understanding what we just did
* `git` tracks collections of files, usually project related
* repo (aka repository): a collection of files under git control
* repo contains the latest version of files, but also all previous versions
* `clone` a git command that you can think of as "copy files + tracking info"
---
### Navigating the filesystem using Explorer & Editor
1. Click on `07-command-line-lab.md`
2. Review the "code" for the slide
3. Click on `Open Preview for the Slide` - RHS of the editor window
4. Control (right) click on a filename to see actions
---
### Navigating the filesystem from the command line
1. The terminal's current working directory is part of the command line prompt
    * use can also use the `pwd` command to see it
2. List the files in a directory: `ls`
3. See more details: `ls -l`
4. Include hidden files: `ls -la`
---
# Changing directories
* `pwd`: present (i.e., current) working directory
*  `cd archiving-digital-records` 
*  `cd -` change pwd to the previous directory
*  time saver: use <tab> key to autocomplete file names 
---
# Commands in general
* Commands = Programs
* Built-in and user-defined
* Unix (and Linux) origins
* Flags and arguments
    * CLI (command line interface)
    * far simpler than building a GUI
    * largely eliminates cross-platform concerns
---
# Command flag
* Example: `-l` in `ls -l` 
* Modify default command behavior
* Enable/disable a particular feature
* Begins with a `-`
* Sometimes called an option
   * esp. if it accepts arguments
---
# Command argument
* Example: `README.md` in `ls -l README.md` 
* Modifies default command behavior
* Specifies input file(s) or data

---
# Learning more about a command
* On the command line -
    * `man ls` brings up the manual page
    * `which ls` which program is running 
* On the web -
    * Google, StackOverflow
    * chatGPT and variants
---
# [xkcd 627](https://xkcd.com/627/)'s flowchart
![height:512px width:512px](https://imgs.xkcd.com/comics/tech_support_cheat_sheet.png)

---
# Viewing files
* `cat README.md`
* `less 07-command-line-lab.md`
    * use less for bigger files
    * navigation options: <return>, <space>, b, h
    * use `man less` if you forget
---
# Creating a directory
* Create a directory for the PDFs we are going to experiment on
* `mkdir pdfs`
* `cd pdfs`
---
# Downloading a file from the internet
* The curl command lets you fetch a given URL or file

* "client for URLs"

*  To download the Mueller Report PDF from the DOJ website, type this on the command line and press return:

`curl -o mueller.pdf https://www.justice.gov/archives/sco/file/1373816/download`

---
# Installing software 
Note: the exact commands for installing software differ somewhat across OSs 

1. Type on the command line and press return:
`sudo apt-get update`
2. `sudo apt-get install poppler-utils`
3. Answer `Y` to the question:
```
After this operation, 17.2 MB of additional disk space will be used.
Do you want to continue? [Y/n]
```
---
# Understanding software installs `sudo`
* Stands for "superuser do"
* Runs the commands that follow as superuser 
* Superuser is a privileged administrative account 
* Software installs typically require a privileged account
---
# Understanding software installs `apt-get`
* Software installer
* Accepts subcommands such as:
     * `update`  update the package lists for available software packages 
     * `install` install or upgrade packages
---
# What is `poppler-utils`?
* Name of the software package we are installing 
* A set of command-line programs for processing PDFs
* We will initially focus on two:
    * `pdfinfo`
    * `pdftotext` 
---
# `pdfinfo` 
* Shows a PDF's metadata
* From your `pdfs` subdirectory, enter the following at the command line and press return:
`pdfinfo mueller.pdf`
---
# `pdfinfo` output:
```
Title:          Report on the Investigation into Russian Interference in the 2016 Presidential Election
Subject:        Investigation into Russian Interference in the 2016 Presidential Election
Keywords:       2016 Presidential Election; Special Counsel; U.S. Department of Justice; Robert S. Mueller;
Author:         Special Counsel’s Office
Creator:        Adobe Acrobat Pro DC 19.12.20036
Producer:       Adobe Acrobat Pro DC 19.12.20036
CreationDate:   Thu Aug 29 17:13:28 2019 UTC
ModDate:        Tue Sep  3 17:22:42 2019 UTC
Tagged:         yes
UserProperties: no
Suspects:       no
Form:           AcroForm
JavaScript:     no
Pages:          448
Encrypted:      no
Page size:      612 x 792 pts (letter)
Page rot:       0
File size:      11446227 bytes
Optimized:      no
PDF version:    1.7
```


---
# `pdftotext`
* Extracts text from a PDF
* From your pdfs subdirectory, enter the following at the command line and press return:
`pdftotext mueller.pdf`
* Try `ls`

---
# Exercises
1. Create a new directory at the same directory level as `pdfs` called `txt`. Move `mueller.txt` to your newly created `txt` subdirectory.

2. How can we ensure output generated from `pdftotext` goes to the `txt` directory in the future?

3. Test some flags on both `pdfinfo` and `pdftotext`. Find something worth discussing.

4. Load another PDF into codespace - something that interests you. Run both `pdfinfo` and `pdftotext`. How's the text quality? 