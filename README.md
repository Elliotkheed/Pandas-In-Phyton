# Pandas-In-Phyton
Pandas in Python
Pandas is one of the most powerful tools in the Python ecosystem, built specifically for data manipulation and analysis. At its core, it offers two flexible data structures,Series and DataFrame,that make handling datasets intuitive and efficient. With these, you can clean, transform, filter, and even visualize data without breaking a sweat.
Importing Pandas 
To use Pandas, the first step is to import it into your Python environment. Below is how we  import Pandas and give it an alias pd: 
import pandas as pd 
<img width="939" height="242" alt="image" src="https://github.com/user-attachments/assets/718c4cfb-4576-4f00-91ef-4d64f43ae652" />


This line means you can now use Pandas functions in your code by typing pd. before then. Bringing CSV Files into Pandas 
A CSV file (Comma Separated Values) is one of the most commonly used data formats. Example: Loading a CSV file 
df = pd.read_csv(r"C:\Users\Osas\Downloads\countries of the world.csv")
This line loads the CSV file, but to use the data, we must assign it to a variable. Bringing in a Text File 
A text file can also be loaded through Pandas. Sometimes, text files are separated by tabs instead of commas. In that case, we must specify  the separator. 
Separating Text Files Using sep 
<img width="939" height="154" alt="image" src="https://github.com/user-attachments/assets/c6a44dfd-3cbd-4ccf-b4e7-e6c203059dda" />

When working with text files separated by a tab, we use the parameter sep = '\t': 
 This ensures that the text is read correctly into columns. 
Bringing in a JSON File 

A JSON file stores data in a structured format similar to a dictionary. Loading JSON data is  done this way: 
Bringing in an Excel File 
Pandas can read Excel files easily. 
# Bringing a excel files

df = pd.read_excel(r"C:\Users\Osas\Downloads\world_population_excel_workbook.xlsx", sheet_name = 'Sheet1')
df
If an Excel file contains multiple sheets, you can select the specific sheet you want to load. 
Filtering and Ordering in Pandas
Filtering helps us extract specific rows or information from a dataset based on certain  conditions. 
Loading the Data to Filter 
import pandas as pd 
 Filtering Values Less Than 10 in the Rank Column 
df[df["Rank"] < 10] 
<img width="939" height="363" alt="image" src="https://github.com/user-attachments/assets/ae6b8225-8242-480f-a825-3823955c3a45" />

 
This displays only the rows where the Rank is less than 10 while carrying along all other  column information for those rows. 
Searching for Specific Countries Using isin()
<img width="939" height="290" alt="image" src="https://github.com/user-attachments/assets/01d65a49-75c0-4e36-84b5-4f311f1395a5" />

  
The isin() function is used when you want to search multiple values in a column. First assign the countries to a variable: 
our_countries = ['Bangladesh', 'Brazil'] 
Then filter the dataset using isin(): 
df[df['Country'].isin(our_countries)] 
This returns only the rows that contain Bangladesh or Brazil. 
Using str.contains() to Search Part of a Word 
when we can only remember a part of something but we seem not to be able to remember all of it
#works like LIKE in SQL


This works like the SQL LIKE operator. It helps when you remember part of a word but not  This will display all countries that contain the word United, such as United States or United  Kingdom.  

<img width="939" height="310" alt="image" src="https://github.com/user-attachments/assets/c114ccf8-6585-48f4-a36e-3405da08994d" />
