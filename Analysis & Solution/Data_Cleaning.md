**Data Cleaning**

Dataset: The raw dataset is an Excel file named as raw_datset.xlsx.

Issue: The Exit Date column has many missing data

Problem: Due to missing data in Exit Date Column it's difficult to use the Exit Date column in the pivot table and pivot chart, because excel does          not allow a column to be used in pivot table if it has too many missing data

Solution: 1) Make another column known as Year_Exit
          2) Put condition such as that if a cell is empty in Exit Date then put -1 in the cell of Year_Exit and if the cell is not empty then find 
             the year from the date mentioned in the cell of Exit Date and put it in the cell of Year_Exit
          3) For example: =IF(N2="",-1,YEAR(N2))
             Here N2 is the cell reference of the Exit Date Column
          4) Now when pivot table is plotted by using Year_Exit instead of Exit Date, many -1 are shown in the chart then with the help of filter,                 many -1 are removed and we get pivot table showing the year of exit. The earlier problem of not able to plot pivot table due to empty              cells in the column is now removed

Issue: Employee ID column name is missing

Solution: Employee ID named as Emp ID

Note: Now in the cleaned excel file along with all pivot tables and pivot charts named as main_excel_file.xlsx many columns were added but those were part of the questions asked, and as far as cleaning was concerned there were only two issues missing data and employee id column name. Both these two issues were resolved.
      So the main_excel_file contains the cleaned data along with many added columns which were part of the questions asked in the project and it also contains pivot tables and pivot chart which help to analyse data.
