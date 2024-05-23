# Documentation Outline

The idea is to create descriptions of what we would like the ALR to do.

The writing style will be based on the following:

The guide will be considered a Step-by-step guide acording to the Diátaxis method as the audience will be users familiar with data science tooling and paper writing (as Diátaxis describes it - a work place instruction).

 - Technical writing method: Diátaxis - https://diataxis.fr/
 - Technical writing style: MDN Web Docs - https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide
 - Style guide: APA - https://apastyle.apa.org/

The writing tooling has not yet been selected.

Contributors:

 - [@neerajkumaris](https://github.com/neerajkumaris)
 - [@Amit](https://github.com/ydv-amit-ydv)
 - [@Adesh212](https://github.com/Adesh212)
 - [@Simon Worthington](https://github.com/mrchristian)

## SECTIONS

## Orientation and learning points

Assigned @NOT ASSIGNED - 

**Questions:** 

**Notes:** 

**Outline:**

## A literature review question?

Assigned [@neerajkumaris](https://github.com/neerajkumaris) - 

**Questions:** 

How does the author report on their question in the literature review in terms of the use of ALR?

**Notes:** 

**Outline:**

## Using CoLab

Assigned [@neerajkumaris](https://github.com/neerajkumaris) - 

**Questions:** 

- How and when to add CoLab to GitHub? [@Simon Worthington](https://github.com/mrchristian)

**Notes:** 

**Outline:**

## Install

Assigned [@neerajkumaris](https://github.com/neerajkumaris) - 

**Questions:** 

**Notes:** 

**Outline:**

## Searching open corpora<br>

Assigned [@Amit](https://github.com/ydv-amit-ydv) <br>

**Identification of the Topics and queries** <br>
	
	Start by removing the stop words and select the most relevant keywords<br>
	For example : Ques : What is the role of silicon transporter in the rice ? <br>
	Step 1 : Remove Stop words : Remaing words are :   Role , Silicon , transorter, rice <br>
	
**Installation of the Semantic toolkit :**<br>
		_Using Desktop :_<br>
		1)_(skip if already installed)_: Install python by downloading from the : https://www.python.org/downloads/<br>
			Add path variable in the installation process<br>
	    2) Open command promt: and type <code> pip install pygetpapers </code><br>
		2)                              <code> pip install docanalysis </code><br>
		

**Searching the corpora (EUPMC) :**<br>
	Open the command terminal in ther directory where you wish to store your project<br>
	1) <code>  _pygetpapers -q "your query terms" -n "lantana_query_config"--save_query_ </code>   Using this you will be able to count the total number of available papers on EUPMC for the query , <br>
				we can also use the attributes like -startdate and enddate to filter out the query <br>
				
	2 ) <code> _pygetpapers -q " role silicon transporter rice " -k 10 -p -x -makecsv -makehtml -o path/to/some/output/directory/optional --loglevel debug -x --logfile test_log.txt_ </code><br>
 
				This will download the 10 papers from the EUPMC in both the xml and pdf formats , make the csv and html of the associated metadata and download these papers in the given output directory	<br>
				Similarly we can download more papers and make the entire cProject tree<br>
				_--loglevel debug -x --logfile test_log.txt_ is to write the log to a .txt file in your HOME directory, while simultaneously printing it out.<br>
				When _o output ath is not given the downloaded copora is saved to the pwd as a time-stamed directory<br>

**Outline:**

## Analysing your collection

Assigned [@Adesh212](https://github.com/Adesh212) -

**Questions:** 

**Notes:** 

**Outline:**

## Using the literature collection in your review paper

Assigned [@Simon Worthington](https://github.com/mrchristian) -

**Notes:** 

The author needs to use the collection, and information and data about the collection in their literature review paper. 

**Questions:** 

What does the collection (or what would we like it to collect) and the process produce that the author can use in their paper?

 - A complete Git repository
 - A replicable and reusable system
 - A DOI references data and code set on Zenodo or other academic repository as a full GitHub repository using Software Citation
 - A saved query: https://pygetpapers.readthedocs.io/en/latest/user_documentation.html#example-query Flag --save_query as saved_config.ini
 - A CProject for the whole query
 - A CTree per paper
 - Custom terms and dictionaries
 - Data analysis results?
  - Hits
  - Word frequency
 - Bibtex output and import with content an/or contnet links to Zotero
 - CSS Paged media outputs

**Outline:**

**Ideal process**

 - Add reference list to the paper and store it in Zotero
 - Take a GitHub Release of repository add to Zenodo and link as data to paper
 - Link to all papers in repo CTree
 - Present question and methods for converting into query, show table of queries, link to data
 - Provide information on how to reproduce and reuse / extend the CProject
 - Present data analysis of literature review in paper
  - Chart and data link to number of hits
  - Chart of NGram of search term
  - Table of word frequency
  - Table of top ten papers
  - Table of top journals, top authors

**Current process**

 - Take a GitHub Release of repository add to Zenodo and link as data to paper
 - Link to all papers in repo CTree
 - Present question and methods for converting into query, show table of queries, link to data
 - Provide information on how to reproduce and reuse / extend the CProject
 - Present data analysis of literature review in paper
  - Table of the number of hits
  - Table of word frequency
  - Table of top ten papers
  - Table of top journals, top authors

## Other sections

### Metadata

### Other publication sections needed

Covers, title pages, table of contents, contributors, etc. See style guide: APA - https://apastyle.apa.org/

### Colophon

### Introduction

### Resources

### Glossary and abbreviations

### References

Zotero collection: 




