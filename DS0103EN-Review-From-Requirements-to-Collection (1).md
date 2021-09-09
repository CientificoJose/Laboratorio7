<img src = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0103EN-SkillsNetwork/labs/Module%202/images/IDSNlogo.png" width = 400>

# From Requirements to Collection

Estimated time needed: **15** minutes

## Objectives

After completing this lab you will be able to:

-   Understand Data Requirements
-   Explore the stages in Data Collection


## Table of Contents

<div class="alert alert-block alert-info" style="margin-top: 20px">
    
1. [Data Requirements](#0)<br>
2. [Data Collection](#2)<br>
</div>
<hr>


# Data Requirements <a id="0"></a>





<img src="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0103EN-SkillsNetwork/labs/Module%202/images/lab2_fig1_flowchart_data_requirements.png" width=500>


In the videos, we learned that the chosen analytic approach determines the data requirements. Specifically, the analytic methods to be used require certain data content, formats and representations, guided by domain knowledge.


In the **From Problem to Approach Lab**, we determined that automating the process of determining the cuisine of a given recipe or dish is potentially possible using the ingredients of the recipe or the dish. In order to build a model, we need extensive data of different cuisines and recipes.


Identifying the required data fulfills the data requirements stage of the data science methodology.

* * *


# Data Collection <a id="2"></a>


<img src="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0103EN-SkillsNetwork/labs/Module%202/images/lab2_fig2_flowchart_data_collection.png" width=500>


In the initial data collection stage, data scientists identify and gather the available data resources. These can be in the form of structured, unstructured, and even semi-structured data relevant to the problem domain.


#### Web Scraping of Online Food Recipes

A researcher named Yong-Yeol Ahn scraped tens of thousands of food recipes (cuisines and ingredients) from three different websites, namely:


<img src="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0103EN-SkillsNetwork/labs/Module%202/images/lab2_fig3_allrecipes.png" width=500>
<div align="center">
www.allrecipes.com
</div>
<br/><br/>
<img src="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0103EN-SkillsNetwork/labs/Module%202/images/lab2_fig4_epicurious.png" width=500>
<div align="center">
www.epicurious.com
</div>
<br/><br/>
<img src="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0103EN-SkillsNetwork/labs/Module%202/images/lab2_fig5_menupan.png" width=500>
<div align="center">
www.menupan.com
</div>
<br/><br/>


For more information on Yong-Yeol Ahn and his research, you can read his paper on [Flavor Network and the Principles of Food Pairing](http://yongyeol.com/papers/ahn-flavornet-2011.pdf?utm_email=Email&utm_source=Nurture&utm_content=000026UJ&utm_term=10006555&utm_campaign=PLACEHOLDER&utm_id=SkillsNetwork-Courses-IBMDeveloperSkillsNetwork-DS0103EN-SkillsNetwork-20083987).


Luckily, we will not need to carry out any data collection as the data that we need to meet the goal defined in the business understanding stage is readily available.


#### We have already acquired the data and placed it on an IBM server. Let's download the data and take a look at it.


<strong>Important note:</strong> Please note that you are not expected to know how to program in python. The following code is meant to illustrate the stage of data collection, so it is totally fine if you do not understand the individual lines of code. There will be a full course in this certificate on programming in python, <a href="http://cocl.us/PY0101EN_DS0103EN_LAB2_PYTHON_edX">Python for Data Science</a>, which will teach you how to program in Python if you decide to complete this certificate.


### Using this notebook:

To run any of the following cells of code, you can type **Shift + Enter** to excute the code in a cell.


Get the version of Python installed.



```python
# check Python version
!python -V
```

Read the data from the IBM server into a _pandas_ dataframe.



```python
import pandas as pd # download library to read data into dataframe
pd.set_option('display.max_columns', None)

recipes = pd.read_csv("https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0103EN-SkillsNetwork/labs/Module%202/recipes.csv")

print("Data read into dataframe!") # takes about 30 seconds
```

Show the first few rows.



```python
recipes.head()
```

Get the dimensions of the dataframe.



```python
recipes.shape
```

So our dataset consists of 57,691 recipes. Each row represents a recipe, and for each recipe, the corresponding cuisine is documented as well as whether 384 ingredients exist in the recipe or not beginning with almond and ending with zucchini.

* * *


Now that the data collection stage is complete, data scientists typically use descriptive statistics and visualization techniques to better understand the data and get acquainted with it. Data scientists, essentially, explore the data to:

-   understand its content,
-   assess its quality,
-   discover any interesting preliminary insights, and,
-   determine whether additional data is necessary to fill any gaps in the data.


### Thank you for completing this lab!

This notebook is part of a course called _The Data Science Method_. If you accessed this notebook outside the course, you can take this course, online by clicking [here](https://cocl.us/DS0103EN-Review-From-Requirements-to-Collection).

## Author

<a href="https://www.linkedin.com/in/aklson/" target="_blank">Alex Aklson</a>

## Change Log

| Date (YYYY-MM-DD) | Version | Changed By | Change Description                 |
| ----------------- | ------- | ---------- | ---------------------------------- |
| 2021-04-06        | 2.1     | Malika     | Updated lab link                   |
| 2020-09-25        | 2.0     | Lakshmi    | Fixed Typo errors                  |
| 2020-08-27        | 2.0     | Lavanya    | Moved lab to course repo in GitLab |

<hr>

## <h3 align="center"> © IBM Corporation 2020. All rights reserved. <h3/>

