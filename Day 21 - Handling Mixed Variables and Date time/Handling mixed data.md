
#  Handling Mixed Variables and Date-Time

<br>

## Mixed variables : -
**Mixed variables** in data refer to the presence of different types of variables in a single dataset. In the context of machine learning, mixed variables can refer to the presence of both numerical and categorical variables, as well as the presence of both continuous and discrete variables.

Generally we will see 2 types of columns containing mixed variables

 1. **Numeric and Categorical Variables in the Same Column:**
 
-   This type occurs when a single column contains both numerical and categorical data. For example, a column might include alphanumeric codes where part of the code is numeric (e.g., product codes like P1234) and part is categorical (e.g., department codes like P).

-   **Example:** A column like 'Cabin' in Titanic dataset where each entry combines a letter (categorical) and digits (numeric), such as 'A12', 'B45', etc.

| Cabin |
|-------------|
| A12         |
| B45         |
| C58         |
| D128        |
| E76         |

Lets see how to deal with this kind of data


```python
df['cabin_num'] = df['Cabin'].str.extract('(\d+)') #Extract numerical part
df['cabin_cat'] = df['Cabin'].str[0] #Extract categorical part
```
code snippet to extract numerical part and Categorical part separately

| Cabin | cabin_num | cabin_cat |
|-------|-----------|-----------|
| A12   | 12        | A         |
| B45   | 45        | B         |
| C58   | 58        | C         |
| D128  | 128       | D         |
| E76   | 76        | E         |

---

 2. **Mixed Data Types within a Category:**
 
-   This type occurs when a column is supposed to be of one type (e.g., numeric), but due to data entry errors or heterogeneous sources, it contains a mix of numeric and non-numeric (categorical) values.

-   **Example:** A column like 'Ticket' in Titanic dataset where entries can be alphanumeric codes or purely numeric, such as 'B/4 11223', 'QC 23987', '556712', etc.

| Ticket           |
|------------------|
| B/4 11223        |
| QC 23987         |
| XON/O3. 9876543  |
| 556712           |
| 987654           |


Lets see how to deal with this kind of data


```python
df['ticket_num'] = df['Ticket'].apply(lambda s: s.split()[-1])
df['ticket_num'] = pd.to_numeric(df['ticket_num'],
                                   errors='coerce',
                                   downcast='integer')

# extract the first part of ticket as category
df['ticket_cat'] = df['Ticket'].apply(lambda s: s.split()[0])
df['ticket_cat'] = np.where(df['ticket_cat'].str.isdigit(), np.nan,
                              df['ticket_cat'])
```

Code snippet to divide mixed column into 2 different columns (i.e numeric and categorical)

| Ticket           | ticket_num | ticket_cat |
|------------------|------------|------------|
| B/4 11223        | 11223      | B/4        |
| QC 23987         | 23987      | QC         |
| XON/O3. 9876543  | 9876543    | XON/O3.    |
| 556712           | 556712     | NaN        |
| 987654           | 987654     | NaN        |

---
## Date and Time  variables : -

-   **datetime.datetime**: This class represents a datetime object, combining date and time information.
    
    -   Functions:
        -   `datetime(year, month, day, hour=0, minute=0, second=0, microsecond=0)`: Creates a datetime object.
        -   `datetime.now()`: Returns the current local datetime.
        -   `datetime.strptime(date_string, format)`: Parses a string into a datetime object based on the specified format.
-   **datetime.date**: Represents a date object (year, month, day).
    
    -   Functions:
        -   `date(year, month, day)`: Creates a date object.
        -   `date.today()`: Returns the current local date.
-   **datetime.time**: Represents a time object (hour, minute, second, microsecond).
    
    -   Functions:
        -   `time(hour=0, minute=0, second=0, microsecond=0)`: Creates a time object.
-   **datetime.timedelta**: Represents a duration, or the difference between two dates or times.
    
    -   Functions:
        -   Arithmetic operations (`+`, `-`, `*`, `/`) can be used directly with timedelta objects.
        -   `timedelta(days=0, seconds=0, microseconds=0, milliseconds=0, minutes=0, hours=0, weeks=0)`: Creates a timedelta object.
-   **datetime.timezone**: Represents a timezone object for aware datetime objects.
    
    -   `timezone.utc`: UTC timezone object.
-   **datetime.datetime.now()**: Returns the current local datetime.

## Commonly used function in Date  & Time Data
-   `date['date'].dt.year`: Extracts the year from each datetime in the 'date' column.
    
-   `date['date'].dt.month`: Extracts the month (1-12) from each datetime in the 'date' column.
    
-   `date['date'].dt.month_name()`: Returns the full name of the month for each datetime in the 'date' column.
    
-   `date['date'].dt.day`: Extracts the day of the month (1-31) from each datetime in the 'date' column.
    
-   `date['date'].dt.dayofweek`: Returns the day of the week as an integer (0-6, Monday-Sunday) for each datetime in the 'date' column.
    
-   `date['date'].dt.day_name()`: Returns the full name of the day of the week for each datetime in the 'date' column.
    
-   `date['date'].dt.isocalendar().week`: Returns the ISO week number (1-53) for each datetime in the 'date' column.
    
-   `date['date'].dt.quarter`: Returns the quarter (1-4) of the year for each datetime in the 'date' column.