# Command Line Basics

## Prerequisites

* If you are on a linux or mac system you should be good to go!
* If you are on windows you have a couple options:
	- [WSL (Windows Subsystem for Linux)](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
	- [Git Bash](https://appuals.com/what-is-git-bash/)

## Getting to know the Shell

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

`cd` is short for change directory. Knowing each of the folders within our computer is a directory, we can simply give the name of the directory we would like to go to. There is a catch however, we can only navigate to directories that are in the same directory we are in. For example lets say we are in our home directory (typically denoted by `~`). We can `cd` into any of the other folders in our home directory, such as `Documents`. What if we wanted to go into a folder in `Documents`? We can simply put the name of the folder we want to navigate to after a `/`. For example, `cd Documents/School` takes us to the `School` folder within `Documments`. 

This is known as a **path**. It is essentially a literal path to a folder or a file. You can follow each `/` to see the path to any folder or file. What if we want to see our current path? We can use the `pwd` command. `pwd` stands for print working directory, and it does exactly what it says.

	$ pwd
	/home/nabil/Dev/ucsc_bash_tut

In the example above we can see that I am in the ucsc\_bash\_tut folder which is in the Dev folder which is in the nabil folder, and finally this is in the home folder. Okay now we can navigate to folders we want, but how can we see the contents of a folder. We can use the `ls` command. 

`ls` stands for list, and again, it does exactly what it implies. We can use it list all the files within a directory. For example:

	$ ls
	README.md test_files

We can see that this is what our ucsc\_bash\_tut folder contains. Now of course there are a lot of other combinations of movement commands and useful flags but these are the essentials.

Okay, so we can now go into folders and take a look at its constants, but what happens when you want to go back out of the folder. You have 2 options: you can cd back into the previous folder, *or* you can use `cd ..`. This command takes you back a folder. 

### Working with Files

Now that we know how to navigate through our file system we want to be able to work with files. How do we create files? There a plethora of command line text editors (you may have heard of `vim`, `emacs`, `nano`), however the most user friendly one is `nano`. Whichever text editor you use, look up the syntax to see specifically what you need to do. Generally it is `name of the editor` followed by `name of file you want to create`. For example `vim test.md` creates a markdown file called `test`. Once within your text editor you can write whatever you want similar to any other editor such as vscode or sublime text. 

Lets say, you've created your file, but you created it in the wrong place and you want to move it. Unsurprisingly there is the `mv` command. To use `mv` all you need to do is give the file you're moving a location to move to. For example, we want to move `test.md` from `ucsc_bash_tut` to `test_files`. We can do:
	
	$ mv test2.txt test_files
	$ cd test_files
	$ ls
	test2.txt

Another use for the `mv` command is to *rename* files. Instead of providing a path to move the file to, you can simply provide the new name that you want to use. 
	
	$ ls
	test2.txt
	$ mv test2.txt new_test2.txt
	$ ls
	new_test2.txt

Okay so we have created, edited, and renamed files, but how do we remove files? Simple, we use the `rm` command. We can provide `rm` the name of the file we want to delete and it will remove it for us. Keep in mind that by default using `rm` only lets you delete files. There is a different syntax for folders.

Let's say you want to make a new folder to put files in. Again, this is very simple within the command line. We can use the `mkdir` command. 
	
	$ ls
	new_test2.txt
	$ mkdir new_folder
	$ ls
	new_test2.txt new_folder

Another useful command might be the `cp` command. As you might have guessed, it stands for copy and works very similarly to the other commands we have covered previously. 

### Viewing Files

How can we take a look at files within the terminal? There are a couple main commands to use. Of course, you can open up whatever you want in your text editor. In addition to that we have the `head` and `tail` commands. By default `head` will print the *first* 10 lines of whatever file you want, whereas `tail` will print the *last* 10 lines of the file. These commands are very useful for taking a peak into longer files. 

Additionally we can use the `cat` command. Instead of printing a certain number of files for us to see, `cat` will print the contents of our entire file to the terminal. 

## End Notes

There is so much to using the terminal than what was covered in this short tutorial. Definitely go out there and do some research about all the things you can do in the command line, You will definitely be surprised! Some useful links:
	- [Intro to Bash Scripting](https://www.youtube.com/watch?v=v-F3YLd6oMw)

	- [Linux File Structure](https://www.youtube.com/watch?v=HbgzrKJvDRw)




