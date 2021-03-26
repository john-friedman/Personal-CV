# Personal-CV

### Education
UC Berkeley 

Stats Major

Economics Major

### Classes Taken
Andy Ng ML Sequence: Course 1

### Various Jobs:
Research Assistant UCB (Fall 2019 - Present)

Summer Researcher MIT (Summer 2018, Summer 2019)

### Volunteer/unpaid work:
Covid-19 Policy Alliance (Spring 2020 - Summer 2020)

Undergraduate Research Apprenticeship Program (Fall 2017 - Fall 2019)

### Coding Languages:
Python - Significant Experience. Have written many projects in Python. Decent for performance, great for hacking together a GUI.

R - Significant Experience. Have written many projects in R. I find it's often the quickest language to hack something data sciency together in, if performance is not an issue.

Julia - Minor Experience. Julia looks awesome, it feels intuitive and can be extremely fast compared to Python. I'm actively looking for an excuse to write something big in this language.

Octave - Minor Experience. I used this for Andy Ng's ML courses. I'm not the biggest fan, but it seems nice for matrix multiplication.

Fish (><>) - I will never touch this. Ever.

### APIs:
Google Cloud Vision

Google Maps 

Dropbox

FCC

### Coding Experience


#### Created a data pipeline to detemine if observations of a civil servant in a civil servant dataset were the same based on name and some additional information. (March 25th-Present)
Languages: R

Quick example: We needed to determine whether a 'John Doe' in year 1909 who worked in the Navy and was born in Poland was the same as say 'John D' from the year 1911, who was
also born in Poland, but worked in the Treasury. 

This was complicated because the names not only were sometimes initial vs full, but also frequently had spelling errors. Additionally, the birth states also had spelling errors/
differences such as Virginia vs VA, as well as would change over time. What do I mean by change over time? I mean that someone who put their birthplace as 'Austria' in 1909, might in
1917 put their birthplace as 'Hungary'. This may have to do with the rise of nationalism in Europe, as well as the independence of countries such as Hungary. Another interesting
thing to find was that people changed their birthplace from Virginia to West Virginia during this time period. Whether this was by accident, or on purpose (West Virginia seceeded
from Virginia during the Civil War only 40 years prior) is interesting. It's important to note that during this period (1907-1917), President Woodrow Wilson had resegregated federal
agencies, so changing your birth state to WV may have been a subtle form of resistance to his policies.

Useful experience: 
* Creating a fairly large data pipeline with several moving parts from scratch, and making heavy use of levenshtein string distance and modularity.
* Thinking big picture, as we are later going to use mTurk to aid in the matching process.

Quick Notes: My original code is quite nice, very malleable, and straightforward. My later code is not as nice. This is because once the code worked really well, I was assigned a new task, and so
the quick additions were last minute tweaks to improve efficiency before changing tasks. I may in the future tidy up the code. It also looks as though I will be assigned a similar task
with additional data, and so might write a new version of this as well.


#### Using Custom Google Search Engine (Feb 2021)
Languages: R
Quick desc: We needed to determine if current government employees were the same using email address. The task was to use a google web search on a specific site, e.g. "site://sitename"
and then find the civil servants full name. 
Quick example: 'arafeal@someagency.gov' matched to Rafael Adams (Not real email or name of course)

Useful experience: 
* Learned how to create google custom search engines (Very easy! Although there are some nuances (e.g. it's results differ from a default google search))
* Practice w/ levenshtein string distance

#### Scraped a website for procurement data (approx 1tb of xml files). Then converted the xml files into csv files. Used R's Rvest for scraping, Python's lxml for xml parsing. (Feb 2021)
Languages: R, Python
Useful experience: 
* Learned how to handle memory in coding. The xml files (some bigger than 30gb) were too large to fit into my computers (8gb) memory. Using lxml to load parts
of an xml tree into memory and then writing to disk was very interesting. I quite enjoyed lxml's itertree function.

* Learned how to use DropBox's API. My computer had approximately 200gb of SSD, of which at maximum about ~80gb can be free at anytime. As unzipping the xml files 
would sometimes exceed my disk space, I arranged to unzip files, process them, upload them to dropbox, and then delete the files on my computer. I used this until my 4tb external
hard drive arrived.

Notes: I would not use R in the future for large scale scraping. It had fairly slow download speeds. Still a wonderful tool, for when I need to scrape < 50gb of data on the go.

#### Made detailed plots of german counties w/ specific information (Feb 2021)
Languages: R
Quick desc: Had to match latitude and longitude points of protests in east germany within different spatial borders, e.g. counties, and municipalities. This required aggregation at
the specific spatial level, as well as then creating maps of the data.

Useful experience:
* Learned how to manipulate shape files, and wrote a simple package to check if lat/long points were within a shapefile's polygon.
* Learned how R's ggplot2 maps work. Harder than I thought.

Quick Notes: Finding which shape a point is in is slow. I don't think you're supposed to use shapefiles for this, but rather TopoJSON. However, I was restricted to use shapefiles due
to project constraints. My package also is not great, as I wrote it to aid my work, then abandoned it once I learned about TopoJSON.


#### Checking whether a town in India has a railroad nearby, and if it is a junction (Jan 2021)
Languages: R, and using a mouse MACRO.
Quick desc: Was tasked with extracting whether a town had a railroad, and then checking if that was a junction. The simplest solution I found for this was to record a short
mouse macro.

Useful experience:
* Writing macros using free software. (Shame on you, macros that pretend to be free!)
* String extraction (R)

#### Geocoding East German Towns (Fall 2020)
Languages: R, Google Maps API
Quick desc: Used google maps api to get the latitude and longitude of selected east german towns. For any outliers, I verified them using de.wikipedia which is better than the english
version when it comes to german towns.

Useful experience:
* Google Maps API
* Shapefiles (I used the historic east german provinces to identify outliers)
* Wikipedia. Wikipedia is awesome.


#### Misc Projects (Ongoing)
Languages: R, Julia, Python, Node.js
Quick desc: There are a bunch of random projects in my 'Regent' repository. These are generally attempts at me to learn something new about programming, like optimization. Maybe, someday,
I'll actually write something interesting there.

#### US Election Data(December 2020)
Languages: R, Python

Quick Desc: I was interested in why US elections have typically been so close. (e.g. less than 5% of the popular vote for the past 30 years, when compared to countries like Britain, which have had about half of the past elections decided by more than 5%
). Using rVest, I scraped wikipedia for election data, as I really did not like the election datasets I found publicly accessible. I then used integer programming (Python) to determine how many votes determined each election since 1964.

Useful experience:
* Scraping (rVest)
* Integer Programming (cvxopt)

Quick Notes: My Dad suggested this project, and we talked about it for a couple of weeks. He suggested using integer programming to calculate how many votes each side would have needed to win the election.
Love you Dad. I also gather British and Canadian election data through government provided datasets. I also created my first wikipedia account, as it was easier (and socially optimal!) to standardize a few nonstandard wikipedia
pages, than to adjust my scraping methods.

#### Extracting British India Historical Medical Data from Alto XML (TY National Library of Scotland) (Fall 2020)
Languages: Python

Quick desc: Had alto xml/ image pairs. I created a gui using PyQt that allowed me to draw boundary boxes around the image, and extract the information. This allowed me to quickly
build detailed datasets on British India Medical data such as child mortality, and vaccine spending by district.

Useful experience:
* Gui Design
* OCR
* XML

#### Cleaning a 1 million observation Civil Servant Database (US 1900s)
Languages: R

Quick desc: I cleaned a rather dirty dataset, and extracted department names as well as job titles. Since I started with no idea of what the job titles were, I eventually created a 
crosswalk of job titles, ranks, as well as common abbreviations and mistakes. I also used fuzzy matching, and regex to clean the dataset.

Useful experience:
* Regex
* Fuzzy Matching
* Learning that sometimes it's great to start from scratch with a different approach, especially when you're learning.

Quick Notes: I had to rush due to time constraints. (The dataset needed to be ready for a conference). 


#### Using Google Cloud Vision to turn 40 years of British Indian crop reports into a dataset (July 2020 - September 2020)
Languages: Python,

Quick desc: Using publicly available government magazines (available on internet archive), I set up a data pipeline using google cloud vision to 1) Identify crop reports, 2) Convert
Crop Reports to text, 3) Turn text data into a dataset. I also wrote some GUIs to manually aid the conversion of text data into datasets.

Useful experience:
* Gui Design (PyQt)
* Google Cloud Vision API (Thank you Google for the $300 free credit upon signing up)


#### Using Google Cloud Vision and PyQt for data extraction (Fall 2019)
Languages: Python

Quick desc: Used Google Cloud Vision to convert ~100,000 images of blue book data (British Colonial Data) into searchable text. I then made a GUI to take advantage of having
searchable text, to speed up a project where we needed to extract various data (e.g. pay, tenure) from blue book data.

Useful experience:
* Gui Design (TkInter) - I had a lovely time, but will be using PyQt in the future.
* Google Cloud Vision API (Thank you Google for the $300 free credit upon signing up)

