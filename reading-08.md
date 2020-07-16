# LINQs

## What are They?
LINQ stands for Language-Integrated Query. Based on query languages, this allows for some query functionality inside of C#. With LINQs You can write queries against strongly typed collections of objects by using language keywords and familiar operators. The LINQ family of technologies provides a consistent query experience for objects, relational databases and XML.

For anyone who is writing queries, the most visible "language-integrated" part of LINQ is the query expression. Query expressions are written in a declarative query syntax. By using query syntax, you can perform filtering, ordering, and grouping operations on data sources with a minimum of code. This should feel very similar to anyone familiar with database querying, except this time the qurey isn't held in a string, even though toa human the words in the query expression will be almost exactly the same.

## Expressions and Operators
#### Three Main Parts:
- Obtain the data source - ex. Provide a collection.
- Create the query - ex. Use the query statement on the collection assigned to a variable.
- Execute the query - ex. Loops thorugh the variable the represents the queried data.
#### Parts of the Query:
- Obtain a Data Source - using ```from <data> in <dataset>``` reference a data set that is enumberable.
- Filter that Data - using ```where <condition>``` filter in or out data based on specific conditions.
- Ordering - using ```orderby <data property>``` and ```ascending``` or ```descending``` to order the filtered data.
- Grouping - using ```group <data> by <property>``` you group the data that will be returned as a List of Lists.
- Joining - using ```join <new data> in <new data set> on <filtered data> equals <condition to check against>``` you can join one data set to antoher. Since LINQs don't have foreign keys the same way a group a databases might, dot notation can be used to reference another accessible data set.



[Table of Contents](README.md)