# Interview-Practice-Data-Analyst

## 1. Describe a data project you worked on recently.
I remember the challenge I had when I tried to build an algorithm for a project in Udacity Data Analyst Nanodegree program. The project name is "Identifying fraud from enron data". I learned about machine learning and prediction model when I enrolled in edX and Coursera online courses, and did a few projects related to this field in the past, but I can say that this project from Udacity's program was very challenging. I  looked at the project instruction and tried to figure out what I should do step by step. After that, I tried to run the python file that contained basic algorithm but it didn't work. So I researched online materials and used udacity forum to search for the same problem my peers may have. I finally found out that I did not download the necessary data because I forgot to run a python file required by Udacity. After I downloaded the data, I tried to import and visualize it to find out outliers, yet only successfully identified one outlier. The project review gave me a hint to find other 2 outliers. When I tried to build algorithms, I did not know how to get the best parameters for each algorithm, I researched online and found out that I could use GridSearchCV function to get best parameters. I chose 7 best features returned by the SelectKBest function, and my the performance of my naive bayse model finally exceeded the specification of Udacity. However, the project reviewer reminded me that I should explain the reason for choosing 7 best features that I selected; he also told me to measure the effect of new features in the final model by comparing its performances. Now, I know that it is also important that I can explain the process I go through when I build an algorithm.

## 2. You are given a ten piece box of chocolate truffles. You know based on the label that six of the pieces have an orange cream filling and four of the pieces have a coconut filling. If you were to eat four pieces in a row, what is the probability that the first two pieces you eat have an orange cream filling and the last two have a coconut filling?

We have 6 orange cream chocolate truffles and 4 coconut chocolate truffles. The probability of selecting an orange cream chocolate truffles at this time is 6/10.

We have 5 orange cream chocolate truffles and 4 coconut chocolate truffles left, so the probability of selecting an orange cream chocolate truffles at this time is 5/9.

Now, we have 4 orange cream chocolate truffles and 4 chocolate truffles left, so the probability of selecting a coconut filling is 4/8.

So now we have 4 orange cream chocolate truffles and 3 coconut chocolate truffles. The probability of selecting a coconut chocolate truffle is 3/7.

Because the actions are related (truffles are taken one by one), the probability that the first two pieces you eat have an orange cream filling and the last two have a coconut filling is (6/10) * (5/9) * (4/8) * (3/7) = 0.0714

## 3. Given the table users:

Table "users"

<pre>
+-------------+-----------+
| Column      | Type      |
+-------------+-----------+
| id          | integer   |
| username    | character |
| email       | character |
| city        | character |
| state       | character |
| zip         | integer   |
| active      | boolean   |
+-------------+-----------+
</pre>

Construct a query to find the top 5 states with the highest number of active users. Include the number for each state in the query result. Example result:

<pre>
+------------+------------------+
| state      | num_active_users |
+------------+------------------+
| New Mexico | 502              |
| Alabama    | 495              |
| California | 300              |
| Maine      | 201              |
| Texas      | 189              |
+------------+------------------+
</pre>

<code>
SELECT state, sum(active) as num_active_users 
FROM users
GROUP BY state
ORDER BY sum(active) DESC
LIMIT 5
</code>

## 4. Define a function first_unique that takes a string as input and returns the first non-repeated (unique) character in the input string. If there are no unique characters return None. Note: Your code should be in Python.

<code>
def first_unique(string):
  # Use slicing to check for each character 
  for i in range(len(string)):
    # Check if there is no similar character existed before and after that character
    if string[i] not in string[0:i] and string[i] not in string[i+1:]:
      print string[i]
      return string[i]
  # Return None when there's no unique character
  return None
</code>

## 5. What are underfitting and overfitting in the context of Machine Learning? How might you balance them?

Underfitting happens when an algorithm neither models the training data nor generalize to new data. The result is it does not perform well on both training data and new data. 

Overfitting happens when an algorithm models the training data so well that it fails to generalize to new data. The result is the performance on training data is high while its performance to predict new data is low.

To balance underfitting and overfitting, we use a right number of features, and do not over tweak the parameters. Doing this can help us avoid irrelevant detail and noise.

## 6. If you were to start your data analyst position today, what would be your goals a year from now?

I will work hard while studying to become a self-driving car engineer. I want to deepen my knowledge in data science and automation, so I will enroll in Udacity's self-driving car engineer program.

In the first 9 months, I will try to finish this program. After that, I will find a place where I can apply my new skills and work as a self-driving car engineer.