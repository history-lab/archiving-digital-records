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
# Creating a codespace
1. Point your browser at the [codespaces dashboard](https://github.com/codespaces)
2. In *Explore quick start templates* press the "Use this template" button for the *blank* template
3. A new browser tab will open with a new, blank codespace 
---
# Renaming and saving your codespace
1. Return to the codespaces dashboard tab
2. In *Owned by* press the menu button `...` for the newly created codespace and select "Rename"
3. Choose a more suitable name (e.g. Archiving-Digital-Records)
4. Go back to the menu and select "Keep Codespace"
---
# Accessing the command line (terminal)
1. Return to the codespace tab
2. In the terminal window type `ps`
    * show the processes currently running in the terminal
---
# Cloning the slides repo
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
* repo (aka repository): collection of files under git control
* repo contains the latest version of files, but also all previous versons
* `clone` a git command that you can think of as a copy command + tracking info


---
# Navigating the filesystem using Explorer & Editor
1. Click on `06-command-line-101.md`
2. Review the "code" for the slide
3. Click on `Open Preview for the Slide` - RHS of editor window
4. Control (right) click on a filename to see actions
---
# pwd & ls commands
1. Note that terminal's current working directory is part of the command line prompt
    * use can also use the `pwd` command to see it
2. List the files in a directory: `ls`
3. See more details: `ls -l`
4. Include hidden files: `ls -la`
---
# Commands in general
* commands = programs
* built-in and user defined
* Unix (and Linux) origins
* flags and arguments
---
# Command flag
* example: `-l` in `ls -l` 
* modify default command behavior
* begins with a `-`
* sometimes called option
   * esp. if it accepts arguments
---
# Command argument
* exammple: `README.md` in `ls -l README.md` 
* modifies default command behavior
* sometimes called option
   * esp. if it accepts arguments
---
# Learning more about a command
* man command (e.g. `man ls`)
* Google
* chatGPT and variants
---
# Follow [xkcd 627](https://xkcd.com/627/)'s flowchart
![height:512px width:512px](https://imgs.xkcd.com/comics/tech_support_cheat_sheet.png)

---
# Changing directories
* pwd: present (i.e., current) working directory
*  `cd archiving-digital-records` change pwd to named directory
*  `cd -` change pwd to previous directory

---
# Viewing files
* `cat README.md`
* `less 06-command-line-101.md`
    * Use less for bigger files
    * Navigation options: <return>, <space>, b, h
    * Use `man less` if you forget
---
# Creating a directory
* Create a directory for the PDFs we are going to experiment on
* `mkdir pdfs`
* `cd pdfs`
---
# Downloading a file from the internet
* The curl command lets you fetch a given URL or file

* "client for URLs"

*  To download the Mueller Report PDF from the DOJ website, type this on command line and press return:

`curl -o mueller.pdf https://www.justice.gov/archives/sco/file/1373816/download`

---
# Installing software 
Note: the exact commands for installing software differs somewhat across OSs 

1. Type on the command line and press return:
`sudo apt-get update`
2. `sudo apt-get install poppler-utils`
3. Answer `Y` to question:
```
After this operation, 17.2 MB of additional disk space will be used.
Do you want to continue? [Y/n]
```
---
# Understanding software installs `sudo`
* stands for "superuser do"
* runs the commands that follow as superuser 
* superuser is a privilaged administrative account 
* software installs typically require a privilaged account
---
# Understanding software installs `apt-get`
* software installer
* accepts subcommands such as:
     * `update`  update the package lists for available software packages 
     * `install` install or upgrade packages
---
# What is `poppler-utils`?
* name of the software packaged we are installing 
* a set of command-line programs for processing PDFs
* we will intially focus on two:
    * `pdfinfo`
    * `pdftotext` 
---
# `pdfinfo` 
* Shows a PDF's metadata
* From your `pdfs` subdirectory enter the following at the command line and press return:
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
* From your pdfs subdirectory enter the following at the command line and press return:
`pdftotext mueller.pdf`
* Try `ls`

---
# Exercises
1. Create a new directory at the same directory level as `pdfs` called `txt`. Move `mueller.txt` to your newly created `txt` subdirectory.

2. How can we ensure output generated from `pdftotext` goes to the `txt` directory going forward?

3. Test out some of the flags on both `pdfinfo` and `pdftotext`. Try to find something worth discussing.

4. Load another PDF into codespace - something that interests you. Run both `pdfinfo` and `pdftotext`. How's the text quality? 