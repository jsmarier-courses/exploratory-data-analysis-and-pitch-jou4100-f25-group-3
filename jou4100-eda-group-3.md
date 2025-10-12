**Oct.12, 2025**<br>
**JOU4100, Digital Journalism II**<br>
**Liam Fox, Noah Leafloor, and Luke Lau**<br>
**Presented to Jean-Sébastien Marier**<br>

# Exploratory Data Analysis (EDA) & Pitch



## EDA of the City of Ottawa's 2021 Census and Ward Data 

For this assignment, you must extract data from a dataset provided by the instructor. You must then clean and analyze the data, create exploratory charts/visualizations, and find a potential story idea. Your assignment must clearly detail your process. You are expected to write about 1500-2000 words, and to include several screen captures showing the different steps you went through. Your assignment must be written with the Markdown format and submitted on GitHub Classroom.

I have been assigning different versions of this project to my digital journalism and data storytelling students for a few years now. Its structure was inspired by the main sections/chapters of [*The Data Journalism Handbook*](https://datajournalism.com/read/handbook/one/). This version was further inspired by the [Key Capabilities in Data Science](https://extendedlearning.ubc.ca/programs/key-capabilities-data-science) program offered by the University of British Columbia (UBC).

**Here are some useful resources for this assignment:**

* [GitHub's *Basic writing and formatting syntax* page](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [The template repository for this assignment in case you delete something by mistake](https://github.com/jsmarier/jou4100_jou4500_mpad2003_project2_template)

Did you notice how to create a hyperlink? In Markdown, we put the clickable text between square brackets and the actual URL between parentheses.

And to create an unordered list, we simply put a star (`*`) before each item.

## 1. Introduction

In our Exploratory Data Analysis (EDA) assignment, our group of Digital Journalism students at the University of Ottawa will analyze data from the City of [Ottawa’s 2021 Long Form Census - Ward Data](https://open.ottawa.ca/datasets/ottawa::2021-long-form-census-ward-data/about). 

The data in the Census — which aims to collect data regarding demographic, social and economic characteristics representative of the entire population — was collected through questionnaires sent to all households in Ottawa by Statistics Canada as part of their National Census. The City originally published the dataset on November 28, 2023 and last updated on October 19, 2024. The City’s open Census data is updated in tandem with each National Census, which is collected every five years. Updated Ward and City data is expected to be updated in 2028, as the Census data will need to be processed after its collection in 2026. Eva Walrond, who works for the City’s Planning, Real Estate and Economic Development department, is the steward of the 2021 Long Form Census Data. The dataset includes information about Ottawa residents’ income, ethnicity, nationality, spoken languages, education and employment, among other variables. 

The original dataset published on the City of Ottawa’s open data portal can be found and downloaded [here](https://open.ottawa.ca/datasets/ottawa::2021-long-form-census-ward-data/about). 

The CSV file for the raw and unchanged dataset we will be using for our EDA can be found and downloaded [here](https://raw.githubusercontent.com/jsmarier/files-for-course-assignments/refs/heads/main/2021_Long_Form_Census_-_Ward_Data.csv) 

First, for our EDA assignment, we will explain the process of exporting a dataset in Google Sheets and note some general and specific observations about the data in the **Getting Data** section. 

Next, we will conduct a VIMO (valid, invalid, missing, outliers) analysis, clean our dataset and summarize key findings in the **Understanding Data** section. 

After this, we will pitch a story idea we gathered from our data analysis of the City of Ottawa’s Census in the **Potential Story** section.

 Last, we will cite the relevant course material we consulted for our EDA in the **References** section. 


## 2. Getting Data

Use two hashtag symbols (`##`) to create a level 2 heading like this one.

To include a screen capture, use the sample code below. Your images should be saved in the same folder as your `.md` file.

![](import-screen-capture.png)<br>
*Figure 1: The "Import file" prompt on Google Sheets.*

**Here are examples of functions and lines of code put in grey boxes:**

1. If you name a function, put it between "angled" quotation marks like this: `IMPORTHTML`.
1. If you want to include the entire line of code, do the same thing, albeit with your entire code: `=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)`.
1. Alternatively, you can put your code in an independent box using the template below:

``` r
=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)
```
This also shows how to create an ordered list. Simply put `1.` before each item.

## 3. Understanding Data

### 3.1. VIMO Analysis

Use three hashtag symbols (`###`) to create a level 3 heading like this one. Please follow this template when it comes to level 1 and level 2 headings. However, you can use level 3 headings as you see fit.

Insert text here.

Support your claims by citing relevant sources. Please follow [APA guidelines for in-text citations](https://apastyle.apa.org/style-grammar-guidelines/citations).

**For example:**

As Cairo (2016) argues, a data visualization should be truthful...

### 3.2. Cleaning Data

Insert text here.

### 3.3. Exploratory Data Analysis (EDA)

Insert text here.

**This section should include a screen capture of your pivot table, like so:**

![](pivot-table-screen-capture.png)<br>
*Figure 2: This pivot table shows...*

**This section should also include a screen capture of your exploratory chart, like so:**

![](chart-screen-capture.png)<br>
*Figure 3: This exploratory chart shows...*

## 4. Potential Story

Insert text here.

## 5. Conclusion

Insert text here.

## 6. References

Include a list of your references here. Please follow [APA guidelines for references](https://apastyle.apa.org/style-grammar-guidelines/references). Hanging paragraphs aren't required though.

**Here's an example:**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)
