# More useful bash commands

## Understanding the ls -l command

When we run ls with the -l flag we get a bunch of
information about each file and folder. The 
first character that starts each line conveys whether
or not it's a file or a directory.

Then there are three sets of three characters which
specify the permissions available to the User
of the file, Groups of users, and Other users.

Permissions are read, write and execute. If you
are interested in learning more, follow the
link on the slide to learn more about permissions and
how to change permissions using the chmod command.

## nano is a simple text editor

nano usually available on most Linux installs

$ sudo nano <filename> is handy for modifying system files

In shell, navigate to  Downloads_shell/data
$ nano notes.txt

Try adding a line, change some text, and then save the file.

Notice it's not like modern text editors you might be used to.
But, it's pretty easyto figure out how to save the file and
exit. Note that the "caret" symbol usually means the CTRL key.

## Display and join files with the cat command

Navigate to data/rivertemp directory
These are actual data files from iButton temperature sensors
I created a Python program to process this data for some ecology grad students 
	$ cat 510F_2012.csv
displays file to screen
	$ cat file1 file2
combines the two files
can use > to redirect to a new file
can use wildcards to glob multiple files
	$ cat *.csv > onebigfile.csv
*
what would be problem in using cat to combine all the files that start with 510 into a single file?

## Finding things in files with the grep command

The grep command is a very powerful and useful command for
searching inside of text for other text

grep stands for Global Regular Expression Print
We'll do much more soon with regular expressions (regex)
A super powerful and useful command which you can use
to do things like:

* display lines from one or more files matching a simple text pattern or a more complex regex pattern
* count lines matching a pattern in files
* display subset of voluminous output from other Linux commands
* control its behavior with several command line options (follow link above)
use with | and >, >> to do all kinds of text magic

## Let's see grep in action

Navigate to data/rivertemp_raw directory and do an ls to see what's there

Let's say we want to get all of the lines from all the
csv files that have the words 'Mission Start' in them.
Let's explore a bit to see how we might do this.

	$ grep 'Mission Start' *.csv

*
Now let's do this just for files from 2011
	$ grep 'Mission Start' *_2011.csv

*
Finally, let's redirect the output to a new file
	$ grep 'Mission Start' *_2011.csv > missionstart_2011.log
	$ cat missionstart_2011.log

*
Let's takea closer look at one of the files. I'll pipe the
cat output through more.	
	$ cat 510F_2011.csv | more


We can use the -c flag to ount lines in file(s) 
$ grep -c 'Mission Start' *.csv

*
Now just display lines with 'Mission Start' but also include the 2 lines directly below the match
$ grep -A 2 'Mission Start' *.csv

*
How does one figure this out? Well,

* man grep
* Google 'grep lines before and after'

grep is useful for filtering output of other commands

Explore your command history with history
then just display previous commands of interest by piping the output of history into grep

Example: Find all lines in history that used wc command

you can rerun a command by entering !123 (where 123 is just an example of a command number you want to rerun)
Rerun the  wc command we did to find the 5 largest files by using !

## Retrieving web content with curl

We can use the curl command to interact with the web from
a bash shell.

Let's check out one of the data files we'll be using
later in the semester.

	$ curl "https://jaredlander.com/data/housing.csv"
	
Above is simplest case; output to screen, fixed URL

Use >  or the -o flag to send output to a file

The real magic is in URL “wildcards”
let's get some weather data from a few cities using 
https://github.com/chubin/wttr.in

Let's first check out the wttr Github site. We'll be
using Github in this class as a place to store our
version controlled files remotely.

Now, let's put this url into a browser:

http://wttr.in/Rochester+Michigan?0

Now, let's do it from the command line using curl:

	$ curl https://wttr.in/{Detroit,Vancouver}?0

## Learning more

We have barely scratched the surface in learning to use
the bash shell. I highly recommend you go through parts
1-4 in the Software Carpentry bash shell. If you want
to go further, you can learn about more advanced topics
like shell scripting.
