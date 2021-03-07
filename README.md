# Spark++
__What are the advantages and disadvantages of Column-based storage? Explain these in plain English.__

The data format I used for this exercise was in Parquet, which is the opensource file format for the Hadoop. By storing the nested data structures in a Column-based storage, it gave a greate advantages and disadvantages in terms of storage and performance. It is also have been called as the future of Business Intelligence (BI). Below are some advantages and disadvantages of Column-based storage in the situations of the business usage.

__Advantages__: Column-based storage, compared to a row-oriented approach, has a great advantage in efficient storage for data. It stores each column as contiguous blocks, which is quite useful in a situation called online analytical processing (OLAP). 
I can get a great performance with retrieving information that is grouped together, and by not retrieving information that are unnecessary for the analysis.
Also, columnar databases reduces the amount of data that needs to be read from disk, by compressing similar data to reduce storage. This cannot be done with the row based storage, with different fields throughout.

__Disadvantages__: With all the advantages in column-based storage, there are some disadvantages too. It cannot be used for every use cases.
When writing a new record into a column-based database, it takes more computing resources as you have to write all the fields to the proper columns one at a time. With this reason, in the case of Online transaction-processing (OLTP) applications, the row-based storage is the better choice.

__What technical errors did you experience? Please list them explicitly and identify how you corrected them.__

In the beginning, I was using the Physical cluster until it gave me some trouble. 
When I moved to the docker, I had to download the 6Gb of data and configure the settings for my macbook pro to handle the tasks. 
However, the tasks were just too heavy for my laptop, as it crashed everytime I ran the `show()` function.
So I went back to using the physical cluster, and did a lot of troubleshooting with help from others. 
Finally, the cluster ran smoothly after fixing some function in the joining data part.

__What conceptual difficulties did you experience?__

In the beginning, I could not choose between the dataframe and SQL. I started with the SQL with more familiarity, but then realized that dataframe is more user-friendly in pyspark. There were some parts that I didn't have choice but to use SQL, but that was ok. 

__How much time did you spend on each part of the assignment?__

About 2~3 hours each. It could be faster if the computing environment did not give any stress on me. 

__Track your time according to the following items: Gitlab & Git, Docker setup/usage, actual reflection work, etc.__

- __GitLab & Git__: Pretty short with daily usage.

- __Docker setup/usage__: I switched between Docker and Physical cluster multiple times. Setting Docker wasn't too bad, except it crashed multiple times, which I had to spend a lot of time restarting the docker, and reopening the jupyter notebook.

- __Actual reflection work__: There were a lot of thinking process, but I could have done it faster if I didn't have that stress from Physical cluster.  

__What was the hardest part of this assignment?__

For me, I had the most difficult time with finding out the average % contribution of an order to the sellers daily quota.
I just did not understand what the question was asking until I read it for 30 times repeatedly.

__What was the easiest part of this assignment?__

The hashing part was relatively easy, as the hashlib library was provided to use. I didn't really have to do anything crazy with hashing.  

__What advice would you give someone doing this assignment in the future?__

First, I would give advice on have a good knowledge of what type of functions are available in pyspark functions. 
For example, countDistinct function exist for you to count only the distinct items in the column.

Second, know the data well. We had three different tables to work with, and foreign keys related to each other. 
However, one thing to be careful is that when joining tables, it must be in the proper order. 
This is where I had the trouble the most, as I didn't really care which table would be the left one when doing the inner join.

__What did you actually learn from doing this assignment?__

One thing I learned from this exercise is that there is nothing to be afraid of. Spark might be popular, but it was totally new to me. 
Even though I read all the papers and watched videos on it, still it was new to me until I had my hands on it. These were not some crazy difficult tasks, but it gave me a confidence to work on a bit more complex tasks using Spark. 
I am a better a better programmer compared to last week. That's all it matters. 

__Why does what I learned matter both academically and practically?__

This was the exercise that I got to work with relatively big data, compared to previous exercises.
Being able to practically use Spark is an essential for data science student, or data scientist in the industry.
I still got a long way to go, but this was a good first practice for me to actually handle a relatively big data in a cluster, which got rid of my fear of handling big data. 

## License
[MIT](https://choosealicense.com/licenses/mit/)