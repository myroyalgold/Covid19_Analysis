# Covid19_Analysis
COVID-19 (coronavirus disease 2019) is a disease caused by a virus named SARS-CoV-2. It can be very contagious and spreads quickly. Over one million people have died from COVID-19 in the United States.

COVID-19 most often causes respiratory symptoms that can feel much like a cold, the flu, or pneumonia. COVID-19 may attack more than your lungs and respiratory system. Other parts of your body may also be affected by the disease. Most people with COVID-19 have mild symptoms, but some people become severely ill.

# Problem Statement
- How bad was the COVID19 Prevalence?
- What are the Top 5 Countries with the Highest prevalence of COVID19?
- What are the Bottom 5 Countries with the Lowest prevalence of COVID19?
- Whats the rate of death to confirmed cases?
- What is the total confirmed cases by Year?
- What is the total confirmed cases by Month?
- What is the total confirmed cases by Day?

# Link to Dataset
https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series

# Data Transformation
### Step1: Loading Confirmed COVID19 Dataset
- Open Excel on your laptop
- Go to Data
- Select From web
- Go to link of the dataset provided, locate confirmed cases
- Copy and paste the url of the dataset in to excel and click on ok
![2024-06-10 (3)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/cdc3705f-5d8b-4359-8798-02ed8ed6cb8d)


- Access web content window will pop up then click on connect
  ![2024-06-10 (4)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/8981f88a-5ec9-462c-97c6-952219cda889)


- Select transform data 
![2024-06-10 (5)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/87b0cdcc-3a0f-41e5-b50a-d190daba2afb)


- Rename the timeseries data to confirmed
![2024-06-10 (6)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/213ac60e-0f6e-4269-a66c-d74a64239e92)


- Go to datasource, click on the drop down and clear column
![2024-06-10 (8)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/b3b91791-f1de-47e5-bc7c-aaf4b97390a0)


- Click on the icon beside column1 and use first row as header
![2024-06-10 (9)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/354a1241-99fd-44c0-a642-437afafb262d)


- Select province, country/region, lat, long(To do this hold your control key and select each column)
- Rightclick and select unpivot other columns
![2024-06-10 (11)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/2f22dc28-cef9-4775-90ce-3a9d4e2a80b6)


- Rename attribute to date and value to confirmed.
![2024-06-10 (12)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/c07070b4-3ac8-40f8-9974-a3fc5dff115f)


### Step2:  Loading Death COVID19 Dataset
- Rightclick on confirmed and duplicate it
![2024-06-10 (13)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/76905ada-06a1-46ad-86e2-fc0652f8b563)


- You will have confirmed2 rename it to death
![2024-06-10 (14)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/1a8c8d31-39f8-4c7d-aa94-3c5321aa6f79)

  
- Copy the url of death cases
- Go to setting icon beside Source on the applied steps
- paste the link copied to URL space and click Ok
![2024-06-10 (15)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/107b565f-ac8a-46d2-a5ce-10cd1d0d2b88)


- On the the applied steps, click on renamed columns
- Then on the columns next to date rename confirmed to deaths
  ![2024-06-10 (16)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/1aa6ef61-b9e1-4a42-b1a2-3abe81cc167e)


### Step3:  Loading Recovered COVID19 Dataset
- Right click on death and dupicate it
![2024-06-10 (17)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/00371f7b-dcde-4ba8-9638-85b1170f74f3)


- rename it  to recovered
![2024-06-10 (18)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/468d9d96-2251-4a64-adb7-1703dbc21a16)


- Copy the url for recovered in the link of the dataset provided
- Go to setting icon beside Source on the applied steps
- paste the link copied to URL space and click Ok
![2024-06-10 (19)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/95a18f05-5d40-47d8-9fb1-c265664ae623)

  
- On the the applied steps, click on renamed columns
![2024-06-10 (20)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/788c3a57-b0f8-41ea-a40c-838ec02bdf31)


- On the columns next to date rename deaths to recovered
![2024-06-10 (21)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/45fb236c-9158-4c3d-9564-9fc154c152ad)

### Step 4: Merge Data
- On the queries pane
- Select confirmed, Select merge query as new
![2024-06-10 (22)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/07e9c9f0-a18f-4358-a281-9a560f9e740e)


- Select death in the second merge pane
![2024-06-10 (24)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/14994fee-e23a-4f58-b044-4c12b1690458)


- Press and hold your controlkey and select Province/state, Country/Region and date in both confirmed and death
- Select Ok
![2024-06-10 (25)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/a1a99751-01f2-4d47-ac16-de7b897bd201)


- It will ask for privacy level, select public and save.
- Click on Ok
- On the queries pane, select merge1
- Click on the expand arrow next to death column
- Click to uncheck the select all, and select death
![2024-06-10 (27)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/3ff95f6f-a236-4d68-8d42-4072e24764a4)


- Click Ok and edit death.Death to Death
![2024-06-10 (28)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/c613e9a6-54ac-4fdb-9913-27924a7d46f1)


- Go to the queries pane and select merge1 and click on merge query
![2024-06-10 (29)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/28b802c8-aab2-4373-b6a8-9c8fb13d9294)


- To merge merge1 with recovered; on the merge dialog select recovered
![2024-06-10 (30)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/7ca84da0-5c29-4f0c-a9ad-65b32fa02c0a)


- select province/state, region/country and date and click Ok.
![2024-06-10 (31)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/29b186e4-9f2e-46a0-b6c0-47fee1cd78b5)


- Click on the expand arrow beside recovered
![2024-06-10 (32)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/2da2814e-01d8-451b-97e7-82c91a2d6754)


- Uncheck the checkbox to deslect all and select only recovered
![2024-06-10 (33)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/6d27e44e-1cd3-47e6-aeec-ab58c7b800be)


- Rename recovered.Recovered to Recovered
![2024-06-10 (34)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/5fb0648a-d0a4-4668-88b4-05ec8c3a2102)


-Select date column; Goto datatype and select date
![2024-06-10 (36)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/3716b8f2-3cbb-4cc4-b7ae-c1eaccab25fd)


- Rename merge1 on the queries pane to Consolidated_Data

- Click on close and load under File ribbon
![2024-06-10 (35)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/0afbb059-f2c9-4b28-9e40-82765b22f284)


# Data Manipulation
After the data is copmletely loaded
- On colum I1,J1 &K1 write Year, Month and Day.
- On column I2 type =YEAR(@[DATE]) and autofill.
![2024-06-10 (38)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/16513c94-5773-4e6f-bde9-0ccdb3e3a2e5)


- On column J2 type  =TEXT([@DATE],"mmmm") and autofill.
![2024-06-10 (39)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/4f72b4fd-c0ec-4c44-a6a7-60be94dbf6be)


- On column K2 type =TEXT([@DATE],"dddd") and autofill.
![2024-06-10 (40)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/3159790e-bdbd-4c48-9388-dcc212894107)


- On the Worksheet; select consolidated_data, go to table design and select summarize with pivot table.
![2024-06-10 (41)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/e5514c7c-47aa-43bd-9108-8c8374d74afd)


- Select OK
![2024-06-10 (42)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/e016c4f0-de0c-4787-8868-b568a4bce417)


- Start analyzing with pivot table.
![2024-06-10 (43)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/7f4f5232-1600-4234-bb52-a29bae249c02)

- Rename sheet2 to Analysis and add a new worksheet and rename it as dashboard.
- This is what my analysis sheet looks like
- ![2024-06-11](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/5d4732dd-72da-4d59-95b8-781f65c24298)


Note: The rate of death to confirm was calculated by Death/Confirmed

- This is what my dashboard looks like, but i am still not done with it.
![2024-06-11 (1)](https://github.com/myroyalgold/Covid19_Analysis/assets/107118603/59e59e59-f36c-45c2-a54b-ffcc4125606a)

HELLO!!!
This is my COVID19 Dashboard
insights were written on it for easy reading.
Thank you.





