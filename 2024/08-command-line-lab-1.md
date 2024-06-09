---
marp: true
theme: default
class:
  - invert
paginate: true
---
<!-- _class: lead -->
# Command line lab 1
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
1. Click on `08-command-line-lab-1.md` in the `2024` folder
2. Review the "code" for the slide
3. Click on `Open Preview to the Side` - upper RHS of the editor window
4. Control (right) click on a filename to see actions
---
### Navigating the filesystem from the command line
1. The terminal's current working directory is part of the command line prompt
    * use can also use the `pwd` command to see it
2. List the files in a directory: `ls`
3. See more details: `ls -l`
---
# Changing directories
* `pwd`: present (i.e., current) working directory
*  `cd archiving-digital-records/2024` 
*  `cd -` change pwd to the previous directory
*  time saver: use <tab> key to autocomplete file names 
---
# Viewing files
* `cat 08-command-line-lab-1.md`
* `less 08-command-line-lab-1.md`
    * use less for bigger files
    * navigation options: <return>, <space>, b, h
---
# Commands in general
* Commands = Programs
* Built-in and user-defined
* Unix (and Linux) origins
* Flags and arguments
    * CLI (command line interface)
---
# Command flag
* Example: `-l` in `ls -l` 
* Modify default command behavior
* Enable/disable a particular feature
* Begins with a `-`
* Sometimes called an option
---
# Command argument
* Example: `README.md` in `ls -l README.md` 
* Modifies default command behavior
* Specifies input file(s) or data
---
# Learning more about a command
1. GitHub Copilot
   * Free for verified students and teachers, see   https://education.github.com
   * Alternatives:
        * Google Codeium
        * Amazon CodeWhisperer
2. LLM chat client or web search
3. From the command line:
    * `man ls` brings up the manual page 
---
# [xkcd 627](https://xkcd.com/627/)'s flowchart needs updating!
![height:512px width:512px](https://imgs.xkcd.com/comics/tech_support_cheat_sheet.png)

---
# Exercises
For each exercise, provide a single command that produces the stated results: 
1. List all the files in the `archiving-digital-records` directory and its subdirectories.
2. List all the markdown files in `archiving-digital-records/2024` beginning with the number 0.
3. Repeat (3) but in long format ordered by their last modification.
