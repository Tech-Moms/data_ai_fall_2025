<img width="200" alt="Tech-Moms Logo Vertical" src="https://github.com/user-attachments/assets/02aae052-a29d-493b-bac1-a884f84a6891">

# Tech-Moms Student SQL Analysis 

In this assignment, you will use Deep Note, a data analysis tool, to explore the Tech Moms applicant dataset using SQL. You will upload the applicant dataset into Deep Note and answer key questions to gain insights from the data.

## Step 1: Create a Deep Note Account & Upload Data 

Deepnote.com is a collaborative data science notebook platform designed for data analytics and data science work. It allows users to write and run code in SQL (as well as Python and R) directly within the browser, making it accessible and easy to use without requiring software installation.

- [x]  Go to [Deep Note](https://deepnote.com/) and create a free account if you haven't already.
- [x] Download the `.csv` file of the Tech Moms applicant dataset [here](https://github.com/Tech-Moms/data-analytics-course/blob/main/module_3/assignment_2/Cleaned_Tech_Moms_Application_Data_9.12.2024.csv).
- [x] In Deep Note, create a new project.
- [x] Upload the `.csv` file into your project.

Video: [Overview, Create a Deep Note Account, & Upload Data](https://www.loom.com/share/5fc400d191dd414088c900cadbc439e5?sid=80486bf3-c3b9-400d-897e-f8f82eabd741)

## Step 2: Get to Know Your Data 

In order to get to know your data, you'll want to see a preview of the table. Use Deep Note's built-in SQL editor to explore the dataset. 

<img width="1524" alt="Screenshot 2024-09-12 at 8 25 50 AM" src="https://github.com/user-attachments/assets/9b5c2ebb-2428-48e3-91d0-19dd871578ec">

To start, write the following query: 

  ```
   SELECT
      *
   FROM [your_table_name]
   LIMIT 10;
  ```

_Note: [your_table_name] will be the exact name of the csv file you uploaded in double quotes. See example below._

<img width="700" alt="Screenshot 2024-09-12 at 8 31 52 AM" src="https://github.com/user-attachments/assets/97feb5d2-8f93-4dcc-9d88-d7b19ebc9187">


This will give you a preview of 10 rows so you can get to know what the data and columns look like generally. 

## Step 3: Analyze the Data (aka Ask Questions) 

Use Deep Note's built-in SQL editor to explore the dataset and answer the following questions:

1. **How many applications has Tech Moms received?** 
   - [ ]  Write a query to count the total number of applications. (as of the end of July)
   - Example SQL:
     
    ```
    SELECT 
      COUNT(distinct contact_id) -- to confirm there aren't duplicate use COUNT(distinct)
    FROM 'Cleaned_Tech_Moms_Application_Data.csv'
    WHERE create_date <= '2024-07-31' 
    ```

2. **How many applications were assigned a cohort?** 
   - [ ] Determine how many applicants were successfully assigned to a cohort. (as of the end of July)
   - Example SQL:
   
   ```
     SELECT 
      COUNT(distinct contact_id) as total_count --- to rename the column header in your SQL output use `as [new_column_header]`
     FROM 'Cleaned_Tech_Moms_Application_Data.csv'
     WHERE applicant_status = 'assigned cohort'
     AND create_date <= '2024-07-31' 
   ```

3. **How many children are supported through Tech Moms programs?** 
   - [ ] Find out the total number of children supported by the Tech Moms programs using the available data. (as of the end of July)
   - Example SQL:

   ```
   SELECT
     SUM(children) as total_children
   FROM 
   'Cleaned_Tech_Moms_Application_Data.csv'
   WHERE applicant_status = 'assigned cohort'
   AND create_date <= '2024-07-31' 
   ```

Note: Your numbers here should match your Excel/Google Sheets analysis. 
     
4. **Etc** 
     - [ ] Answer at least 10 additional questions using SQL

## Step 4: Submission

- [ ] Drop in a link to your completed project in [this discussion](https://github.com/Tech-Moms/data_ai_fall_2025/discussions/51).

#### How to Share a Deep Note Link:

Step 1: 

<img width="400" alt="Screenshot 2024-09-12 at 8 07 23 AM" src="https://github.com/user-attachments/assets/05c5ab15-fd04-4b0a-9822-72c894ae2734">

Step 2: 

<img width="400" alt="Screenshot 2024-09-12 at 8 08 27 AM" src="https://github.com/user-attachments/assets/705d32ec-831a-4a4b-8fb5-972b04379ea3">

Step 3:

<img width="500" alt="Screenshot 2024-09-12 at 8 09 38 AM" src="https://github.com/user-attachments/assets/1cf191d9-fafc-4a4e-904b-3ac51adaf7ba">

Step 4: 

<img width="500" alt="Screenshot 2024-09-12 at 8 11 12 AM" src="https://github.com/user-attachments/assets/9920c8db-81c4-4b4e-9193-d6cbd3a51b63">
