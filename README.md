# KPI and Quality Analytics Dashboard

## Project Scope


The purpose of this project was to address the lack of key performance indicator (KPI) visibility for coworkers, and to increase the efficiency and ease of use of the data entry process. 

By creating a single data entry app, this project aimed to condense data entry over multiple spreadsheets into a centralised database, making it easier for coworkers to input and access the following:

 - Worked hours
 - PTO balance
 - Overtime
 - Bank holidays
 - KPIs (Quality and Productivity)

This project aimed to provide a user-friendly interface for data entry and real-time access to data, improving transparency and efficiency in the workplace. With this app, coworkers could easily monitor their KPIs, access their data, and make informed decisions to improve their work performance.


## Features


### Interactive calendar 
The app includes an interactive calendar that allows users to quickly view the days for which they have created records. The calendar is filtered based on the specific user who is logged in, allowing for personalised tracking of their working hours, PTO requests, bank holiday hours, and overtime hours.

> <img src="https://user-images.githubusercontent.com/125451487/221929969-b59f4726-be8b-4d1c-8c13-18d5645ff527.jpeg" width=25% height=25%>

### New record creation 
The app includes a new record creation screen that provides users with the ability to input and save their working hours, PTO requests, bank holiday hours, overtime hours, and miscellaneous comments. The fields are auto-filled based on the user, making data entry more efficient.

> <img src="https://user-images.githubusercontent.com/125451487/221930641-f0faceb3-f9b4-4ae0-abc7-68e2a3cfe0f9.jpeg" width=25% height=25%>

### Record modification
Users are able to modify their own records in case of a mistake or to update their working hours, PTO requests, bank holiday hours, overtime hours, and miscellaneous comments.

> <img src="https://user-images.githubusercontent.com/125451487/221931432-183dbd61-afae-4645-a2a2-54ae7dd1a3c7.jpeg" width=25% height=25%>

### User Settings 
Users are able to edit their profiles to default to a number of options to enhance their experience. Default manager, language and hour selection are some of the customizations available.

> <img src="https://user-images.githubusercontent.com/125451487/221931212-938124f4-3828-41ce-a5bd-d349a3352307.jpeg" width=25% height=25%>

### Google Looker Studio dashboard 
>Users can launch a Google Looker Studio dashboard from the app in their browser. This enhances the user experience by providing visual renditions of the collected data, improving transparency and efficiency in the workplace


## Data


Data gathered through the App was fit for purpose by default, since I was able to ensure accuracy and consistency through data validation. Quality KPI data however came from a different source and needed manipulation prior to being used.

SQL was used to transform it into a more usable format for analytical purposes. The original grid-style wide format table had limitations when it came to data aggregation and analysis. To address this, columns were transformed into categories by grouping them using the following SQL query which was based on the unpivot operation that grouped a total of 11 columns into 1 Section column and added a Type column with the intersection result of the previous grid-style wide format table.

> <img src="https://user-images.githubusercontent.com/125451487/224489740-81d9c9f2-f294-49e2-b09b-838010b14d31.jpg" width=100% height=100%>


## Limitations


**Google Sheets row limit and filter functions:**  
> Since the app uses filter functions and Google Sheets does not support delegation, only the first 2000 rows of data can be used for storage. Once this limit is reached, a new worksheet must be added to the file and connections made within the app to continue recording data on the new sheet. This means that users should monitor the amount of data being entered to ensure that the 2000 row limit is not exceeded, and take action to add new worksheets as needed to continue recording data.

**Google Looker Studio connections:** 
> When a new sheet is added to the Google Sheets file, connections must be set up in Google Looker Studio to ensure that the data being visualised is accurate and up-to-date. This may require modifications to the existing dashboard to ensure that it is pulling data from the correct source. Users should be aware of this process and work closely with the Looker Studio team to ensure that connections are established properly and that data visualisations remain accurate and informative.
