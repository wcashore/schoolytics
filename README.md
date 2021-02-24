# schoolytics

This app was written in pseudo code, using Plotly Dash. The general structure of the page is a series of dropdowns and tables. The tables created use the SQL prompts from the Assignment email. The dropdowns for each table indicate a variable that can be specified in order to pare down the results shown.


# Code Refactoring

I've added a refactored Jupyter notebook to this repository with an attempt at making the SQL queries dynamically generated. The refactored code is a functional app that accepts multiple user inputs and generates a SQL query according to the variables selected. Currently, the table and column options are hard-coded, because I’m unable to generate them dynamically.  However, the use-case of the query-generating function would be in a scenario where inputs are not generated from dropdown menus. The output of this app is only meant to illustrate the process of constructing a query based on different inputs. In a production environment, a similar function could accept inputs from a variety of sources, not just manual user inputs. In its current form, this app is simply generating a query string but in production it would feed the query into a database and extract the requested rows.

Below are the app’s outputs for the first three assignment query prompts.

## Group by student_id and count completed assignments
https://i.imgur.com/1xuka61.png

## Group by course_id and average grade
https://i.imgur.com/166q4Cr.png

## Group by teacher_id and count assignments created
https://i.imgur.com/RzZaOGt.png

 I had difficulty incorporating the 4th query (“Group by school_id and find percentage of students with more than 1 assignment completed”) into this application, so it was not included. The complexity of the function behind the scenes could be increased to accommodate for these kinds of expected outputs but I felt that the solution would be extremely cluttered if I did so. 
