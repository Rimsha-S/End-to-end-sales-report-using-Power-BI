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

### Requirement gathering /Data Collection - (Project step 1 & 2)

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

###  Data transformation / Data Computations - (Project steps 3 & 4)

#### STEP 1 :

Go through all the tables and understand the data.

#### STEP 2 :

Create relationship using modelling but before that we need to do some transformations and cleaning.

After doing some transformationsand data cleaning we will build relationships between the table 

![image](https://user-images.githubusercontent.com/105121789/214298002-482f6a29-873e-47c0-81e0-1dd2a637170b.png)

Below are the various cleaning processess done on different tables.

![image](https://user-images.githubusercontent.com/105121789/214307675-215ec48d-8ffd-4088-9699-08e8f23fe15c.png)


We have also created a datemaster table because it is very helpful when we are working with time intelligence function.

![image](https://user-images.githubusercontent.com/105121789/214298698-3ec44565-4bdf-41e8-97d8-fcc180907d8e.png)


DAX Calculatons

We used DAX functions and calculated the following measures 

Total revenue:

![image](https://user-images.githubusercontent.com/105121789/214304162-e962d6f5-04bb-452a-a10f-2a1015b4bec8.png)

Total Cost:

![image](https://user-images.githubusercontent.com/105121789/214304485-2605791b-2374-44b7-b49f-24f5c6ef16df.png)


Gross profit :

![image](https://user-images.githubusercontent.com/105121789/214304555-feb37512-98fb-4c1c-ace3-dc6a0f85e5f0.png)


## SECTION 3

### Power BI Reports / UI 

#### STEP 1 : 
