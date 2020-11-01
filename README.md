# Command Line Basics

## Prerequisites
---
* If you are on a linux or mac system you should be good to go!
* If you are on windows you have a couple options:
	- [WSL (Windows Subsystem for Linux)](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
	- [Git Bash](https://appuals.com/what-is-git-bash/)

## Getting to know the Shell
---
When you first open up your terminal, you will be greeted by some text and a blinking cursor. In my case it looks like this:

	nabil@pop-os[~]%

The first part is simply the name of my machine, and yours will very likely be different. The little `~` means that I am in my home directory. We will get into this a little later. Finally the `%` is an indicator as to where to start typing. The terminal is designed to be used purely with the keyboard, so try not to use your mouse, as it may not work on other systems. 

### The File System

Every location within your computer has a specific folder where its contents live. Similarly to how you might organize your documents, the computer organizes all of its core programs, and other files it needs to run in a similar way. Each one of these files are known as a **directory**. You are easily able to go into each of these folders, access contents, and even edit files all within the terminal. We can run the `tree` command to view a graphical representation of our file structure. For example, running tree on this folder gives us:

	|__ README.md
	|__ test_files
	    |__ test.txt

### The **Man** Command

If you're going to remember any other command from this tutorial, `man` is it. Man is short for manual, and does what the name implies it will. Give it the command which you want to see the manual for and it will return the man page for that specific command. You can see exactly how to use it, any optional flags, and much more! Try running `man cd`.

### Basic Movement

We've established that we can somehow navigate through our file system, but exactly how do we do that? There aren't any folders to click on to go into! Not surprisingly, there are a set of commands to do exactly this. The first command we will go over is the `cd` command.

`cd` is short for change directory. Knowing each of the folders within our computer is a directory, we can simply give the name of the directory we would like to go to. There is a catch however, we can only navigate to directories that are in the same directory we are in. For example lets say we are in our home directory (typically denoted by `~`). We can `cd` into any of the other folders in our home directory, such as `Documents`. What if we wanted to go into a folder in `Documents`? We can simply put the name of the folder we want to navigate 




