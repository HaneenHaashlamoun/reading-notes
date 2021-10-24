# Pandas

![panda](https://geo-python.github.io/site/_images/pandas-structures-annotated.png)

> pandas is like Excel in Python: it uses tables (namely DataFrame) and operates transformations on the data. But it can do a lot more.

> `import pandas as pd`

# The most elementary functions of pandas

## Reading data

>`data = pd.read_csv('my_file.csv')`

Some other great functions: read_clipboard (which I use way too often, copying data from Excel or from the web), read_sql

## Writing data

>`data.to_csv('my_new_file.csv', index=None)`

I usually don’t go for the other functions, like .to_excel, .to_json, .to_pickle since .to_csv does very well the job. And because csv is the most common way to save tables. There’s also the .to_clipboard if you’re like me an Excel maniac who wants to paste your results from Python to Excel.


## Checking the data

>`data.shape`

## Seeing the data

>`data.head(3)`

# The basic functions of pandas

## Logical operations

>`data[(data['column_1']=='french') & (data['year_born']==1990) & ~(data['city']=='London')]`

## Basic plotting

This feature is made possible thanks to the matplotlib package. As we said in the intro, it’s usable directly in pandas.
>`data['column_numerical'].plot()`

![plot](https://miro.medium.com/max/489/1*QyYuLym-PSTQk_3MYt81VA.png)

## Updating the data
>`data.loc[8, 'column_1'] = 'english'`

# Medium level functions

## Counting occurrences
>`data['column_1'].value_counts()`
![ex](https://miro.medium.com/max/378/1*7h20rGiaDoXUlWyfKhP1Vw.png)


## Operations on full rows, columns, or all data
The .map() operation applies a function to each element of a column.

>`data['column_1'].map(len).map(lambda x: x/100).plot()`

## tqdm, the one and only
When working with large datasets, pandas can take some time running .map(), .apply(), .applymap() operations. tqdm is a very useful package that helps predict when theses operations will finish executing (yes I lied, I said we would use only pandas).


>`from tqdm import tqdm_notebook`

>`tqdm_notebook().pandas()`

![ex](https://miro.medium.com/max/713/1*uerveZ-vqCl5sTyaeRLwSw.gif)

## Correlation and scatter matrices
>`data.corr()`

>`data.corr().applymap(lambda x: int(x*100)/100)`

![ex](https://miro.medium.com/max/875/1*VcCx97BF-kTMpzxbxPDqXg.png)


# Advanced operations in pandas

## The SQL join
>`data.merge(other_data, on=['column_1', 'column_2', 'column_3'])`

## Grouping
>`data.groupby('column_1')['column_2'].apply(sum).reset_index()`

![sql](https://miro.medium.com/max/728/1*2J7_KS-3EbDSICOj4OxoJg.png)

## Iterating over rows
>`dictionary = {}`
`for i,row in data.iterrows():dictionary[row['column_1']] = row['column_2']`


## Overall pandas is one of the reason why Python is such a great language

- simple to use, hiding all the complex and abstract computations behind
- (generally) intuitive
- fast, if not the fastest data analysis package (it highly optimized in C)


    
© Haneen Hashlamoun

