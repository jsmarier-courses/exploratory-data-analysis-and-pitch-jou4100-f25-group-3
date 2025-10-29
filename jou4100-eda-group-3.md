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


To import the raw [dataset](https://raw.githubusercontent.com/jsmarier/files-for-course-assignments/refs/heads/main/2021_Long_Form_Census_-_Ward_Data.csv) into [Google Sheets](https://docs.google.com/spreadsheets/d/1r-4qwR_3zLg95GB5UP3KQ-1nzTT0DsBS9QNl8Lruv88/edit?gid=0#gid=0), we manually input the GitHub repository [CSV file](https://raw.githubusercontent.com/jsmarier/files-for-course-assignments/refs/heads/main/2021_Long_Form_Census_-_Ward_Data.csv) by inserting its URL with the import data function  —  _IMPORTDATA=“url”_  —  in the A1 cell.

The full function in cell A1 of our dataset was formatted as such:
`=IMPORTDATA("https://raw.githubusercontent.com/jsmarier/files-for-course-assignments/refs/heads/main/2021_Long_Form_Census_-_Ward_Data.csv")`

![Image of data imported into Google Sheets](<Screencaptureoforiginaldataset.png>)<br>

*Figure 1: Screen capture of the dataset in Google Sheets immediately after importation.* 

The public link to the dataset in our Google Sheets spreadsheet can be found [here](https://docs.google.com/spreadsheets/d/1r-4qwR_3zLg95GB5UP3KQ-1nzTT0DsBS9QNl8Lruv88/edit?gid=0#gid=0)

The full City of Ottawa 2021 Long Form Census dataset in Google Sheets is 26 columns by 2,603 rows. 

On its face, the data looks clear and accurate, although it is hard to digest due to the extensive quantity of demographic sample data included in the Census.


The columns are separated by each ward in the City of Ottawa, as well as cumulative data for the entire city summed from every ward. 

The order and labeling of all 24 wards are correct, according to the [City of Ottawa’s Mayor and City Councillors Directory](https://ottawa.ca/en/city-hall/mayor-and-city-councillors). 


The rows are organized by labels in the first column, each describing a different variable, and the corresponding values for each ward and the city as a whole are listed in the rest of the columns. 

For example, the 12th row in the dataset lists the number of people who are 30 to 34 years old in Ottawa’s total population for each ward and the entire city. 

While the data appears to be clean, for the most part, the full Census dataset is too overwhelming to conduct a thorough analysis. Therefore, we decided to focus our data analysis on the section of the dataset about commuting methods, distance, and times for the employed labour force aged 15 years or older with a usual place of work in Ottawa detailed in the 2021 Census. 

 Our group created [another sheet](https://docs.google.com/spreadsheets/d/1r-4qwR_3zLg95GB5UP3KQ-1nzTT0DsBS9QNl8Lruv88/edit?gid=1160608891#gid=1160608891), copying the data from rows 2575 to 2595 from the raw, original dataset into a more digestible dataset on commuting behaviour. 

 All of the variables we analyzed in our dataset about commuting habits in the City of Ottawa are continuous variables.

 
According to Statistics Canada’s [Power from Data handbook](https://www150.statcan.gc.ca/n1/edu/power-pouvoir/ch8/5214817-eng.htm), a variable is continuous if “it can assume an infinite number of real values within a given interval.” The variables in our dataset measure the number of people in a population, which can assume an infinite number of real values and a meaningful zero. 

For instance, row four in our commuting behaviour dataset features continuous variables about people aged 15 or over in the labour force who commute by driving a car, van, or truck to their place of work in each ward of the City of Ottawa. 

Column P in our condensed dataset features continuous variables about the commuting habits of Somerset Ward residents in the labour force aged 15 or over.

 Row 18 features continuous variable observations about the number of people across the city who leave for work between 6:00 to 6:59 a.m. 

 
Our group observed that while over 210,000 people aged 15 or over in Ottawa’s labour force use a motor vehicle to commute to work, only about 64,000 people — which is under 25% of the sample — reported using other methods such as public transit, walking, or biking to get to work. 

Based on this observation, our group formulated the hypothesis that the City of Ottawa and other levels of government — amid efforts to reduce carbon emmission and combat climate change — are prioritizing and investing in initiatives that incentivize alternative methods of transportation, such as public transit and active transportation infrastructure.

Our observation that the large majority of the labour force who commute to work in Ottawa drive a personal motor vehicle also led us to wonder, “Is Ottawa more car-centric than other major Canadian cities and if so, why?” 

## 3. Understanding Data

### 3.1. VIMO Analysis

Use three hashtag symbols (`###`) to create a level 3 heading like this one. Please follow this template when it comes to level 1 and level 2 headings. However, you can use level 3 headings as you see fit.

### 3.1. VIMO Analysis

![Screenshot](<Screenshot 2025-10-29 163314.png>)<br>

Methods for exploring the validity and correctness of the data was done through a vimo analysis. Following Statistics Canada’s guide for “Data Accuracy and Validation: Methods to ensure the quality of data,” a vimo analysis was conducted where the accuracy and validity was assessed. 

Focusing on the dataset, finding any invalid, missing, or outlier values was done to determine the quality and validity. No errors or outliers were detected. However, the data is continuous as it changes frequently. Additionally, twenty five per cent sample data was collected for the methods, duration, and time for the 24 wards.

For exploring the correctness of the data, the 2016 total census for wards one to 23 was the best option for comparing the 2021 data. The 2016 census was then explored and found comparable data like methods of transportation, duration, and time. However, since it is 2016, the number of wards has changed to 24. They also broke up the three identified columns (method, duration, time) between gender. While analyzing the correctness of the data, they also used a 25 per cent sample in 2016. The population was proportionate as it went up slightly in 2021. Furthermore, since the data is from the City of Ottawa, the accuracy is trusted more.

The 2021 dataset was explored for its validity and correctness of data after choosing to focus on the commuting census. There was little to improve since the vimo analysis was not large. The level of accuracy is trusted since the data comes from the City of Ottawa’s official census and Statistics Canada. Additionally, it is difficult to measure and find other sources of the focused data, because it is about duration and time along methods for transportation.
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
