# Election-Winner
Shell scripting to combine, explore and analyze Big Data. Main idea is to predict who was more popular amongst Facebook users: Donald Trump or Hillary Clinton, from a messy data.

# How to understand the project?
The pdf contains all the shell commands to do specific tasks related to investigating the Facebook data along with the snapshots of each command. 
The .zip file contains all the data required for this project

# Task 1 - Data Manipulation
1) Decompress the file. How big is it (bytes)?
2) What delimiter is used to separate the columns in the file and how many
columns are there?
3) The first column is the unique identifier for each article. What are the other
columns?
4) How many articles are there in the file?
5) What is the date range for the articles in this file? (Assume that the data is in
order)
6) How many unique titles are there?
7) How many articles don’t have a title?
8) When was the first mention in the files regarding “Italian food” and what was
the title of the post?
9) How many times is “Hillary Clinton” mentioned in the articles? How did you
find this? (Do not ignore the case)

10) What about “Donald Trump”? Who is the focus on more articles, Clinton or
Trump? (Do not ignore the case)
11) Select the posts where “Trump” (Ignore the case) is mentioned in the post
content and number of likes for those posts are greater than 100. Generate a
new file with post_id and the sorted like_count and name it “trump.txt”. (In the
output, you need to show the headers as well) [Hint: Find Trump in the
message column, i.e., a specific column]. Then copy and paste the first 5 lines
of trump.txt in your answer.
12) Find the total number of love_count and angry_count for “Donald Trump” and
“Hillary Clinton” separately. Who has more positive feeling among people?
Justify your answer.
[Hint 1: you will need to search online to find how to sum a column of numbers
using awk.
Hint 2: You will need to consider both love and angry count when justifying your
answer.]
13) How many articles discussed Trump and Putin? How many discussed Trump but not
Clinton?
14) For each publication in trump.txt, find out which month had the most articles about
Trump. Try to do this without using grep.



# Task 2 - Data graphing
1) How many times does the term ‘Trump’ appear in the post message?
(use Unix shell to answer to this question)

2) We want to consider how the amount of discussion regarding Donald Trump
varies over the time period covered by the data file. To answer this question,
you will need to extract the timestamps for all posts referring to Trump using
shell. You will then need to read them into R and generate a histogram.
[Hint: To read the data into R, first generate a file containing only the
timestamp column as text, then read the file into R as a CSV.]
R will not recognise the strings as timestamps automatically, so you’ll need to
convert them from text values using the strptime() function. Instructions on
how to use the function is available here:
https://www.rdocumentation.org/packages/base/versions/3.6.1/topics/strptime
You will need to write a format string, starting with “%a %b” to tell the function
how to parse the particular date/time format in your file. What format string do
you need to use?

    1. Once you have converted the timestamps, use the hist() function to plot
        the data in R.
    2. The plot may have a bit of an unusual shape. Describe the pattern you
see.

3) In this question, we want to investigate the Facebook posts of a few top media
sources. To answer this question, you will need to extract the Facebook posts
made on the pages of "abc-news", "cnn" and "fox-news" from your original
Facebook dataset.

    1. Use the Unix shell to first generate a file containing all the records
belonging to "abc-news", "cnn" and "fox-news" only. Then read the
resulting file in R.
    2. Background: We now want to see if any relationship exists between the
number of times a post is shared on Facebook and the number of likes
it generates.
Task: Use appropriate R code to generate a plot showing the
relationship between the number of shares and the number of likes in
your dataset. Do you see any relationship?
    3. Fit a linear regression model using R to the above data (i.e.,
shares_count and likes_count) and plot the linear fit. Does it look like a
good fit to you?
    4. Use the linear fit to predict the number of likes a post will generate if itis
shared 0 times, 100 times, 1000 times, 10000 times and 100000 times
on Facebook.

