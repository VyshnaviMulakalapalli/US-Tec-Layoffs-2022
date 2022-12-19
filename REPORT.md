# Project Report
## Authors - Sriram and Vyshnavi

## 1. Purpose 

* The dataset used for the project is regarding the US Tech Layoffs in 2022.
* This dataset is taken from crunchbase website - `https://news.crunchbase.com/startups/tech-layoffs-2022/`
* Author of this dataset is **Keerthi Vedantham**.
* The dataset was last updated on December 9,2022.
* The dataset has 355 rows and 8 attributes which provides details about the layoffs in different companies.
* The attributes are:
     * Company: Name of the company

     * Reported Layouts: No of reported Layouts

     * Workers impacted: Percentage of workers impacted in the respective company

     * Reported date:Date which Layoff's reported

     * Industry: Type of Industry

     * HQ: Headquarters of company

     * Source:In which the article is published
  
     * Company status: whether is private or public

* In this project, we have investigated on the below questions:
  1) What are the industries that have major impact?

  2) What are the ranges of percentage of impact in each type of company(public or private)? What are the companies in those ranges.

  3) What is the impact of layoffs in each city?

## 2. Approach 

### What are the industries that have major impact?

* Initially an empty dictionary named `company_dict` will be created.
* Using a **for** loop, dictionary `company_dict` is transformed into a dictionary with keys as the industry names and values as the total number of layoffs in each industry.
* Next all the values of this dictionary which are total number of layoffs in different industries will be stored in a list `lst`.
* This list `lst` will be sorted and reversed in order to have the elements in the list in descending order.
* A variable `rank` is created and 1 is assigned to it.
* Next using another **for** loop, all the values in dictionary `company_dict` and elements in the list `lst` will be compared.
* In the dictionary `company_dict`, the key which has its value as the first element(the highest number of layoffs) in list `lst` is taken as key to another new dictionary `comp_dict` and give its value as `rank` which indicates its impact.
* The above step is repeated for all the values in dictionary `company_dict` and rank is incremented during each key-value assignment to dictionary `comp_dict`.
* Now the dictionary `comp_dict` has the industry names as keys and its values are the ranks indicating its level of impact.

