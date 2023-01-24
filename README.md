# End-to-end-sales-report-using-Power-BI

## Introduction

Sales Analysis is the process of understanding how the business performs in terms of sales. It provides insights into the past, present, and future performance of a business and can be used to forecast trends, identify opportunities for growth, and develop a strategic action plan for the company.Sales analysis is an important aspect of running a successful business. Through sales analytics, we can decide which products to focus on, where to sell and how best to reach customers. Many sales analysis tools exist to help small businesses improve and grow their businesses.

Through this project we will analyze sales data from various aspects. The main objective here is to extract key performance indicators (KPIs) that will enable us to make data-driven decisions and improve company’s business.  

## Project steps :

1. Requirement gathering (Business Requirement Document(BRD) / Functioal Requirement document (FRD))
2. Data Collection (Database/CSV/EXCEL)
3. Data Modelling
4. Data Cleaning /Data pre- Processing
5. UI Reports (Charts/Custom Charts)
6. Additional Information(DAX Calculations)
7. RLS(Implement row level security)
8. Create workspace in Power BI Service to share among other team members
9. Publish
10. Dashboard
11. Gateway
12. Schedule Refresh
13. Add roles.Subscribe,alerts
14. Share the report
15. Create App and Share

## SECTION 1

### Requirement gathering /Data Collection

#### STEP 1 : 

The most important step is to get BRD/FRD form the client that indicates what the business wants to achieve.The BRD indicates all the project deliverables and the inputs and outputs associated with each process function.

A BRD describes what the product should do where as an FRd describes how the project should do it.BRD is mandatory for any project but FRD is optional.

Data required for this project is these formats:
* Sales (CSV files saved in folder by year)
* Categories (EXCEL)
* Geography (EXCEL)
* Product (CSV)
* SalesRep (EXCEL)
* SubCategory (EXCEL)


#### STEP 2 :

Load the Data into Power BI.

Sales data has 4 years data (2014,2015,2016,2017) in CSV file format saved in a folder by year which can be either loaded one by one as CSV file but instead of doing that it is better to do automation because if there comes more data for another years then the report will be automatically updated.

In order to do this we will do the following steps :

* Copy the path of the folder
* Get data
* Choose folder
* Give entire path
* Combine and load

![image](https://user-images.githubusercontent.com/105121789/214292911-9108f9e7-52fe-4409-880b-9eb8e25acc4c.png)

In the data we have 5 dimension tables and 1 facts table.

     
## SECTION 2

###  Data transformation / Data Computations

#### STEP 1 :

Go through all the tables and understand the data.

#### STEP 2 :

Create relationship using modelling but before that we need to do some transformations and cleaning.
