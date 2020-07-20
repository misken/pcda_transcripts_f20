The pcda computing appliance
============================

Now that we've gotten an overview of data analytics and the
coursewebs, let's dive in and start learning to use the pcda virtual
machine.

pcda - the big picture
----------------------

The big blue rounded rectangle represents your computer, which might
be running Windows, Mac OS, or Linux. I'm assuming most of you are
running Windows and a handful use Macs.

On your computer you've got numerous programs installed, including
things like MS Office, Notepad and browsers such Firefox or Chrome.

FYI, NEVER use MS Edge as your browswer for accessing Moodle. 

In addition, you should have already downloaded and installed VirtualBox, a free
package for creating and managing virtual machines. 

In addition to programs, you've got many documents stored on your
computer - spreadsheets, presentations, text files, images, and all
kinds of other files. 

In addition, each virtual machine you create is actually comprised of
a few files - a giant disk image file and smaller logs and configuration
files. By now you should have already downloaded the pcda VM
archive file I made available on the course website and gone through
the process for importing it and getting the pcda VM running on your
computer. 

This smaller orange rectangle represents the pcda VM. No matter what
operating system you computer (the "host") is running, the pcda VM (the "guest")
is running Lubuntu Linux. There are numerous programs already installed and
you'll be downloading and creating many files such as R Markdown
documents, Jupyter notebooks, Python scripts, text files and many
other file types.

Lubuntu Linux and New to Linux
-------------------------------

Lubuntu is a very lightweight version of Ubuntu Linux. Ubuntu is 
probably the most well known and mainstream of all Linux distributions.
I've been running Linux for over ten years and use it for all of
my research, personal computing, and a good bit of my teaching. The
only real reason I also have a Windows based computer is to use
Excel to teach my spreadsheet based Business Analytics course - MIS
4460/5460.



Why learn to use Linux?
-----------------------

* Linux is widely used in the data science and analytics world

Next week we'll do a whole session on the bash shell.

* Linux shell FAR superior to Windows command line application
* Powerful shell scripting language
* Tab completion - we'll see this shortly
* Command line is often way more efficient than GUI

* Linux is free and open source
* Sets you apart from other business analysts who only know Windows and Microsoft applications

Linux is based on the Unix operating system. By the way,
the Mac OS is also based on Unix and is one of the reasons that
Macs are widely used in the data science world.

Why R and Python?
-----------------

    Both R and Python are widely used in the data science and business analytics worlds
    A quote from Enterprise Data Analysis and Visualization: An Interview Study on the growing need for technically adept analysts: When discussing recruitment, one Chief Scientist said “analysts that can’t program are disenfranchised here”
    Both support a combination of interactive use via tools like R Studio and Ipython/Jupyter along with programmatic use via text scripting
    Huge communities and ecosystems supporting R and Python for analytics work
    Both facilitate reproducible analysis - this is a big deal. Often the work we 
    do using tools like Excel are not reproducible. Unless analysts carefully document
    all of the various data manipulations they do, it can be extremely difficult to
    know exactly how the state of a data table was reached. Even if you document
    things closely, unless you automate the steps with VBA, the analysis is not
    easily reproducible. 
    Some things that are simply hideously difficult to do in tools like Excel or a database, are simple in R and/or Python
    
    These are blog posts I made several years ago
        Group By or Pivoting type analysis for operations such as percentiles
        Small multiples and other complex graphing/charting/plotting
        Documenting and reproducing complex series of data cleaning and transformations


Peek at R and Python
--------------------

Let's first start up the pcda VM. 

Start VirtualBox. Any virtual machines you have will appear in the
left sidebar. Here's our pcda-2004-f20 VM we'll be using. The "2004"
stands for Lubuntu v20.04. 

TODO: Make the recording and try auto transcript

Main menu

File Manager

Browser

Redownload the Downloads file

