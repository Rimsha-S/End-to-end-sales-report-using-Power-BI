# Retail Sales-Analysis-An End To End Project in - Power-BI

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


#### DAX Calculatons

We used DAX functions and calculated the following measures 


##### Total revenue:

![image](https://user-images.githubusercontent.com/105121789/214304162-e962d6f5-04bb-452a-a10f-2a1015b4bec8.png)



##### Total Cost:

![image](https://user-images.githubusercontent.com/105121789/214304485-2605791b-2374-44b7-b49f-24f5c6ef16df.png)



##### Gross profit :

![image](https://user-images.githubusercontent.com/105121789/214304555-feb37512-98fb-4c1c-ace3-dc6a0f85e5f0.png)


## SECTION 3

### Power BI Reports / UI 

#### STEP 1 : 

We will create slicers for country,years and months

![image](https://user-images.githubusercontent.com/105121789/214312190-5c3c38e9-8c3b-4b8b-bb84-281d0ea46e79.png)

We will use cards to display sum of total revenue ,sum of gross profit and sum of units

![image](https://user-images.githubusercontent.com/105121789/214313280-302338ca-ec3b-45fc-8091-ccdeface69e9.png)

Using multicard top 5 salespersons can be represented

![image](https://user-images.githubusercontent.com/105121789/214313583-06407b80-8f33-4959-aa2c-ea2999056c3b.png)

Sum of Total revenue by year and Product Name

![image](https://user-images.githubusercontent.com/105121789/214314702-c3cef9d5-6b92-4716-8baf-4646a6749933.png)


Sum of Total revenue by Product Name and Sub category name

![image](https://user-images.githubusercontent.com/105121789/214315029-d74597b9-cc2a-41da-b7a6-44b62b880936.png)

We will create a new measure and calculate the quater on quater growth and plotted a graph by sum of total revenure and QOQ growth

![image](https://user-images.githubusercontent.com/105121789/214316272-56a3f15f-eb43-42dc-8788-88cc7eda01c7.png)

We will also create a new measure and calculate the Month on Month growth

![image](https://user-images.githubusercontent.com/105121789/214317489-4e495b89-d4f3-483a-a074-de764cb704fd.png)


## SECTION 4 

### Dashboarding / Publishing

![image](https://user-images.githubusercontent.com/105121789/214320383-bd20d069-ff72-4e9d-9288-87a6e995da3e.png)

#### We will now implement RLS 

Row-level security (RLS) with Power BI can be used to restrict data access for given users. Filters restrict data access at the row level, and you can define filters within roles. In the Power BI service, members of a workspace have access to datasets in the workspace. RLS doesn't restrict this data access.
Two main types of RLS can be implemented into your Power BI report: Status RLS and Dynamic RLS.

When choosing between Static RLS and Dynamic RLS, here is a good rule of thumb: Use Static RLS if: You need to restrict data visibility for a specific group of users that require the same level of information (e.g., regional sales team to view data for their specific region).

Using dynamic role-level security, you can restrict users' access to reports and dashboards based on their login credentials. This is one of Power BI's more advanced features that is covered in our Power BI classes.

RLS has to be implemented in Power BI desktop then only it can be pushed to Power BI service 

Go to manage roles and create roles using DAX expression

![image](https://user-images.githubusercontent.com/105121789/214328373-64a35c86-12ed-400b-b85d-1feda8629869.png)

We will create a workspace in Power BI service

![image](https://user-images.githubusercontent.com/105121789/214329577-de2bcc6d-7730-46db-8425-c5521895fc3a.png)


#### Next step we will publish the report to workspace

![image](https://user-images.githubusercontent.com/105121789/214330444-4eb5463f-9a0c-4014-a38e-2621535d7489.png)

There are four roles in Power BI workspace, Admin, Member, Contributor, and Viewer.Now we can give access to as many people as we need by selecting the different roles.

#### Next step is to create a dashboard

A Power BI dashboard is a single page, often called a canvas, that tells a story through visualizations. Because it's limited to one page, a well-designed dashboard contains only the highlights of that story. Readers can view related reports for the details.

![image](https://user-images.githubusercontent.com/105121789/214332174-1f89478c-7ef8-452b-9611-bd1a72e3d585.png)


We will pin the required charts to the dashboard and arrange properly in the tile format.

![image](https://user-images.githubusercontent.com/105121789/214337141-58d36a44-6e32-4c05-a932-2fc4e331d696.png)

We can edit the theme of the dashboard add title and cuatom the look of the Dashboard.

![image](https://user-images.githubusercontent.com/105121789/214341430-090a204e-0a5a-4329-bcd9-5c3c8314cead.png)


In the next step we will create a gateway which will set up a connection between desktop and service by automating the refreshes.Inorder to create a gateway we have to first download the data gateway.

![image](https://user-images.githubusercontent.com/105121789/214343027-a7b9796c-3625-45d3-a42d-630877836a8f.png)


There re two types of gateways:

* Standard Mode
* Personal Mode

The difference is the way that you want to use the gateway. The personal mode is mainly used for one-person use, not for the team. On-premises standard gateway, on the other hand, is a choice when you want to work in a collaborative environment.

![image](https://user-images.githubusercontent.com/105121789/214344251-5f8a5874-68b3-4740-b40a-71afd8a1a2bf.png)

We will configure the gateway

![image](https://user-images.githubusercontent.com/105121789/214348839-c82fe365-2862-4701-917e-164f85fb8e59.png)

After configuring the gateway we can set up a refresh time and day.

### As a final step we can create an app 


![image](https://user-images.githubusercontent.com/105121789/214354208-40c5e24a-fe77-4f45-8068-039029632245.png)

On the Content tab, you add the content from the workspace to the app.

* Select Add content on the Content tab.
* Select the contents that you want to add from the current workspace.
* Create and manage audiences
* On the Audience tab, we can create and manage audience groups within the app.

To create an audience, select New Audience.

Double-click the default audience label to change the audience name.

Select the hide/show icon next to each item in the workspace to determine the content that this app audience can see.

In the Manage audience access pane, specify groups or users to add to the current audience group.

For each audience group, grant access to either all people in your organization or specific users or groups. You can also expand the Advanced option to configure the following settings per audience group:

Allow users to share the datasets in this app: This option gives app consumers permission to share the app and underlying datasets of the app audience.

Allow users to build content with the datasets in this app: This option lets your app consumers create their own reports and dashboards based on the app audience datasets.

![image](https://user-images.githubusercontent.com/105121789/214354625-b3e69aa7-a823-4e53-a82e-ac19d7d77bc1.png)

Save a copy of a report
We can allow app users who have build permissions to save copies of reports to their workspace. Once they save the reports, the app users can customize the reports copies to meet their needs.

To enable your app users to save a copy, select the Allow users to make a copy of the reports in the app checkbox on the Setup tab.

Screenshot of save a copy checkbox in Setup tab.

### Publish the app

Now that you've decided on the audiences and the content for each audience, it's time to publish your app. You can install the app automatically for the recipients, if your Power BI admin has enabled this setting for you in the Power BI Admin Portal. 




