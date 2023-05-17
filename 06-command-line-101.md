---
marp: true
theme: gaia
class:
  - invert
paginate: true
---
<!-- _class: lead -->
# Command line 101
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
# What is bash?
1. command-line shell
2. command language
3. Originally writen for Unix but now available on Windows/Mac/Linux 
---
# What is a shell?
A computer program that provides an interface between the user and the operating system
![height:384px width:288px](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRgL8vVGby133vx9tQBjKyZ24VdkDrnlNdWRdwRg6EBjCYHzaa5ckhI7up6YthQAal7Yag&usqp=CAU)

---
# What is a command-line shell?
A shell where the user inputs commands via keyboard and receives text output
![height:384px width:288px](https://upload.wikimedia.org/wikipedia/commons/8/84/Bash_demo.png)
---
# What is a command language
A programming langaguage for automating command line tasks

----
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
2. To list the files this directory, type `ls`
3. To see more details, type `ls -l`
4. To include hidden files, type `ls -la`
5. To see other command options, type `man ls`
---
# Creating a directory
---
# Downloading a file from the internet
---
# Installing software 
---
# Xpdf tools
---
# Using pdfinfo 
---
# Using pdftotext
---
# Using man
