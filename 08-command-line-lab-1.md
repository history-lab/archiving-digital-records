---
marp: true
theme: gaia
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
1. Click on `08-command-line-lab-1.md`
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
# Viewing files
* `cat README.md`
* `less 08-command-line-lab-1.md`
    * use less for bigger files
    * navigation options: <return>, <space>, b, h
    * use `man less` if you forget
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
# Exercises
For each exercise, provide a single command that produces the stated results: 
1. List all the files in the `archiving-digital-records` directory and its subdirectories.
2. Repeat (1) but include hidden files and directories.
3. List all the markdown files in `archiving-digital-records` beginning with 0.
4. List all the markdown files (3) in long format ordered by their last modification.