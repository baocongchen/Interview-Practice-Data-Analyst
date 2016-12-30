# Interview-Practice-Data-Analyst

### 1. Describe a data project you worked on recently.
I recently worked on a project called "Make Effective Data Visualization". The goal of the project is to create a data visualization from a data set that tells a story or highlights trends or patterns in the data. I used dimple.js  to create the visualization. I used Prosper's loan data in this project. I built 3 charts that highlights the relationships between loan status with other variables such as employment status, loan term etc... I successfully built the charts and submitted my work. In the first review, the reviewer said that my work was great as a technical thing but he also pointed out that it was not explanatory, saying that I had created a very interesting set of charts that should engage the viewers to explore it in details, but the main aim of the project was to present explanatory visualization. I found out my big mistake, so I decided to add an explanation section to each chart. Moreover, I added an introduction section and a conclusion section. Some designs such as loading icon were also added. However, I did not collect feedback as required. So the reviewer recommended some questions I could pose to collect feedback. I got positive feedback from 3 people, but there were also some places they asked me to fix such as adding a link to download the data, adding a space to each word in a label to make it easy to read etc... I fixed them according to the feedback. Now everytime I look back at this project, I feel great about the process I went through and understand how important it is to collect feedback to improve user experience design. I think that this ability is something I could bring to my work at 23andMe. I would collect feedback from the customers, classify, analyze, and create solutions to improve their satisfaction with personal genetic services at 23andMe.

### 2. You are given a ten piece box of chocolate truffles. You know based on the label that six of the pieces have an orange cream filling and four of the pieces have a coconut filling. If you were to eat four pieces in a row, what is the probability that the first two pieces you eat have an orange cream filling and the last two have a coconut filling?

We have 6 orange cream chocolate truffles and 4 coconut chocolate truffles. The probability of selecting an orange cream chocolate truffles at this time is 6/10.

We have 5 orange cream chocolate truffles and 4 coconut chocolate truffles left, so the probability of selecting an orange cream chocolate truffles at this time is 5/9.

Now, we have 4 orange cream chocolate truffles and 4 chocolate truffles left, so the probability of selecting a coconut filling is 4/8.

So now we have 4 orange cream chocolate truffles and 3 coconut chocolate truffles. The probability of selecting a coconut chocolate truffle is 3/7.

Because the actions are related (truffles are taken one by one), the probability that the first two pieces you eat have an orange cream filling and the last two have a coconut filling is `(6/10) * (5/9) * (4/8) * (3/7) = 0.0714`

####Follow-up question:  If you were given an identical box of chocolates and again eat four pieces in a row, what is the probability that exactly two contain coconut filling?

<pre>
Combination 1: Orange, Orange, Orange, Coconut 
Combination 2: Orange, Coconut, Coconut, Orange
Combination 3: Orange, Coconut, Coconut, Coconut
Combination 4: Coconut, Coconut, Coconut, Coconut
...
Combination 14: Coconut, Orange, Orange, Orange
</pre>

There are 14 combinations available.
When you choose 2 coconut chocolates from 4 chocolates, there are 2C4 combinations, which is 6 combinations. 

The probability that you eat exactly two coconut chocolate is `6/14=0.42857`

### 3. Given the table users:

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

My answer: 

<pre>
SELECT state, sum(active) as num_active_users 
FROM users
GROUP BY state
ORDER BY sum(active) DESC
LIMIT 5
</pre>

### 4. Define a function first_unique that takes a string as input and returns the first non-repeated (unique) character in the input string. If there are no unique characters return None. Note: Your code should be in Python.

<pre>
def first_unique(string):
  # Use slicing to check for each character 
  for i in range(len(string)):
    # Check if there is no similar character existed before and after that character
    if string[i] not in string[0:i] and string[i] not in string[i+1:]:
      print string[i]
      return string[i]
  # Return None when there's no unique character
  return None
</pre>

### 5. What are underfitting and overfitting in the context of Machine Learning? How might you balance them?

Underfitting happens when an algorithm neither models the training data nor generalize to new data. The result is it does not perform well on both training data and new data. 

Overfitting happens when an algorithm models the training data so well that it fails to generalize to new data. The result is the performance on training data is high while its performance to predict new data is low.

To balance underfitting and overfitting, we use a right number of features, and do not over tweak the parameters. Doing this can help us avoid irrelevant detail and noise.

### 6. If you were to start your data analyst position today, what would be your goals a year from now?

I think at 23andMe I would be able to learn so much interesting knowledge about genomic analysis and report. I would feel excited about being part of a team that helps people examine genes to tell them about their ancestry, carrier status, wellness and traits. I would use this opportunity to collaberate with the team to develop data-driven product that will help people access, understand and benefit from the human genome. Because technology is evolving so fast, I will work hard while studying to become a senior data scientist, deepening my knowledge in data analytics, prediction models and user experience design, so I will enroll in Udacity's Machine Learning engineer program, AI engineer program, and Coursera's User Interaction Design specialization.

In the first 6 months, I will try to finish Machine Learning engineer program and User Interaction Design specialization to improve my ability to use metrics and analytics to measure and optimize the design of the report based on user interaction. After this, I will try to build a segmentation system that will help customize and generate report based on user's features. In the second 6 months, I will enroll in AI engineer program. After finishing this program, I want to develop a automatic design system based on user experience. 
