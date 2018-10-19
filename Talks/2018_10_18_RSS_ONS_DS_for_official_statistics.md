Data Science for official statistics: the story so far
======================================================

First talk: Statistics on jobs, business and people - where data science is adding value
----------------------------------------------------------------------------------------

**by Karen Gask - Office for National Statistics Big Data team**

Karen gave examples of where they are using Data Science (DS) at ONS.

She briefly presented the ['better statistics, better
decisions'](https://gss.civilservice.gov.uk/wp-content/uploads/2012/12/Better-Statistics-Better-Decisions.pdf)
note.

Large parts of their code are published [on the Data Science Campus
GitHub account](https://github.com/datasciencecampus).

Then she gave some examples of applications of DS methods:

***Matching addresses***: For the census it's really critical to have a
complete list of addresses, but this can be complicated. The challenge
is to take an input address string, which comes from unstructured, messy
and incomplete data and convert it into a clean list of addresses.

First, they tokenise the raw inputted strings. They used 'structured
learning' and an algorithm called 'conditional random fields' which
calculates the likely sequence of words. They have a really good
accuracy overall.

Then they have to match the tokenised strings with the original data.
They do so with 'elastic search'. They compute a 'confidence score'.
This service is available to everyone else in the government, through
API and a webpage.

They are now trying to create a 'time machine' so people can find
addresses from the past.

***Online job vacancies***: Business surveys gathering data for
vacancies can be limited. They collect data from job portals. They try
to match the survey data with the data scrapped or accessed from the job
portals. Some conclusions: whenever they can agree access to data from
job portals is much easier than doing web scrapping. Their OJV can not
replace the job vacancy survey. The next phase will look at using the
OJV for official stats.

They seem to have a [published Shiny
App](https://datasciencecampus.shinyapps.io/employmentProspects/).

***Automated survey coding***: In the Crime Survey for England and Wales
they ask respondents whether they have been a victim of crime. There is
free text and closed questions. they use 'Natural Language Processing'
(NLP) and machine learning to predict the code. If the confidence of the
model for a given string is &gt; 97%, they use the predicted code
automatically.

***Using Zoopla to find caravan homes***: They used the Zoopla API to
obtain data. They used NLP and ML on the property description to predict
which properties were caravan homes.

Second talk: Data is coming: The Data Science Campus and its projects
---------------------------------------------------------------------

**by Jasmine Latham, Data Science Campus**

She gave more examples of DS applications at ONS:

***Urban forest***: Natural capital statistics from images. Uses street
view to analyse trees in urban areas. There is currently very poor data
at local level. They use street level image data to spot where there are
urban forests. This allows them to map urban forests across the UK and
analyse the availability of these areas in different places. Part of the
code to visualise the results seems to be
[here](https://github.com/datasciencecampus/vegetation-deckgl)

***Internet traffic indicators***: They analyse (internet) data
consumption and try to relate it to socio-economic
indicators/activities.

***Identifying emerging technology trends through patent
applications***: There are 90 million global patent applications. Can we
analyse them using text analytics and forecast new
technologies/innovations (if possible, by location)? Code seems to be
[here](https://github.com/datasciencecampus/patent_app_detect)

***Understanding UK port operation and freight ship behaviour using big
data***: LAs want to do future planning on harbor activity/demand. How
can we plan for potential future events? Ships are sending encoded
messages to each other every three seconds. They modeled the ship
behaviour to predict delay windows. How likely is a ship to be delayed?

***Synthetic data for secure sharing***: Some microdata is very
sensitive. Can we create a dataset that represents the original data but
it's not real? They use deep learning models (WGAN) for this. Next
steps: produce synthetic data for LFS!

***Improving ONS search function with Natural Language Processing***:
Make the search engine better. They use LDA (topic modelling) and
Word2Vec. They compare the ONS publications text with the search query.

***Access to Services. A Multi-Modal Transport System***: Used to
identify deprived areas to target public services. They use Open Trip
Planner (an open source "Google Maps" type of app). They can compute the
time it takes to reach critical infrastructure/areas from any point. She
shows dark areas representing areas in Whales that do not have access to
a hypothetical important area/point.

![](https://github.com/JosepER/talks_and_presentations/blob/master/raw_rmd/images/181019_1.jpg)

Third talk: Data science for official statistics: the story so far
------------------------------------------------------------------

**by Suzy Moat from Data Science Lab, Warwick Business School**

Suzy argued that now we are starting to try to use data that people are
leaving behind instead of collecting the data through surveys or similar
methods. We are interested in quicker, cheaper, novel measurements. The
question is: are we going to replace original approaches or just enhance
these? She said that (short term) we are not so likely to replace
traditional sources, but to improve the estimates these produced. New
sources of data might have biases and many new methods might be
black-box algorithms. She said we should test how accurate they are
instead of trying to understand the exact nature of the source and the
algorithm.
