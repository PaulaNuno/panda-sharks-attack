

# panda-sharks-attack
W2 Project - Data cleaning & wrangling

​
## TODO's
​
1. Decide a hypothesis with which you will clean the data

Since 1975, when Jaws was released, the white shark has been reknowed as the most killer one over the years.
Let's see if that's true :)


I have to select the injury cases provoked by whithe sharks resulting in death.
Once I got them, I need to sort them by year.
Finally, I'm displaying a graph with the deaths caused by white sharks each year.
   
*Each row corresponds to a shark attack (https://www.kaggle.com/teajay/global-shark-attacks)  


2. Explore the data and write down what you have found
   - you can use: `df.describe()`, `df["column"]`, etc.
 
df.shape = 25723 rows, 24 series

There are some hidden series between "Sex" and "Species" that can't be seen in the raw DataFrame.

We check df.info() and we find the series must be analized taking into account the aim of the project:

Year (float)
Injury (object)
Fatal (Y/N) (object)
Species (object)

When analising the technical info the first thing that grabs my attention is the large number of nulls.
The file has almost 26000 (25723) entries and the number of non nulls in the series I'm working on is:

Year -------------> 6300
Injury -----------> 6274
Fatal (Y/N) ------> 5763 
Species ----------> 3464
   
I see that the number of rows in Year and Injury is quite the same, which could be great, but we have to check them.
On the other hand, we have only the half entries in Species comparing to Year ones.

*Checking Year: 

The min is 0, which is not possible, and the max, 2018.
If we take a look,the 25% corresponds to 1942 so we could think the begginig of the records stars around 1910 (when Titanic sunk).



   


3. Use at least 5 data cleaning techniques inside a file named `clean.ipynb`
   - null values, columns drop, duplicated data, string manipulation, apply fn, categorize, regex, etc.
4. Show data that validates the conclusions based on your hypotesis in a file named `analysis.ipynb`



Cleaning data 

- 25722 rows 
- Analizing the rows:
Desde la fila 25722 hasta la 8701, todos los campos aparecen como "NaN" en todas las columnas.
En la fila 8701 todos los campos siguen como NaN, si embargo, en la columna "Case Number" empiezan a aparecer registros "0"
Desde 8701 hasta 6302 todos los cases number son 0 y el resto NaN

df.loc[:] analizamos el contenido de las filas


 

​
## Suggested Ways to Get Started
​
- Examine the data and try to understand what the fields mean before diving into data cleaning and manipulation methods.
- Break the project down into different steps - use the topics covered in the lessons to form a check list, add anything else you can think of that may be wrong with your data set, and then work through the check list.
- Use the tools in your tool kit - your knowledge of Python, data structures, Pandas, and data wrangling.
  Work through the lessons in class & ask questions when you need to! Think about adding relevant code to your project each night, instead of, you know... procrastinating.
- Commit early, commit often, don’t be afraid of doing something incorrectly because you can always roll back to a previous version.
- Consult documentation and resources provided to better understand the tools you are using and how to accomplish what you want.
​
## How to deliver the project
​
1. Create a new repo with the name `data-cleaning-pandas` in your github account.
   - Create a `README.md` file on repo root with project documentation
   - At least 1 jupyter notebook is required
   - **DO NOT UPLOAD SHARKs ATTACK DATASET TO GITHUB**
2. Do a `PR` with the link of your repo copy pasted inside `m1/pandas-project/PROJECT-REPO.md` on our labs repo.
​
## Links & Resources
​
- <https://www.kaggle.com/teajay/global-shark-attacks>
- <https://numpy.org/doc/1.18/>
- <https://pandas.pydata.org/>
- <https://docs.python.org/3/library/functions.html