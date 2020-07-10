# Combine shell commands

Now that you know some shell basics, let's see how you can use multiple shell commands together to do more complex things.

This is really a lead in to shell scripting which is really just another example of programming.

“small pieces, loosely joined” is the Unix way.

Get a terminal window open and get to the following directory: (trick - use GUI File Manager to get to path and press F4 or use tab completion)

Downloads_shell/data/rivertemp_raw

## Challenge - Find csv file with fewest number of lines it it

We'll use several different Linux commands chained together with pipes and redirects
wc - counts lines, words, characters in files
sort - sorts things
head - gets a specified number of lines from top of file 

Let's start by learning how to count words, lines and
characters in files

Let's use wc on all the csv files
	$ wc *.csv
*
Let's experiment with some of the command flags
	$ wc -l *.csv (*try -c and -w flags as well)
	
Let's redirect the output to a file called lengths using the > (use cat to see it)
	$ wc -l *.csv > lengths
*
	$ cat lengths
	$ sort lengths

Hmmm, what happened with this last command? We wanted a
numeric sort, but got an "alphabetic" sort. Doesn't it
seem likely that there's a flag to specify you want things
sorted numerically? And if there was such a flag, what
letter do you think it might be?

	$ sort -n lengths
	$ sort -n lengths > sorted_lengths
	
Now we'll use the head command to see part of the file
starting at the top

	$ head -1 sorted_lengths
	$ head -5 sorted_lengths

## Input, output, redirection and pipes

A running program, or process, has standard input channels and output channels
	stdin and stdout
	keyboard and screen by default
	
> redirects output to some other destination

>> like > but appends if destination already exists

< sets input channel to something other than keyboard

| (the “pipe”) takes output from one program and sends it through the input channel of another 

Now, we can combine a bunch of things we just learned to
solve our problem of finding the csv file with the 
fewest number of lines.

Let's do the following one piece at a time 

$ wc -l *.csv | sort -n | head -1

*
Good graphical view of this at http://swcarpentry.github.io/shell-novice/04-pipefilter/

NOW TRY THIS: Find the 5 files containing the greatest number of characters

Make sure the results are sorted in descending order
Couple different ways to do this
Need to deal with that Total line

You can find the answer at the end of the slide presentation.


