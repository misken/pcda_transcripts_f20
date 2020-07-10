# File management

Here's a typical file structure on a Linux based machine.

The house represents the "home" directory for the user lucy.

Just like in Windows, there are a number of subfolders, such
as Documents and Downloads. Within the folders are files. 

Back upstream from the lucy home directory we see the
system "root" directory reprented by a single forward
slash. Within the root are a number of subfolders with
the Lucy directory being one that is inside the Users
folder. It doesn't look a whole lot different than what
you are used to seeing in Windows.

## Let's learn a few basic shell commands.

The bash shell usually has a command prompt that ends with the $ (do NOT type the $)
	$ whoami - try it
	$ pwd - present working directory
	$ ls - list files and folders
Many commands have options or flags that start with the -
	$ ls -l
	$ ls -l -a
You can often combine the flags
	$ ls -la
What do you think the -r flag does?
	$ ls -l -r
Most commands take arguments
	$ ls -l *.csv
*
	
## Absolute vs relative paths

An absolute path such as             /home/pcda/Documents

Starts at root, i.e. at /
Specifies series of folders separated by /'s
It's important to note that Folders and filenames are CASE SENSITIVE

A relative path such as            Documents/sandbox

Starts in present working directory (pwd gives it)
Specifies series of folders separated by /'s

There are a numer of special directory symbols

“dot” or . Is the present working directory
“dot dot” or .. is the parent of the present working directory
~ is the home directory
/ is the root directory

## Navigating the directory tree

The cd directory command is how we move between directories (folders)
You can use absolute or relative paths

Use pwd after trying each of the following

Use the ~ to go directly to the home directory
	$ cd ~
From the home directory go to the Documents subdirectory. Notice that
since there is no sympol before the subdirectory name, we are using
a relative path from the home directory.
	$ cd Documents
Let's go back home
	$ cd ~
This is another way to navigate to the Documents subfolder. The dot
is the current directory and then we use forward slashes between
subdirectory names.
	$ cd ./Documents
Where does the following command take us to? Remember, the double dot
means one directory "above" the current directory. We relative to
our current spot in Documents, where does .. take us and from there we
go into the Downloads subdirectory.
	$ cd ../Downloads
Typing long paths can get get tedious.
	$ cd ~/Documents/Downloads_shell/data

Tired of typing yet?

## Tab completion

Just like as we'll see in R Studio, the shell has tab completion
Can save TONS of typing and mistyping
Shell also uses arrow keys to cycle back and forward through previously entered commands
cd ~ back into your home directory and then...
cd Doc<TAB>/Dow<TAB>
Pretty awesome, eh?
Home and End keys are also useful when editing previously used commands

## Filename wildcards

I'm sure many of you are familiar with basic file selection wildcards

* matches any number of any characters EXCEPT the /
? matches a single character
change directories to get into the /Downloads_shell directory

List all the files ending in '.txt'
	$ ls *.txt

List all the files in the rivertemp subfolder ending in '.csv'
	$ ls data/rivertemp/*.csv

List all the files in the rivertemp subfolder that start with
'510F_' and end in '.csv'
	$ ls data/rivertemp/510F_*.csv

List all the files in the rivertemp subfolder that start with
'510' followed by a single character and end in '_2012.csv'
	$ ls data/rivertemp/510?_2012.csv


NOTE: These wildcards have different meanings in regex world

## More file management commands

To make a directory use:
mkdir

Removing files and directories
rmdir, rm
USE WITH CAUTION

Copying and moving files
cp - copies files
mv - moves (or rename) files 
See http://swcarpentry.github.io/shell-novice/03-create/
for a very good tutorial on all of these commands and more
basic file management tips.

It's easy to find info on Linux commands through basic 
web searches.

Example: Linux cp command

## File copying exercise

Now we'll get a little practice with Linux file management commands.
Try to complete the following tasks. The answers are at the end of
the slide presentation.

 Change directories into Downloads_shell
 Change directories into the data subdirectory
 Make a new directory called 510F within the data directory
 Copy all the csv files from within data/rivertemp that are from the 510F site into this new 510F directory
 Change directories into 510F and then do an ls to make sure everything worked
 Now delete all the files in the 510F directory
 Finally, remove the 510F directory
 
## Text file snooping with more or less

Text files are a “common currency” of computing
A common issue is having a HUGE text file that you 
don't really want to try to open with a text editor
but would like to see the first few lines
perfect job for more or less (because “less is not more”)
Change directories into the Downloads_shell/data/rivertemp subfolder (of course you don't need to type all that)
list the .csv files
pick one and try the more command on it

"man" pages (short for "manual" pages) are another way to get help
regarding command usage

To see the manual page for more (q to quit)
	$ man more 
To see the manual page for less
	$ man less 

less is more powerful than more
less doesn’t read entire file into memory
less allows forward and backward navigation through file
