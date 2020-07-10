# The CELLDEX project
A few years ago I got involved in an ecology research study which
was looking at decomposition rates of organic material in streams
throughout the world. 

As part of that study, small temperature sensors were put in hundreds
of streams by ecologists on all seven continents. After a few months of
collecting data, the ecologists downloaded the temperature readings
from the sensors to their PCs and then sent the data files in to
us for processing and analysis. 

This presented numerous challenges and I like to use this example to
show the role of many of the tools and concepts we will learn in this 
class. It highlights the value of knowing how to use tools like
the bash shell to aid in automated file management and file processing.

The main processing stops looked like this:

* csv or xls or xlsx files were emailed to us. Let's take a look at one
of these files. Note that in this file there is a header and then
a bunch of data lines.
* I created a Python based tool to help semi-automate the cleaning
and standardization of these data file. 
* Standardized data was stored in a SQLite database
* R was used to analyze and visualize the cleaned up and standardized
data.

There were literally thousands of input and output files to manage.

We used standardized filenames to facilitate automated file management
in the bash shell. Notice that the filenames are composed of distinct
parts which each have meaning and notice that we are careful about
letter case and using underscores instead of spaces in the filenames.
NEVER use spaces in filenames as they make automated processing more
difficult.

What were some of the challenges with cleaning and standardizing
all these input data files?

Different number of records due to
Sampling frequency (hourly, half-hourly, quarter-houry)
Duration of sampling
header section of variable size and presence
logger brand
Number of fields and field delimiter (comma, semicolon, tab)
Numerous date and time formats
Temperature scale – F vs C
International number formats (comma instead of decimal point)
Different text encodings (no such thing as truly “plain text”)
Determining when sensors were “out of water”
Excel files vs csv files
... and we just need to manage all those input and output files efficiently

Developing bash skills can help you with all kinds of text file processing
and file managent challenges that arise frequently in analytics
related projects. Doing these things manually with a GUI file
manager is simply not efficient nor reproducible.
