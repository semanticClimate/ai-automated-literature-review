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

When the author reports on their question in the literature review using Automated Literature Review (ALR) tools such as pygetpapers, they typically follow a systematic process that leverages the capabilities of the tool to enhance the efficiency and comprehensiveness of their review. 

**Outline:**
Outline for Reporting on the Research Question in the Literature Review Using pygetpapers :

**Introduction:**

1. Introduce the research question and its significance.
2. Provide background information on the topic.
3. Explain the relevance of Automated Literature Review (ALR) tools like pygetpapers.
4. State the purpose of the literature review and its organization.

**Methodology for Literature Search:**

1. Describe the methodology used to conduct the literature search.
2. Explain the use of pygetpapers for automating the retrieval of academic papers.
3. Specify the search strategy, including keywords, phrases, and Boolean operators.
4. Detail the sources from which papers were retrieved (e.g., Europe PMC).

**Selection Criteria and Filtering:**

1. Define the inclusion and exclusion criteria used to filter the search results.
2. Discuss the process of filtering papers based on relevance and quality.
3. Highlight any manual or programmatic filtering techniques employed.

**Organization and Categorization:**

1. Explain how the retrieved literature was organized and categorized.
2. Discuss the criteria used for categorization, such as themes, methodologies, or findings.
3. Provide insights into the structure of the literature review based on these categories.

**Synthesis of Findings:**

1. Summarize the main findings from the retrieved literature.
2. Discuss common themes, trends, and patterns identified in the literature.
3. Highlight any contradictions or inconsistencies among the findings.

**Critical Analysis and Quality Assessment:**

1. Conduct a critical analysis of the methodologies employed in the retrieved studies.
2. Assess the reliability, validity, and generalizability of the findings.
3. Utilize metrics such as citation counts or impact factors to evaluate the quality of the literature.

**Conclusion:**

1. Summarize the key findings and insights from the literature review.
2. Reiterate the significance of the research question and its implications for the field.
3. Reflect on the role of ALR tools like pygetpapers in facilitating the literature review process.

## Using CoLab

Assigned [@neerajkumaris](https://github.com/neerajkumaris) - 

**Questions:** 

- How and when to add CoLab to GitHub? [@Simon Worthington](https://github.com/mrchristian)

**Notes:** 

**Outline:**

**When to Add CoLab to GitHub**

1. To keep track of changes and revisions to your notebooks.

2. To easily share notebooks with collaborators and work together on the same project.

3. To keep a backup of your work in case of accidental deletions or changes.

4. To integrate your notebooks into a larger project managed on GitHub, benefiting from issues tracking, pull requests, and other GitHub features.

**Steps to integrate Google Colab to GitHub**

**1. Linking GitHub to Colab**

**First, you need to link your GitHub account with your Google Colab account:**

a. Open a Google Colab notebook.

b. Click on "File" in the menu.

c. Select "Save a copy in GitHub".

d. If you haven't linked your GitHub account before, a prompt will appear asking you to authenticate with GitHub. Follow the instructions to grant access.

**2. Saving a Colab Notebook to GitHub**

**Once your GitHub account is linked, you can save notebooks directly to a GitHub repository:**

a. Open the notebook you want to save.

b. Click on "File" in the menu.

c. Select "Save a copy in GitHub".

d. A dialog will appear where you can specify the repository, the branch, and the commit message.

e. Click "OK" to save the notebook to the specified GitHub repository.

**3. Opening a Notebook from GitHub in Colab**

**To open a notebook directly from a GitHub repository:**

a. Go to the Google Colab homepage.

b. Click on "GitHub" in the menu.

c. Authenticate with your GitHub account if prompted.

d. Search for the repository or notebook you want to open.

e. Click on the notebook to open it in Colab.

**4. Using Git Commands in Colab**

**For more advanced use cases, you can use Git commands directly within a Colab notebook:**

**Start by cloning a repository:**

!git clone https://github.com/yourusername/yourrepository.git 

**Navigate into the repository directory:**

%cd yourrepository 

You can now use other Git commands, such as git pull, git add, git commit, and git push, just like you would in a local development environment.

## Install

Assigned [@neerajkumaris](https://github.com/neerajkumaris) - 

**Questions:** 

**Notes:** 

**Outline:**

## Searching open corpora</br>

Assigned [@Amit](https://github.com/ydv-amit-ydv) </br>

### **Identification of the Topics and queries** <br>
	
Start by removing the stop words and select the most relevant keywords<br><br>
For example : Ques : What is the role of silicon transporter in the rice ?<br><br>
>Step 1 : Remove Stop words : Remaing words are :   Role , Silicon , transorter, rice <br>
	
### **Searching the corpora (EUPMC)** <br><br>
Open the command terminal in ther directory where you wish to store your project<br>
>Step 2 : <code>  _pygetpapers -q "your query terms" -n "lantana_query_config"--save_query_ </code><br>

Using this you will be able to count the total number of available papers on EUPMC for the query  <br><br>
We can also use the attributes like -startdate and enddate to filter out the query <br>
				
>Step 3 : <code> _pygetpapers -q " role silicon transporter rice " -k 10 -p -x -makecsv -makehtml -o path/to/some/output/directory/optional --loglevel debug -x --logfile test_log.txt_ </code><br>
 
This will download the 10 papers from the EUPMC in both the xml and pdf formats , make the csv and html of the associated metadata and download these papers in the given output directory<br><br>
Similarly we can download more papers and make the entire cProject tree<br>
>_--loglevel debug -x --logfile test_log.txt_ is to write the log to a .txt file in your HOME directory, while simultaneously printing it out.<br>

>_When -o output path is not given the downloaded copora is saved to the pwd as a time-stamed directory<br>_


### **Short Summary of the essential tags of the pegetapers**

|Flag|What it does|In this case `pygetpapers`...|
|---|---|---|
|`-q`|specifies the query|queries for 'invasive plant species' in METHODS section|
|`-k`|number of hits (default 100)|limits hits to 10|
|`-o`|specifies output directory|outputs to invasive_plant_species_test|
|`-x`|downloads fulltext xml||
|`-c`|saves per-paper metadata into a single csv|saves single  CSV named [`europe_pmc.csv`](resources/invasive_plant_species_test/europe_pmc.csv)|
|`--makehtml`|saves per-paper metadata into a single HTML file|saves single HTML named [`europe_pmc.html`](resources/invasive_plant_species_test/eupmc_results.html)|
|`--save_query`|saves the given query in a `config.ini` in output directory|saves query to [`saved_config.ini`](resources/invasive_plant_species_test/saved_config.ini)|


`pygetpapers`, by default, writes metadata to a JSON file within:
- individual paper directory for corresponding paper (`epmc_result.json`)
- working directory for all downloaded papers ([`epmc_results.json`](resources/invasiv_plant_species_test/eupmc_results.json))

### **Notes :**
-The query terms can be also specified in the purticular section like Abstract, methods, results etc 
><code>C:\Users\lilia>pygetpapers -q abstract:"money" -n<br>
INFO: Total number of hits for the query are 22161</code>

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




