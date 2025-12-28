<p align="center">
    <img src="https://howtolearnmachinelearning.com/wp-content/uploads/2021/04/coursera_machine_learning_ibm.png?raw=true" alt="IBM and Coursera Logos" width="926" height="133"/>
</p>

# Data Visualization with Python

This is the Capstone Project for Course 9, _IBM Data Analyst Capstone Project_. Part of IBM's Data Analyst Professional Certificate from Coursera.

I will take on the role of a Data Analyst with a global IT and Business Services firm. In this role, I will be analyzing several datasets to help identify trends for emerging technologies. We have recently been hired as a Data Analyst by a global IT and business consulting services firm that is known for its expertise in IT solutions and its team of highly experienced IT consultants. To keep pace with changing technologies and remain competitive, our organization regularly analyzes data to help identify future skill requirements.

As a Data Analyst, I will be assisting with this initiative and have been tasked with collecting data from various sources and identifying trends for this year's report on emerging skills.

### Task 1

The first task is to collect data for the technology skills that are most in demand from various sources including job postings, blog posts, and surveys. I will begin by scraping internet websites and accessing APIs to collect data in various formats like .csv files, excel sheets, and databases.

### Task 2

Once I've collected enough data, I will take the collected data and prepare it for analysis by using data wrangling techniques like finding duplicates, removing duplicates, finding missing values, and inputting missing values.

### Task 3

Now that the data is ready, I will apply statistical techniques to analyze the data and identify insights and trends like: What are the top programming languages that are in demand? What are the top database skills that are in demand? What are the most popular IDEs? And Demographic data like age and education level distribution of developers.

### Task 4

In the fourth task, I'll focus on choosing appropriate visualizations based on the data I want to present using charts, plots, and histograms to help reveal my findings and trends. I am going to access the Data from an SQL database and pull only the data I need into DataFrames.

### Task 5

For task 5, I will employ Cognos to create interactive dashboards to help analyze and present the data dynamically.

### Task 6

For the final task, I will use my storytelling skills to provide a narrative and present the findings of my analysis.

## Table of Contents

- [Data Description](#data-description)
- [Tools](#tools)
- [Deliverables](#deliverables)
  - [Task 1: Data Collection](#task-1-data-collection)
  - [Task 2: Data Wrangling](#task-2-data-wrangling)
  - [Task 3: Exploratory Data Analysis](#task-3-exploratory-data-analysis)
  - [Task 4: Data Visualization](#task-4-data-visualization)
  - [Task 5: Dashboard Creation](#task-5-dashboard-creation)
  - [Task 6: Presentation of Findings](#task-6-presentation-of-findings)
- [Stretch Goals](#stretch-goals)

## Data Description

Stack Overflow, a popular website for developers, conducted an online survey of software professionals across the world. The survey data was later open sourced by Stack Overflow. The actual data set has around 49,000+ responses from 177 countries across 62 questions.

The dataset I am going to use comes from the following source: https://survey.stackoverflow.co/ under a ODbL: Open Database License.

I will be given a subset of the original data set in this capstone project. We will explore, analyze, and visualize this dataset and present my analysis.

Note: This randomised subset contains around 1/10th of the original data set. Any conclusions we draw after analyzing this subset may not reflect the real world scenario.

The dataset is available as a .csv file here.

The below table lists the questions asked in the survey and the column under which the response was collected.

<details>
 <summary><strong>View Table</strong></summary>
<table>
  <thead>
    <tr>
      <th>Column Name</th>
      <th>Question Text</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ResponseId</td>
      <td>
        Randomized respondent ID number.
      </td>
    </tr>
    <tr>
      <td>MainBranch</td>
      <td>
        Which of the following options best describes you today? 
      </td>
    </tr>
    <tr>
      <td>Age</td>
      <td>What is your age?</td>
    </tr>
    <tr>
      <td>Employment</td>
      <td>What is your current employment status?</td>
    </tr>
    <tr>
      <td>RemoteWork</td>
      <td>How often do you work remotely?</td>
    </tr>
    <tr>
      <td>Check</td>
      <td>
        Check Various verification or check questions related to survey consistency.
      </td>
    </tr>
    <tr>
      <td>CodingActivities</td>
      <td>
          What coding activities do you engage in (hobby, professional, and open-source contributions)?
      </td>
    </tr>
    <tr>
      <td>EdLevel</td>
      <td>
        What is the highest level of formal education you have completed?
      </td>
    </tr>
    <tr>
      <td>LearnCode</td>
      <td>
        How did you learn to code?
      </td>
    </tr>
    <tr>
      <td>LearnCodeOnline</td>
      <td>Have you used online resources to learn coding?</td>
    </tr>
    <tr>
      <td>TechDoc</td>
      <td>
        How do you use technical documentation?
      </td>
    </tr>
    <tr>
      <td>YearsCode</td>
      <td>
        How many years have you been coding?
      </td>
    </tr>
    <tr>
      <td>YearsCodePro</td>
      <td>
        How many years have you coded professionally?
      </td>
    </tr>
    <tr>
      <td>DevType</td>
      <td>What is your role or type of development work you do?</td>
    </tr>
    <tr>
      <td>OrgSize</td>
      <td>
        What is the size of the organization you work for?
      </td>
    </tr>
    <tr>
      <td>PurchaseInfluence</td>
      <td>
        How much influence do you have on purchasing technology at your company?
      </td>
    </tr>
    <tr>
      <td>BuyNewTool</td>
      <td>How does your company decide whether to buy new tools or technology?</td>
    </tr>
    <tr>
      <td>BuildvsBuy</td>
      <td>
        Does your company prefer to build or buy software?
      </td>
    </tr>
    <tr>
      <td>TechEndorse</td>
      <td>Do you endorse any specific technologies at your company?</td>
    </tr>
    <tr>
      <td>Country</td>
      <td>In which country do you reside?</td>
    </tr>
    <tr>
      <td>Currency</td>
      <td>Which currency do you use day-to-day?</td>
    </tr>
    <tr>
      <td>CompTotal</td>
      <td>
        What is your current total compensation (salary, bonuses, and so on)?
      </td>
    </tr>
    <tr>
      <td>LanguageHaveWorkedWith</td>
      <td>Which programming languages have you worked with in the past year?</td>
    </tr>
    <tr>
      <td>LanguageWantToWorkWith</td>
      <td>
        Which programming languages do you want to work with in the future?
      </td>
    </tr>
    <tr>
      <td>LanguageAdmired</td>
      <td>Which programming languages do you admire most?</td>
    </tr>
    <tr>
      <td>DatabaseHaveWorkedWith</td>
      <td>
        Which database technologies have you worked with in the past year?
      </td>
    </tr>
    <tr>
      <td>DatabaseWantToWorkWith</td>
      <td>
        Which database technologies do you want to work with in the future?
      </td>
    </tr>
    <tr>
      <td>DatabaseAdmired</td>
      <td>
        Which database technologies do you admire most?
      </td>
    </tr>
    <tr>
      <td>PlatformHaveWorkedWith</td>
      <td>
        Which platforms have you worked with in the past year?
      </td>
    </tr>
    <tr>
      <td>PlatformWantToWorkWith</td>
      <td>
        Which platforms do you want to work with in the future?
      </td>
    </tr>
    <tr>
      <td>PlatformAdmired</td>
      <td>Which platforms do you admire most?</td>
    </tr>
    <tr>
      <td>WebframeHaveWorkedWith</td>
      <td>
        Which web frameworks have you worked with in the past year?
      </td>
    </tr>
    <tr>
      <td>WebframeWantToWorkWith</td>
      <td>Which web frameworks do you want to work with in the future?</td>
    </tr>
    <tr>
      <td>WebframeAdmired</td>
      <td>Which web frameworks do you admire most?</td>
    </tr>
    <tr>
      <td>EmbeddedHaveWorkedWith</td>
      <td>
        Which embedded systems have you worked with in the past year?
      </td>
    </tr>
    <tr>
      <td>EmbeddedWantToWorkWith</td>
      <td>Which embedded systems do you want to work with in the future?</td>
    </tr>
    <tr>
      <td>EmbeddedAdmired</td>
      <td>Which embedded systems do you admire most?</td>
    </tr>
    <tr>
      <td>MiscTechHaveWorkedWith</td>
      <td>
        Which miscellaneous technologies have you worked with in the past year?
      </td>
    </tr>
    <tr>
      <td>MiscTechWantToWorkWith</td>
      <td>Which miscellaneous technologies do you want to work with in the future?</td>
    </tr>
    <tr>
      <td>MiscTechAdmired</td>
      <td>Which miscellaneous technologies do you admire most?</td>
    </tr>
    <tr>
      <td>OpSysPersonal</td>
      <td>
        What operating systems do you use for personal tasks?
      </td>
    </tr>
    <tr>
      <td>OpSysProfessional</td>
      <td>
        What operating systems do you use for professional tasks?
      </td>
    </tr>
    <tr>
      <td>SOVisitFreq</td>
      <td>
        How frequently do you visit Stack Overflow?
      </td>
    </tr>
    <tr>
      <td>SOAccount</td>
      <td>
        Do you have a Stack Overflow account?
      </td>
    </tr>
    <tr>
      <td>SOPartFreq</td>
      <td>
        How often do you participate in Q&A on Stack Overflow?
      </td>
    </tr>
    <tr>
      <td>AISelect</td>
      <td>
        How do you feel about artificial intelligence tools for development?
      </td>
    </tr>
    <tr>
      <td>AIBen</td>
      <td>
        What benefits have you experienced from using AI tools?
      </td>
    </tr>
    <tr>
      <td>AIChallenges</td>
      <td>
        What challenges have you faced while using AI tools?
      </td>
    </tr>
    <tr>
      <td>JobSat</td>
      <td>
        How satisfied are you with your current job?
      </td>
    </tr>
  </tbody>
</table>

</details>

## Tools

- [`python`](https://www.python.org/downloads/) v3.12.2
- [`pandas`](https://pandas.pydata.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for managing the data.
- [`numpy`](https://numpy.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for mathematical operations.
- [`seaborn`](https://seaborn.pydata.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for visualizing the data.
- [`matplotlib`](https://matplotlib.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for additional plotting tools.
- [`folium`](https://python-visualization.github.io/folium/latest/) for geospatial data visualization such as choropleth maps.
- [`plotly`](https://plotly.com/python/) for interactive plotting tools.
- [`Google Looker Studio`](https://lookerstudio.google.com/overview) for dashboards.
- [`IBM Cognos Analytics`](https://www.ibm.com/products/cognos-analytics) for dashboards.

## Deliverables

### Task 1: Data Collection

- [x] Collecting Data Using APIs
- [x] Collecting Data Using Web Scraping
- [x] Exploring Data

### Task 2: Data Wrangling

- [x] Finding Missing Values
- [x] Determine Missing Values
- [x] Finding Duplicates
- [x] Removing Duplicates
- [x] Normalizing Data

### Task 3: Exploratory Data Analysis

- [x] Distribution
- [x] Outliers
- [x] Correlation

### Task 4: Data Visualization

- [x] Visualizing Distribution of Data
- [x] Relationship
- [x] Composition
- [x] Comparison

### Task 5: Dashboard Creation

- [x] Dashboards

### Task 6: Presentation of Findings

- [x] Final Presentation

## Stretch Goals

- [ ] Create Dashboard in Google Looker or Tableau
