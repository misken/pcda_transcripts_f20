Intro to data science and business analytics - transcript (9:53)
================================================================

Conway's Data Science Venn Diagram
----------------------------------

One of the first visuals that tried to capture the essence of 
data science was "Conway's Data Science Venn Diagram". It quickly
conveys the notion that data science combines computation,
statistical thinking and domain specific expertise.

There have been numerous variants proposed and I've linked to a 
short article in KD Nuggets (a longtime source of information about
the growing field of data science - KD stands for "knowledge discovery".)
Scroll through and check out some of the other Venn Diagrams and by
the end, you will definitely get the gist that data science combines
ideas and techniques from a number of different disciplines. 

My version looks like this - I wanted to explicitly add a bubble
on the art and craft of modeling. This is an extremely important 
skill and pushes back against the idea of simply throwing a bunch
of data into some statistical learning algorithm and calling
that "data science".

Historical perspective
----------------------

For a historical perspective, check out the Analytics Timeline I
created and posted in Moodle. I've included a wide range of events
that have played an important role in getting to where we are today.
Again, you'll notice how multi-disciplinary the evolution of
data science has been.


Flavors of analytics
--------------------

You'll see a number of adjectives put in front of the word "analytics"
and I'd like to give three important examples.


### Descriptive analytics

Describes what was using retrospective data and uses things like
exploratory data analysis, statistics and data visualization.

Anscombe's Quartet is a famous example showing scatter plots of four
datasets that have identical means, standard deviations, 
correlation coefficients and even fitted linear regression line. It shows how such summary stats
or very simple models can fail
to tell the whole story of what is going on in a dataset. It also
shows the power of data visualization.

This next example is a set of statistics for one of the datasets we'll
be exploring in this course. It also shows an example of the Python data
analysis package, pandas, which we'll be using.

And finally, a histogram produced with matplotlib, the venerable Python based
plotting library. Many of the new Python plotting libraries use
matplotlib under the hood.



### Predictive analytics


Predictive analytics are focused on building models that take inputs
and make predictions for outputs of interest. These models are often
some blend of:

* statistics - such as a linear regression model (By the way, this plot was done with the R
package ggplot2 which we'll be using extensively)
* machine learning - such as a neural network
* simulation - such as the Monte-Carlo models we build with @Risk in my spreadsheet modeling class
* mathetical models - such as simple functions fit to data

### Prescriptive analytics


These models prescribe or suggest what might be "best" and include
various optimization techniques such as:

* mathematical programs
* heuristics for complex solution spaces
* nature based metaphors such as genetic algorithms
* heuristics for giant combinatorial problems such as optimal routing

Beyond tabular data
--------------------

While we are all familiar with well structured tabular data,
there are numerous other ways data might be structured and
accessed such as:

* free text, networks, images
* JSON files
* use web APIs

Data, data, more data
----------------------

A proliferation of applications are generating tremendous amounts
of data. Moving this data around and extracting info from this data is a challenge.

The crux of data science
------------------------

There's really nothing magical about analytics or data science. The process
is often the well worn path from idea to communicating results shown
in this diagram from the famous cs109 class at Harvard. The presence of
arrows in both directions underscores the iterative and non-linear of
real analysis projects.

CS109 Key Facets
-----------------

We need skills in:

* data wrangling
* data storage and management
* exploratory data analysis
* modeling
* communicating results

The more adept you are at each of these, the more successful analytics
professional you will be. We will focus on all of these key facets
throughout this course.

Data Science Workflow per RStudio
----------------------------------

Here's another picture of a typical data science workflow done
by the folks at R Studio. We'll be learning things in R related
to every stage in this diagram.

Closing thoughts
----------------

Now that we've gotten a brief overview of data analytics (notice how
I just shmushed the terms together - names aren't that important), let's
take a look at the syllabus and course websites for our pcda course.



